# GRPC Testing

## pre-requisites

## Tutorial / Steps
### Creating a typescript project
https://khalilstemmler.com/blogs/typescript/node-starter-project/

### grpc tutorial link
Part 1: https://floydfajones.medium.com/creating-your-grpc-service-in-nodejs-typescript-part-1-1ee2c59367c2

Part 2: https://floydfajones.medium.com/creating-your-grpc-service-in-nodejs-typescript-part-2-19464c73320b

Part 3: https://floydfajones.medium.com/creating-your-grpc-service-in-nodejs-typescript-part-3-chat-9aca930cf3f7


### gRPC
#### install grpc tools etc

npm install @types/node --save-dev

npm install --save-dev @grpc/grpc-js

npm install --save-dev @grpc/proto-loader

npm install --save-dev ts-node grpc-tools @types/google-protobuf grpc_tools_node_protoc_ts 




### After creating the proto file, MUST RUN THIS COMMAND
need to run this command after writing each finished proto file:  
node_modules/.bin/proto-loader-gen-types --includeDirs ./proto proto/*proto --outDir proto/ proto/random.proto --grpcLib @grpc/grpc-js
** --outDir proto/(where the files generated will be placed) proto/random.proto (file that needs to be converted, need to list all if have more than 1 proto file)


## Running the client/server program
### Running the server
./node_modules/.bin/ts-node ./src/server.ts

### Running the client
./node_modules/.bin/ts-node client user1


