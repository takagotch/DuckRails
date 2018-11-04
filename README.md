### DuckRails
---
https://github.com/iridakos/duckrails

```
docker pull iridakos/duckrails
docker run -p 4000:80 iridakos/duckrails:latest

```

```
<%
  original_response = RestClient.get ""
  result = JSON.parse(original_response)
  
  result[:last_commits] = 10.times.map{|i| {
    changes: Random.rand(1000),
    date: (Date.today - Random.rand(10)),
    hash: Digest::SHA1.hexdigest("DuckRails-#{i}")
  }}
%>
<%= result.to_json %>


```

```
```
