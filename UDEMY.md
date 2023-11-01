# Refereence

## 9. HTTP Get from an API

* server: test-server
* client: http-get

Steps:

1. cd test-server
2. ./start-test-server.sh

3. cd http-get
4. go run main.go http://localhost:8080

```terminal
HTTP Status Code: 200
Body: The server is running!
```

5. go run main.go http://localhost:8080/words              
```
HTTP Status Code: 200
Body: {"page":"words","input":"","words":[]}
```

6. go run main.go http://localhost:8080/wordsss         
```  
HTTP Status Code: 404
Body: 404 Not Found
```

## 10. Parse HTTP JSON Response

* client: http-get-json
* server: test-server

Steps:

1. cd test-server
2. ./start-test-server.sh

3. cd http-get
4. go run main.go http://localhost:8080

```terminal
HTTP Status Code: 200
Body: The server is running!
```

5. ╰─ go run main.go http://localhost:8080/words\?input\=word2,word3
```
JSON: Parsed:
Page: words
Words: word2, word2,word3
```