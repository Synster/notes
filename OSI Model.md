# OSI- Open Systems Interconnection Model
Standardises communication between systems
*MAC address- Media Access Control*

# Sender's View
## Layer 7 Application
## Layer 6 Presentation
## Layer 5 Session
## Layer 4 Transport
## Layer 3 Network
## Layer 2 Data Link
## Layer 1 Physical

# Recievers View
## Layer 1 Physical
This is the physical layer, in which 1 and 0 data bytes can be sent as electric signals, wifi, or light via "the wire"

## Layer 2 Data Link
These are the separation of the data bytes into frames.
Notably, the frames will identify the source and destination MAC addresses of the devices' network card.
Since electrical signals travel in all directions in a network, the data frames reach all devices in the network.
Once the data frame is able to identify that the device is not the intended destination, the frames drop.
In an unsecured network, this is where a malicious application can choose to not drop the frames, and steal the data.

## Layer 3 Network
Once layer 2 is done, it generalizes the frames from MAC addresses to IP addresses.

## Layer 4 Transport
This tranport layer further generalizes the network layer IP address into source and destination ports.

## Layer 5 Session
Since there may be several TCP connections to one server at a time, with identical packet information from layers 1 through 4, we need a way to distinguish the session by ID to tag it.

## Layer 6 Presentation
This is where the resource might be secured/encrypted with HTTPS/TLS by scrambling the HTTP request string.

At this step, if the data is encrypted, the model decrypts the information to reach step 7.
It might be possible that a malicious attack to steal data can be avoided by encrypting.
"This is where you can get screwed if you are on public wifi...people can sniff your unencrypted data."

## Layer 7 Application
This is where a client device makes a request to a server device, such as a GET request.
This request contains a whole bunch of information, such as headers, cookies, content-type headers, etc, which is summarized into a string, so the string can participate with the rest of the OSI models as byte data.

