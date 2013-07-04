[GraphLayer](https://git.oschina.net/cloudcube/graphlayer)
=======


GraphLayer is a Graph database adapter! 

##Completed:
* Node(create/edit/relate/delete/properties)
* Relationship (create/edit/delete/properties)
* Index (create/edit/delete/add node/remove node/find/query)
* Cypher (Cypher queries|Query/Query with paremeter/get path)
* Traversals (Traversal using a return filter
  /return relationship from a traversal
  /return path from a traversal
  /traversal returning nodes below a certain depath
  /creatomg a paged traverser)-still under active development,


##To Do:
* Built-In Graph Algorithms
* Batch Operations
* Gremlin

##Documentation
See [GoDoc](http://godoc.org/github.com/innovationturbo/graphdb) for automatic

##Status
[![Build Status](https://travis-ci.org/innovationturbo/graphdb.png)](https://travis-ci.org/innovationturbo/graphdb)
[![Coverage Status](https://coveralls.io/repos/innovationturbo/graphdb/badge.png?branch=master)](https://coveralls.io/r/innovationturbo/graphdb)

This driver is a work in progress.  It is not yet complete, but may now be
suitable for use by others.  The code has an extensive set of integration
tests, but very little real-world testing. use in production at your own
risk.



##Install

	go get git.oschina.net/cloudcube/graphlayer



##Basic Example

	package main

	import (
		"log"
		//"github.com/innovationturbo/graphdb"  //github.com
		git.oschina.net/cloudcube/graphlayer //oschina.net
	)

	func main(){
		session,err:=Dial(dbConfig)
		if err!=nil{
			log.Println(err)
		}
		//create a node
		data:=map[string]interface{}{
			"name":"test",
			"key":1,
		}
		node1,err:=session.CreateNode(data)
		if err! = nil{
			log.Println(err)
		}
		......
	}

#License

graphdb is licensed under [AGPL V3](http://www.gnu.org/licenses/agpl.html), see LICENSE for more information.
