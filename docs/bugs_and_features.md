# Current known bugs/features yet to be fixed

## Bugs

Here are a list of bugs that have yet to be fixed.

- There is a latency delay between the real-time pygame window and the pygame window being shown on the web interface. Because the console screen outputs print statements from Chronos at real-time, the delay would be apparent to the user of the web interface. 
    - A quick fix is to add a sleep function to delay the console output by an arbitrary number of seconds to make it appear that there is no delay (since the console outputs would run in parallel with the visualisations). However, this would not be a permanent solution especiailly when it comes to sending commands - commands have to be sent in real-time and has to be reflected immediately. 
- The 'send command' button does not work in all cases (this is configured in the .js code). Right now, the safest option is to press the Enter key to send commands.
- Commands should not be allowed to be sent when Chronos is not running - this should be implemented
- Console window is made to stick the scroll to the bottom of the window when not interacted with to allow the console window to scroll while there is additional logs being shown. This is however made possible using an arbitrary magic number. Do refer to the `consoleOut` function in the custom javascript file.

## Features to implement

Here are some of the features that you may be able to implement. Feel free to implement them if you wish!

- Create a class just like `web_table` that connects the graph on the web interface to Chronos
- Automate the window size of the web interface to fit the pygame window's window size (since different pygame simulations can come in different window sizes)

