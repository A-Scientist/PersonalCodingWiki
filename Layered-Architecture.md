[\<\-Back](http://euclid.nmu.edu:3000/ovoisine/CS326/wiki/Practices)
# Layered Architecture
A coding architecture that provides a layout for how sections of code can be structured to interact with each other. Code in a layered architecture is, as the name implies, in horizontal layers. Pieces of code in one layer can communicate with others in its own layer, called (enter name here). Pieces of code in one layer can communicate with others in a layer directly above or below, called (enter name here). This provides isolation between layers of code, making the specific use of any layer clear and not making it harder for communication between pieces of code to become tangled. It also makes updating and replacing of code easier, as a specific layer can be updated while the others are left along. For example, consider a user case of 3 layers, one relating to a database, one for running calculations using data, and one of a user interface for inputting formulas. In a properly implemented layered architecture, if a new kind of database needs to be implemented for storing data, or a new kind of interface for imputing formulas, no work would need to be done to the other layers so long as the messages from the new layer are still recognizable by the old layer.<br>

## Preceding Patterns

## Use Cases

## Examples

## Following Patterns
See [MVC Model View Controller](http://euclid.nmu.edu:3000/ovoisine/CS326/wiki/MVC)