// View output to see simulator.
// Drag the model to rotate.
// Open JavaScript console to view errors.

(new Blinken({title: "Red Snake", 
              author: "Anonymous"})).run(() => {
  // My self-contained program goes here.    
  let rainbowColors = [
    {"r": 255, "g": 0, "b": 0},
    {"r": 252, "g": 165, "b": 3},
    {"r": 252, "g": 248, "b": 3},
    {"r": 0, "g": 255, "b": 0},
    {"r": 0, "g": 0, "b": 255},
    {"r": 223, "g": 3, "b": 252},
    {"r": 255, "g": 176, "b": 204} 
  ];
  
  let lightColors = {};
  

  // Update lights one frame
  return (lights) => {
    for (let i = 0; i < lights.length; i++) {
      color = lightColors[i]
      if (color) {
         color = lightColors[(i+1)%(lights.length)];
         lightColors[i] = color;
         lights[i].rgb(color.r/255, color.g/255, color.b/255);
      } else {
         color = rainbowColors[i%6]
         lightColors[i] = color;
         lights[i].rgb(color.r/255, color.g/255, color.b/255);
      }
    }
    
    return 100; // ms until called again
  };
});
