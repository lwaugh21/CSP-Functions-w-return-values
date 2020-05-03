# CSP-Functions-w-return-values
wrap around turtle
penUp();
var xloc = 160;
var yloc = 240;

onEvent("screen1", "keydown", function(event) {
  if (event.key == "Left") {
    xloc = xloc - 10;
  } else if (event.key == "Right") {
    xloc = xloc + 10;
  } else if (event.key == "Up") {
    yloc = yloc - 10;
  } else if (event.key == "Down") {
    yloc = yloc + 10;
  }
  
  updateTurtle();
});

function updateTurtle() {
  xloc = wrap(xloc,0,320);
  yloc = wrap(yloc,0,450);
  moveTo(xloc, yloc);
}

function wrap(input, low, high) {
  var output;

  //your code goes here
  if (input < low) {
    output = high;
  } else if ((input > high)) {
    output = low;
  } else {
    output = input;
  }
  
  return output;
}
