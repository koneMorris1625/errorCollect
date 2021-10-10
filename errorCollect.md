## ReferenceError: Invalid left-hand 

1. 场景还原

```js
const map = new Map();
for (let i = 0; i < n; i++) {
    const e = nums[i];
    if (map.has(target - e)) {
        return [map.get(target - e), i];
    }
    map.set(e) = i;
}
return [];
// const map = new Map();就一直报错: ReferenceError: Invalid left-hand side in assignment
```

2. 排查思路

给不能赋值的进行赋值, 出现该错误.
 `map.set(e) = i; --> map.set(e, i); `
