https://hooks.slack.com/services/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

curl -X POST --data-urlencode "payload={\"channel\": \"#devops\", \"username\": \"webhookbot\", \"text\": \"This is posted to #devops and comes from a bot named webhookbot.\", \"icon_emoji\": \":ghost:\"}" https://hooks.slack.com/services/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


curl -X POST --data-urlencode "payload={\"channel\": \"#devops\", \"text\": \"This is posted to #devops and comes from a bot named webhookbot.\"}" https://hooks.slack.com/services/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


curl -XPOST $url -d "[{\"status\": \"firing\",\"labels\": {\"alertname\": \"$name\",\"service\": \"my-service\",\"severity\":\"warning\",\"instance\": \"$name.example.net\"},\"annotations\": {\"summary\": \"High latency is high!\"},\"generatorURL\": \"http://prometheus.int.example.net/<generating_expression>\"}]"

curl -XPOST $url -d '[{"status":"firing", "labels":{"alertname":"name"}}]'

curl -XPOST $url -d '[{"status":"resolved", "labels":{"alertname":"name"}}]'

url= /api/v1/alerts

curl -H "Content-Type: application/json" -d '[{"status": "resolved","labels":{"alertname":"TestAlert1"}}]' 10.100.96.109:9093/api/v1/alerts



URL="http://localhost:9093/api/v1/alerts"

curl -si -X POST -H "Content-Type: application/json" "$URL" -d '
[
  {
    "labels": {
      "alertname": "InstanceDown",
      "instance": "localhost:8080",
      "job": "node",
      "severity": "critical"
    },
    "annotations": {
      "summary": "Instance is down"
    },
    "generatorURL": "http://localhost:9090/graph"
  }
]
'
