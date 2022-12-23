## Small project using go with gin as a web service

### To run the project:
1. Create a module to manage the dependecies:
`$ go mod init example.com/web-service-gin`
2. Get the dependecies to project
`$ go get .`
3. Run the local server
`$ go run .`

### To test the endpoints:
- Get all albuns:
`$ curl http://localhost:8080/albums --header "Content-Type: application/json" --request "GET"`
- Get album by the ID:
`$ curl http://localhost:8080/albums/2`
- Add an album:
` curl http://localhost:8080/albums \
    --include --header \
    "Content-Type: application/json" \
    --request "POST" --data \
    '{"id": "4","title": "The Modern Sound of Betty Carter","artist": "Betty Carter","price": 49.99}'`