- 浮动清除

- ```css
  /*设置伪元素,可以设置“全局”的浮动清除，比如设置所有浮动元素包含的类名中有clear选择器
  css部分代码*/
  clear:after{
      content: "";
      display: block;
      clear: both;
  }
  /*html部分代码*/
  <div class="father clear"></div>
  <div class="mather clear"></div>
  ```

- 字体行高

- ```css
  line-height: 20px;
  ```

- 文字阴影>属性顺序：水平距离   垂直距离   模糊度   阴影颜色

- ```css
  //镂空阴影
  text-shadow:0px 0px 5px black;
  //一个元素多个阴影设置》可叠加成3D效果：
  text-shadow:1px 1px 0px black,2px 2px 0px black,3px 3px 0px black,4px 4px 0px black,5px 5px 0px blue;
  ```

- 过渡动画

- ```css
  transition-property: width;//过渡的属性
  transition-property: width，color;//宽度和颜色都产生过渡动画
  transition-duration: 2s;//持续时间
  transition-duration: 2s,3s;//各属性过渡动画持续时间
  transition-timing-function: ease\ease-out\ease-in\linear\cubic-bezier(0.2,0.3,0.5,0.6);//运动曲线
  transittion-delay: 3s;//延迟时间
  //简写顺序：属性 持续时间 运动曲线
  transition: all 1s linear;
```
  
  