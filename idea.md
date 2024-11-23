# SimpleRPC

## Why

### I had a lot of services each needing to access different services and so i quickly discovered quicklu that "REST" is not the answer cuz of  both  the `resource driven architecture` which was not fit for my procdures oriented rather than resources CRUD orientated services and also the `JSON overhead` after a bit of search i decided to use `gRPC` and i liked it and used it for some services but i quickly started to dislike the amount of setup needed and being forced to use a certain person implemenation of the generated server and client without having any alternative. Also i am a huge fan of the repo pattern and seeing that remote procedures could easily make generating browser client code easier than ever before in the repo stype which is so good.

### Also i thought it would be good learning experience and might fix the problem of not having a lightweight gRPC alternative that could also be supported easily in the browser since everyone 

### To summarize i needed something which was able to create typesafe api client and servers, didnt have the `JSON overhead`, was relatively easy to set up (so that REST doesnt get choosed over it just cuz its easy) and deploy (grpc is kinda complex to set up in CICD) and onboard new people (a probelm of grpc exclusively is that it is considered a bit hard to use although i didnt really think it was), potentially being able to run in the browser so that i can generate clients on the browser and potentially being able to easily use with my already `REST` services to generate clients. Basically you can think  of it as plugin based trpc

## What

### So given this and the fact that i had too much free time i decided to make my own `plugin based` Rpc framework which just like grpc uses a intermidiary lang and but the difference is that i am not locked to the client and server implementation, essentially just making a client and server compilers for thee tools i use rather than using their own provided

## Alternatives i have tried

### OpenAPI and Swagger

#### Pros 

- it was a lot easier to set up since the set up process was easy on both the client and server
- almost type safe (if your openapi config is not correct neither the tool will be and also not all framework support automataic openapi docs and beither it will be possible)

#### Cons

- it still had the `JSON overhead` probelm although it supported different ways only the standard REST was 

### tRPC

#### PROS 

- easy to setup and work with 
- typesafe

#### CONS

- only for ts

