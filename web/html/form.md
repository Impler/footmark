# 表单相关知识点汇总
## 1 表单提交方式与参数传递
```html
<form action="a/b?c=c1">
	<input type='text' name="d" value="d1"/>
</form>
```
形如上面的表单，如果采用Post提交方式，请求中的参数为[c:c1, d:d1]，但如果是Get方式提交，请求中仅会包含[d:d1]。因为Get提交会把表单元素拼接起来，然后接在 form action 后面，form action 中`?`后面的参数将会被忽略。  