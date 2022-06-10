Here is an example of a vulnerable grpc implementation in C++.  
These examples came from https://github.com/grpc/grpc/blob/master/examples and were modified.
Refer to https://grpc.io/docs/languages/cpp/quickstart/ for running the server.
greeter_server.cc is vulnerable with the modifications made to it.

1. Follow the instructions to build and locally install gRPC https://grpc.io/docs/languages/cpp/quickstart/#build-and-install-grpc-and-protocol-buffers . If your vm crashes, use make -j4.
2. CD to this directory/cpp/helloworld
3. 
mkdir -p cmake/build
pushd cmake/build
cmake -DCMAKE_PREFIX_PATH=$MY_INSTALL_DIR ../..
make -j

4. Run the vulnerable server: ./greeter_server

The protos folder holds the protobuf files which are passed in client.py.  These can be changed here. 
