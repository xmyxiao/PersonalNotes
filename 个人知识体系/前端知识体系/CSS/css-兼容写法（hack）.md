**css-兼容写法（hack）**</br>
```css
.sofish{ 
	padding:10px; 
	padding:9px\9; /* all ie */ 
	padding:8px\0; /* ie8-9 */ 
	*padding:5px; /* ie6-7 */ 
	+padding:7px; /* ie7 */ 
	_padding:6px; /* ie6 */ 
}
<!--[if IE]>IE only<![endif]--> 
<!--[if !IE]>NOT IE<![endif]-->
```
　　一般使用单独的hack写法,这样在某个低版本浏览器淘汰时可以直接搜索关键字删除hack,易于维护