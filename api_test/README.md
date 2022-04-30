# create basic api handler using go 

follows the steps documented here: 

https://tutorialedge.net/golang/creating-restful-api-with-golang/

## phase 1
build a basic handler using net/http package initially and creates a type handler to access a list of handlers
can be accessed using 
http://localhost:10000 - for the root page
and
http://localhost:10000/articles - to retrieve the full map of articles (specified in the main block) 

## phase 2
this phase replaces the basic net/http functionality with the gorrila/mux capability of the routers
also adds the ability to look up an article by Id,  the ids are added to the article struct and the map
### notes
when adding github.com/gorilla/mux package into the main imports you will also need to run the following command to import:

`go get github.com/gorilla/mux `  

useful details on the package can be found here https://pkg.go.dev/github.com/gorilla/mux@v1.8.0#section-readme

### phase 3 
this phase adds the remaining CRUD functions (read is in phase 2)
- create
- update 
- delete

## todo
pick up with Mutex handling to contrgol race conditions and consistency
create error handling for potential input errors

## Notes

useful sites
- https://mj-go.in/golang/crud-rest-api-with-gorilla-mux#put-a-user
