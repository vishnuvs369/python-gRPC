mkdir grpc_example

cd grpc_example

virtualenv -p python3 env

source env/bin/activate

pip install grpcio grpcio-tools


# For implementing gRPC services, we need to define three files

Proto file -  unary.proto

Once we are done with the creation of the .proto file, we need to generate the stubs. For that, we will execute the below command:-

python -m grpc_tools.protoc --proto_path=. ./unary.proto --python_out=. --grpc_python_out=.


Two files are generated named unary_pb2.py and unary_pb2_grpc.py. Using these two stub files, we will implement the gRPC server and the client.

# Implementing the Server

unary_server.py

python unary_server.py

# Implementing the Client

unary_client.py

Let's check the output:-
Run ->
python unary_client.py 
