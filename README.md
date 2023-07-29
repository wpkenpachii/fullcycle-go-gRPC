# fullcycle-go-gRPC


# Setup Commands
```shell

# setup to go with gRPC
sudo apt update
sudo apt install -y protobuf-compiler
go install google.golang.org/protobuf/cmd/protoc-gen-go@v1.28
go install google.golang.org/grpc/cmd/protoc-gen-go-grpc@v1.2
export PATH="$PATH:$(go env GOPATH)/bin"

protoc --go_out=. --go-grpc_out=. proto/course_category.proto # compile proto files
go mod tidy # install go grpc package
go install github.com/ktr0731/evans@latest # install evans to communicate with gRPC server create
sudo apt install sqlite3 # install sqlite3 to create tablse
```