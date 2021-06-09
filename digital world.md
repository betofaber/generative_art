## Now, creating a function that places a random rectangle with RGB code according to the related pixel color of (x, y) coordinates:
<br>

```
PImage digital;
float grid = 50;

void setup(){
  
  // in this section i load the previous image "digital world pattern"
  
  size(1080, 1080);
  digital = loadImage("digital.png");
  digital.resize(1080, 1080);
  background(245, 239, 208);
  
}

void draw(){
  
  for (int i = 0; i < 1000; i++){
    
    float x = random(width);
    float y = random(height);
    
    float d = 3;
    
    // this "get" function maps the color of each pixel on the image
    color cor = digital.get(int(x), int(y));
    
    // (adding a gride to make it fancy)
    if (x >= grid && x <= width - grid && y >= grid && y <= height - grid){
      noStroke();
      
      // here's where you apply the captured color
      fill(cor);
      rect(x, y, random(d), random(d));
    }
    
  }
  
  save("digitalll.png");
}

```
<br>

## As i made it with tiny rectangles, the results are not that different from the original image, but you can test it with a lot of shapes, sizes, opacities...

<br>

![digitalll](https://user-images.githubusercontent.com/69771514/121327950-488c7880-c8ea-11eb-9843-b1a43c26d5a0.png)
