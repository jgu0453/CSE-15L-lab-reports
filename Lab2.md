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
