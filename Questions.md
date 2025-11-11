# What is gRPC and why does it work accross languages and platforms?
    gRPC is a modern open source high performance Remote Procedure Call (RPC) framework that can run in any environment.
    It genereates the Files for the Server and Client automatically in the version you need

# Describe the RPC life cycle starting with the RPC client?
    Once the client calls a stub method, the server is notified that the RPC has been invoked with the client’s metadata for this call, the method name, and the specified deadline if applicable.
    The server can then either send back its own initial metadata (which must be sent before any response) straight away, or wait for the client’s request message. Which happens first, is application-specific.
    Once the server has the client’s request message, it does whatever work is necessary to create and populate a response. The response is then returned (if successful) to the client together with status details (status code and optional status message) and optional trailing metadata.
    If the response status is OK, then the client gets the response, which completes the call on the client side.
# Describe the workflow of Protocol Buffers?
    create a .proto file
    use a proto compiler
    code gets auto generetad in the waned language
# What are the benefits of using protocol buffers?
    compact, no specific language and the code gets auto generated
# When is the use of protocol not recommended?
    human readability and when it is a one time call/use
# List 3 different data types that can be used with protocol buffers?
    int, String, bool