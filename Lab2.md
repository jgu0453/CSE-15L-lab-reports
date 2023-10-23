```java
import java.io.IOException;
import java.net.URI;

class Handler implements URLHandler {
    
    StringBuffer sb = new StringBuffer();
    int count = 1;

    public String handleRequest(URI url) {
        if (url.getPath().equals("/add-message")) {
            String[] parameters = url.getQuery().split("=");

            if (parameters[0].equals("s")){
                String full = parameters[1].replace('+', ' ');
                sb.append(Integer.toString(count) + ". ");
                sb.append(full);
                sb.append(System.lineSeparator());
            }
            count += 1;
            String str = sb.toString();
            return str;
        } else
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

        Server.start(port, new Handler());
    }
}
```
![image](https://github.com/jgu0453/CSE-15L-lab-reports/assets/119398520/bf0bb389-d39f-41c8-94f0-7641dd8594b5)
![image](https://github.com/jgu0453/CSE-15L-lab-reports/assets/119398520/2e38f7d3-7b95-4b7c-b1b2-a9518449ef2e)

Screenshot 1:
It calls the String handleRequest(URI url) and the Server.start(port, new Handler()) method.
The Server start method takes a port number and a new Handler object and the HandleRequest method takes a url argument.
The Stringbuffer sb gets a new string appended and count is incremented by 1.

Screenshot 2:
It calls the String handleRequest(URI url) and the Server.start(port, new Handler()) method.
The Server start method takes a port number and a new Handler object and the HandleRequest method takes a url argument.
The Stringbuffer sb gets a new string appended, adding on to the string appended in screenshot1, and count is incremented by 1 again.
