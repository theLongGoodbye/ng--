# ng--官网最后一遍

2018-10-29————2019-2-11，耗时三个多月，终于把官网完整的过了一遍

接下来再过最后一遍，然后就再看一遍《ng 权威指南》 + 做一遍ng-zorro 的实战项目

***
生成内联模板
`ng generate component hero -it`

***
**属性（Property，方括号包裹着的）** 和  **元素属性（Attribute）** 的区别在于，Attribute 只是用于初始化，而 Property 是绑定值，会随着数据源的变化而变化，也就是实时更新
> 这句话值得再强调一次： 模板绑定是通过 property 和事件来工作的，而不是 attribute。

> 方括号告诉 Angular 要计算模板表达式。 如果忘了加方括号，Angular 会把这个表达式当做字符串常量看待，并用该字符串来初始化目标属性。 它不会计算这个字符串。

不要出现这样的失误：
`<app-hero-detail hero="currentHero"></app-hero-detail>`

***
#### 四种控制样式的常用模板语法：
```
<div [class.special]="!isSpecial">This one is not so special</div>

<button [style.color]="isSpecial ? 'red': 'green'">Red</button>   
<button [style.font-size.em]="isSpecial ? 3 : 1" >Big</button>

下面两个用到再看吧，跟上面差不多，区别是控制可以多个样式
[NgClass]
[ngStyle]
```

***
在使用 ngModel 指令进行双向数据绑定之前，你必须导入 FormsModule 并把它添加到 NgModule 的 imports 列表中。

***
ngIf 指令通常会用来防范空指针错误。

***
回车键及失焦事件： <input (keyup.enter)="onEnter(box.value)"  (blur)="update(box.value)">

***
#### 内容投影： 
```
<after-content>
   <app-child></app-child>
 </after-content>`
 
  <div>-- projected content begins --</div>
    <ng-content></ng-content>
  <div>-- projected content ends --</div>
```



