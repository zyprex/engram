# engram

hugo theme engram

# javascript tips about throttle and debounce
```javascript
const throttle = (func, wait)=>{
  let last = 0;
  return (...args)=>{
    let now = Date.now();
    if (now-last < wait) return;
    last = Date.now();
    func.apply(null, args);
  }
}
/* test here
window.addEventListener('scroll', throttle(()=>{
   console.log("scroll!"+Date.now());
},2000));
*/
const debounce = (func, wait)=>{
  let timer = null;
  return (...args)=>{
    if (timer) {
      clearTimeout(timer)
    }
    timer = setTimeout(()=>{
      clearTimeout(timer);
      timer = null;
      func.apply(null, args);
    }, wait);
  }
}
/* test here
window.addEventListener('scroll', debounce(()=>{
  console.log("scroll!"+Date.now());
},1000));
*/
```

# ref

https://iconsvg.xyz/

https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Flexible_Box_Layout/Aligning_Items_in_a_Flex_Container
