# led-controller
The general flow of data on this setup is:
- your program (processing, python, etc) sends data to server running on your computer
- server sends it to external controller via USB and handles everything from there

So, assuming hardware is setup correctly (will fill in later), all you have to do to have examples working is
- start up the server: go to fadecandy/bin and run fcserver-*your system*
- go to fadecandy/examples/*your language*. the processing strip64_dot is a pretty cool starting program.
- run your program, it'll automatically connect to the server and start sending data

You can send data directly to each LED using setPixel(number, color), but one nice feature from the end libraries is being able to map the LEDs to specific pixels on your program. This means your can display some visualization on your computer, then easily mirror particular parts of it to the led strand.
