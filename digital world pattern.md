## Creating a background with rectangles of random colors with 50% opacity:
<br/>

```
void setup(){
  size(800,800);
  background(100, 100, 200);
}

void draw(){

  // this generates the rectangles recursively
  
  for (int n = 0; n < 50; n++){
    noStroke();
    fill(random(255), random(255), random(255), 50);
    rect(random(width + 200) - 100, random(height + 200) - 100, 80, 40);
  }
  
  // "save()" function saves the last frame displayed in the Processing compiler
  
  save("digital.png");
}
```

<br/>

## It will look like this:
<br/>

![digital](https://user-images.githubusercontent.com/69771514/121327264-ab314480-c8e9-11eb-9461-a31df257a5fd.png)
