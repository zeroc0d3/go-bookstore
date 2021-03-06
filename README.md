# Simple Golang API
![goreport](https://goreportcard.com/badge/github.com/zeroc0d3/go-bookstore)
![all contributors](https://img.shields.io/github/contributors/zeroc0d3/go-bookstore)
![tags](https://img.shields.io/github/v/tag/zeroc0d3/go-bookstore?sort=semver)
![issues](https://img.shields.io/github/issues/zeroc0d3/go-bookstore)
![pull requests](https://img.shields.io/github/issues-pr/zeroc0d3/go-bookstore)
![forks](https://img.shields.io/github/forks/zeroc0d3/go-bookstore)
![stars](https://img.shields.io/github/stars/zeroc0d3/go-bookstore)
![license](https://img.shields.io/github/license/zeroc0d3/go-bookstore)

## Development
### Prequests
* Install jq libraries
  ```
  apt-get install -y jq
  ```
* Install golang dependencies
  ```
  go mod init
  go mod tidy
  ```

### Runnning
```
go run main.go
```

## API Test
* Get Books
```
GET    : /books
         curl --request GET \
            --url 'http://localhost:8080/books' \
            --header 'Content-Type: application/json' | jq
```

* Add Book 1
```
POST   : /books
         curl --request POST \
            --url 'http://localhost:8080/books' \
            --header 'Content-Type: application/json' \
            --data '{
                "title": "Mastering Go: Create Golang production applications using network libraries, concurrency, and advanced Go data structures",
                "author": "Mihalis Tsoukalos"
            }' | jq
```

* Add Book 2
```
POST   : /books
         curl --request POST \
            --url 'http://localhost:8080/books' \
            --header 'Content-Type: application/json' \
            --data '{
                "title": "Introducing Go: Build Reliable, Scalable Programs",
                "author": "Caleb Doxsey"
            }' | jq
```

* Add Book 3
```
POST   : /books
         curl --request POST \
            --url 'http://localhost:8080/books' \
            --header 'Content-Type: application/json' \
            --data '{
                "title": "Learning Functional Programming in Go: Change the way you approach your applications using functional programming in Go",
                "author": "Lex Sheehan"
            }' | jq
```

* Edit Book 3
```
PATCH   : /books/3
         curl --request PATCH \
            --url 'http://localhost:8080/books/3' \
            --header 'Content-Type: application/json' \
            --data '{
                "title": "Test Golang",
                "author": "ZeroC0D3Lab"
            }' | jq
```

* Delete Book 3
```
DELETE   : /books/3
         curl --request DELETE \
            --url 'http://localhost:8080/books/3' \
            --header 'Content-Type: application/json' | jq
```
