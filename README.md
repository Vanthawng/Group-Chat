# Group-Chat
Testing
01
import java.io.*;
02
/*
03
 * This class defines the different type of messages that will be exchanged between the
04
 * Clients and the Server.
05
 * When talking from a Java Client to a Java Server a lot easier to pass Java objects, no
06
 * need to count bytes or to wait for a line feed at the end of the frame
07
 */
08
public class ChatMessage implements Serializable {
09
 
10
    protected static final long serialVersionUID = 1112122200L;
11
 
12
    // The different types of message sent by the Client
13
    // WHOISIN to receive the list of the users connected
14
    // MESSAGE an ordinary message
15
    // LOGOUT to disconnect from the Server
16
    static final int WHOISIN = 0, MESSAGE = 1, LOGOUT = 2;
17
    private int type;
18
    private String message;
19
     
20
    // constructor
21
    ChatMessage(int type, String message) {
22
        this.type = type;
23
        this.message = message;
24
    }
25
     
26
    // getters
27
    int getType() {
28
        return type;
29
    }
30
    String getMessage() {
31
        return message;
32
    }
33
}
