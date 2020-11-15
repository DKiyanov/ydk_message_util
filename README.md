# Library for working with ABAP messages
This is a simple class that contains several static methods, types and constants that can be useful when working with SAP messages and for raise exceptions with given messages.

## Class YDKMSG
### method MESSAGE_MOVE_TO 
Transferring message data from one structure to another, so historically SAP has many variants of field names in structures containing message data, and quite often it is necessary to transfer these data from one structure to another.  
Parameters:
* SRC - importing, any structure
* DEST - changing, any structure
 
### method MESSAGE_TO_STR
Generates a message string from the message parameters 
unlike standard methods, MSGV1...MSGV4 parameter values are not truncated to 50 characters  
Parameters:
* MSG_STRUCT - importing, any structure

### method DISPLAY_MESSAGE
Display a message to the user 
Parameters:
* MSG_STRUCT - importing, any structure

### method RAISE_MESSAGE
Raise an exception of class ycx_dk_msg with message data  
All parameters are importing:
* MSGID - message class
* MSGNO - message number
* MSGTY - message type
* MSGV1, MSGV2, MSGV3, MSGV4 - message parameters

### method RAISE_MESSAGE_FROM
Raise an exception of class ycx_dk_msg with message data   
Parameters:
* MSG_STRUCT - importing, any structure

### method RAISE_TEXT
Raise an exception of the ycx_dk_msg class with free text   
Parameters:
* TEXT - importing, текст

### method RAISE_MESSAGE_EVENT
Raise event YDKMSG=>MESSAGE with message data  
Parameters:
* MSG_STRUCT - importing, any structure

### set of constants C_MSGTY
Contains possible values for the MSGTY field of the message

#### redeclaring the types of several of the most commonly used message structures