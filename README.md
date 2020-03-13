# Carrots

[Live Link](https://btran1994.github.io/js-project/)

![alt text](https://i.imgur.com/R0RIJtH.png)

Carrots is a simple JavaScript and HTML5 Canvas platformer where your goal is to pick up all of the carrots.

# Technologies 

  * CSS3 to visually style the game canvas
  * HTML5 Canvas to render the pieces and the game canvas
  * JavaScript to handle other gameplay related functionality
  
# Features

  * Case based collision depending on different tiles that are rendered
  ![alt text](https://i.imgur.com/Au30PDH.png)
  * Simple controls and concept
  * Game design and engine that are easily expandable/modifiable 
  
# Controls 

  * Keydown event listeners were placed onto the window and utilized a switch statement to handle different key codes.
```javascript
    const Controller = function () {

    this.left = new Controller.ButtonInput();
    this.right = new Controller.ButtonInput();
    this.up = new Controller.ButtonInput();

    this.keyDownUp = function (type, key_code) {

        let down = (type == "keydown") ? true : false;

        switch (key_code) {
            case 37: this.left.getInput(down); break;
            case 38: this.up.getInput(down); break;
            case 39: this.right.getInput(down);
        }
    };
};

Controller.prototype = {
    constructor: Controller
};

Controller.ButtonInput = function () {
    this.active = this.down = false;
};

Controller.ButtonInput.prototype = {
    constructor: Controller.ButtonInput,
    getInput: function (down) {
        if (this.down != down) this.active = down;
        this.down = down;
    }
};
```
  
# Planned Features
  * Multiple zones
  * More objects to interact/pick up
  * Different models/sprites, custom ones perhaps?
  * Cross platform compatibility

Spritesheet and engine references from: https://github.com/frankarendpoth
