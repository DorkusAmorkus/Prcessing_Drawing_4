# Prcessing_Drawing_5


/* Your name: Elias Han

Date: 9/28/18

Project/assignment name: Java Sketch

Description: click square to spin and change color

Credits for code referenced:
https://processing.org/tutorials/color/
https://processing.org/tutorials/interactivity/

notes: 
uses mouse input
color
pshape
rectangle
*/

PShape rectangle;

void setup() {  //sets up our shape
  size(800,800,P2D);
  rectMode(CENTER);
 rectangle = createShape(RECT,mouseX,mouseY,100,100);
  rectangle.setStroke(color(0,0,255));
 rectangle.setStrokeWeight(4);
  rectangle.setFill(color(255,0,255));
}

void draw() {  //sets up mouse movement correlation to shape
  background(69);
  translate(mouseX, mouseY);
  shape(rectangle);
  
  if (mousePressed) {
    rectangle.setFill(color(255,0,255)); //purple
  } else {
    rectangle.setFill(color(0,255,255)); // cyan
  }
}
void mousePressed() {
  
  rectangle.rotate(QUARTER_PI);  //rotates the object 45 degrees when you click the mouse
}
