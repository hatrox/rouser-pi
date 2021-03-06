# pi-rouser
### Abstract
My main home computer gets connected to the Internet via Wi-Fi, due to it being too far from the Internet cable entry point and therefore the router. Whenever I'm not home that same computer is suspended and I don't have access to it. I need a mechanism of waking it up, regardless of where I am, so I'm able to access my files. One such way is the WoWLAN protocol, though due to its somewhat paradoxical nature (the computer needs to be suspended AND maintain a Wi-Fi connection AND be able to be woken up via the Wi-Fi adapter driver), it didn't get widespread industry support and a very small amount of Wi-Fi cards support it. In thinking about this I remembered I have an old Raspberry Pi Model A which hasn't been used in quite a while, and motivated by my love of reappropriating old tech I have lying around, I'll build a quick Python HTTP server on it,  serving an API with a POST route. When the route is hit, it'll send a magic packet to my PC and start pinging it, letting the user know of whether the computer was woken up successfully. The route should also have some sort of a simple security verification as well. The Raspberry has an Ethernet port, which will get connected to PC's network card and I'll use an old Wi-Fi dongle, which will expose the Pi to my Wi-Fi network.
<br>
This server requires the 'etherwake' package.
<br>
![rouser pi meme](https://github.com/hatrox/rouser-pi/raw/master/rouser-pi-meme.jpeg)
<br>
yeah, welcome to the club, pal.
