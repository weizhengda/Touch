# day01

1. 在手机端，touch事件来替代鼠标事件
   - touchStart，手指触摸到屏幕时触发，
   - touchEnd，手指离开屏幕时触发，
   - touchMove，手指在屏幕上滑动或拖动时触发
   - touchCancel，一些系统事件触发，会关闭触摸事件
   
2. touch事件对象的3个常用属性,他们的值都是一个touchList(数组类型)
   - touches
   - targetTouches
   - changedTouches
> 以上3个属性
   
3. touchList是touch对象的集合，每个对象:
   - identifier 
   - clientX
   - clientY
   - pageX
   - pageY
   - screeX
   - screenY
   
4. 手机端上没有鼠标事件，但是有click事件
   
5. 手机页面上做click事件时会有300ms的延迟（系统留下时间来判断用户操作的类型，避免误操作）

6. 因为在手机端 click事件有延迟，所以使用tab事件来代替(tab事件时自己写的，并不是浏览器提供的)

7. touch事件的原理:
   - touchStart 时记录当前手指的位置和时间点
   - touchEnd 时同样记录手指的位置和时间点
   
8. touch事件需要借助的一些插件
   - zepto.js
   - touch.js
   
9. 300ms引起的bug:tab 点透问题

10. tab 点透问题产生的场景:
   - 有2个元素，一上一下
   - 上面的元素做tab事件，下面的元素做click事件
   - 上面的元素tab事件之后隐藏自己

11. 解决点透问题
   - 上下都是tab事件
   - 延迟处理，上面的元素延迟300ms之后再隐藏
   - 隐藏上面的元素之后，立马在整个页面覆盖一层透明的遮罩层，300ms之后再将这个遮罩层给删掉

12. 做touch端的规范
   - 全使用 zepto.js
   - 使用 jquery + touch.js
   - 使用 zepto + touch.js
   
13.css类库
  
   