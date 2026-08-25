# Malleable-jam
Let me inject my poison into your brain

![buh](https://github.com/nicolasbaez/Malleable-jam/blob/main/xp077.gif)
```javascript
setup = (_) => createCanvas((w = 500), w);
k = 0;
draw = (_) => {
  h = w / 2;
  background(99, 66, 0, 24);
  stroke(h, 99);
  for (i = k; i < 3 * PI + k; i += (3 * PI) / h) {
    r = w * 0.666 * noise(map(i, 0, 2 * PI, 0, w) * 0.01);
    fill(map(i, 0, 2 * PI + k, h, 0), 0, 0);
    circle(r * cos(i) + h, r * sin(i) + h, 9);
  }
  if (k == 0) saveGif("xp077.gif", 900, { delay: 0, units: "frames" });
  k += 0.005;
};
