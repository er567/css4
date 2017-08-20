### css4 

1. [:not]() 

        E:not(s1, s2, ...) {}

> 在css3中仅能匹配一个选择器,css4中可以匹配多个 

> 仅支持safari

2. [:matches]() 

        E:matches(s1, s2) {}
        E:-webkit-any(s1, s2, ...) {}
        E:-moz-any(s1, s2, ...) {} 

> 意义与:not()相反,匹配对应选择器

> 支持大部分主流浏览器,不支持ie和Edge(win10内置浏览器)

3. [:has]() 

        E:has(rs1, rs2, ...) 

> 包含伪类选择器,匹配选择器

> 暂时没有浏览器支持

4. [E:[foo="bar" i]]()

        E:[foo="bar" i]{}

> 属性选择器,忽略大小写

> 不支持ie,Edge和Chrome for Mobile

5. [:dir](http://css4-selectors.com/selector/css4/dir-pseudo-class/)

        E:dir(ltr/rtl){}

> 根据文本方向匹配,从左到右或者从右到左 

> 仅支持Firefox

6. [:lang]()

        E:lang(*-CA) {}

> 在css2中就被添加,css4中新增了通配符

> 暂时木有浏览器支持 

7. [:any-link]()

        E:any-link {}
        E:-webkit-any-link {}
        E:-moz-any-link {}

> 超链接伪类选择器,只要a有href就能匹配

> 支持大部分主流浏览器,不支持ie和Edge 

8. [:scope]() 

        E:scope() {} 

> 样式范围伪类选择器,style scope的父元素以内的范围

> 持大部分主流浏览器,不支持ie和Edge 

9. [:current / :past / :future]() 

        E:current(s1, s2, ...) {}
        E:past(s1, s2, ...) {}
        E:future(s1, s2, ...) {}

> 匹配当前,过去和未来的伪类选择器,类似歌词/字幕

> 暂时没有浏览器支持 

10. [:drop]()

        E:drop(active || valid || invalid) {}

> 匹配被拖动元素覆盖的元素(状态) 

> 暂时没有浏览器支持 

11. [:indeterminate]() 

        :indeterminate {} 

> 匹配不确定的元素,如Checkbox & radio button

> 支持所有主流浏览器

12. [:default]()

        E:default {}

> 匹配默认元素的伪类选择器,一组相近的ui元素中默认的,form表单的第一个按钮

> 不支持ie和Edge浏览器 

13. [Validity](http://css4-selectors.com/selector/css4/range-pseudo-class/)

        E:valid {}

        E:invalid {}

> 匹配input&form元素有效还是无效 

> 兼容所有主流浏览器

14. [Range]()(demo)

        E:in-range {}

        E:out-of-range {} 

> 匹配input的值是否在规定范围区间

> 兼容主流浏览器,除了ie

15. [Optionality]()可选性

        E:required {}
        E:optional {}

> 可选性伪类选择器,匹配表单内input是否必选

> 兼容所有主流浏览器 

16. [:user-error]()

        E:user-error {}

> 必须在:invalid, :out-of-range, or empty :required 中有一个才能使用,当用户与元素有了交互才能生效 

> 不兼容所有浏览器. 

18. [:read-only / :read-write]()

        E:read-only {}
        E:read-write {}

> 前者匹配不能编辑的元素比如p,span,h1,h2..;后者匹配可编辑元素 

> 不支持ie和Safari for mobile,Opera for mobile 

19. [Placeholder-Shown]()

        E:placeholder-shown { /* Style properties */ }
        E::-webkit-input-placeholder { /* Chrome, Safari, Opera */ }
        E::-moz-placeholder { /* Firefox */ }
        E:-ms-input-placeholder { /* IE */ } 

> 匹配有占位字符的输入框,给占位字符设置样式

> 兼容所有主流浏览器 

20. [:blank]()

        E:blank {} 
        E:-moz-only-whitespace { /* Firefox */ }

> 与css3中的:empty类似,区别是:empty中不能有元素,:blank中可以有;匹配空格,换行符,tab

> 仅支持火狐,需兼容写法

21. [Grid-Structural](http://css4-selectors.com/selector/css4/grid-structural-pseudo-class/)

        E:column(selector) {}
        E:nth-column(an + b) {}
        E:nth-last-column(an + b) {} 

> 匹配对应列的所有元素,:nth-last-column是从后往前数

> 暂不支持所有浏览器