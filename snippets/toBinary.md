---
title: Decimal to binary
tags: algorithm,recursion,binary
expertise: intermediate
author: ShivamPande18
cover: blog_images/building-blocks.jpg
firstSeen: 2022-10-13T21:09:30+02:00
lastUpdated: 2022-10-13T10:00:58+02:00
---

Convert a decimal into binary using recursion.

- Declare a variable, `bin`, that will store the binary digits one by one untill we get the whole number converted.
- Declare a variable, `remiander`, to store remiander in each step.
- Declare a variable, `i`, to give the place value of the binary number..
- Use a `while` loop to iterate over each place of the number untill its equal to 0.
- Use the modulus operator (`%`) to get reminder of `x`.
- Use the `parseInt` function to reduce `x/2` to an integer number.
- If `x` is even 0 is added to `bin` else 1 is added


```js
function toBinary(x) {
    let bin = 0;
    let remainder, i = 1;
    while (x != 0) {
        remainder = x % 2;
        x = parseInt(x / 2);
        bin = bin + remainder * i;
        i = i * 10;
    }
    return bin
}
```

```js
toBinary(100); // 1100100
```