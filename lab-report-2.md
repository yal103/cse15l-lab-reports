# Lab Report 2 - Servers and Bugs
**Yangyang Liu \
CSE 15L Section B02 \
PID: A17360266**

## Part 1 - StringServer
Here is an implementation for a web server called `StringServer`. \
It keeps track of a single string that get added to by incoming requests.

Note: It makes use of the `Server.java` file found [here](https://github.com/ucsd-cse15l-f22/wavelet/blob/master/Server.java).

```java
// In StringServer.java file

import java.io.IOException;
import java.net.URI;

class StringHandler implements URLHandler {
    
    String str = "";

    public String handleRequest(URI url) {
        if (url.getPath().equals("/")) {
            if (str.equals("")) {
                return "Start adding words";
            }
            return str;
        }
        else if (url.getPath().contains("/add-message")) {
            System.out.println("Path: " + url.getPath());
            String[] parameters = url.getQuery().split("=");
            if (parameters[0].equals("s")) {
                str += (parameters[1] + "\n");
                return parameters[1] + " has been added.";
            }
        }
        return "404 Not Found!";
    }
}

class StringServer {
    public static void main(String[] args) throws IOException {
        if(args.length == 0){
            System.out.println("Missing port number! Try any number between 1024 to 49151");
            return;
        }

        int port = Integer.parseInt(args[0]);

        Server.start(port, new StringHandler());
    }
}
```
  
