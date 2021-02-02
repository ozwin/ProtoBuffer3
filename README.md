# GO ProtoBuffer3 
 Demo of Protocol buffer 3 with GO
 
 
Installation 

Download the proto3 compiler  from https://github.com/protocolbuffers/protobuf/releases/tag/v3.14.0  and keep the exe in GOPATH  e.g C:\Users\{Name}\go\bin and copy the include folder from the zip to same folder e.g C:\Users\{Name}\go

Run the command  go get github.com/golang/protobuf/protoc-gen-go to add the protobnf plugin for GO

Step 1 : 
Create a file with .proto extension to create message  e.g addressbook.proto

option go_package = "./output"; -> Use a directory path where teh generate code should be stored

run the below command to generate code for the .proto file
protoc -I={exact directory  path} --go_out={exact directory path} {exact directory path}\addressbook.proto


Import  the generated file output/addressbook.pb.go in your code 


e.g import (pb "./output)




# How to run
  To add a entry to the file addressbook.data
    
    go run .\addPerson.go addressbook.data
 To list the data
 
    go run .\ListPerson.go addressbook.data





