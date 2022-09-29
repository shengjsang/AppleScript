`AppleScript`中如何像其他语言一样使用循环来遍历，并且每次都能通过下标来获取当前遍历的值是什么，从而对当前的值进行操作



下面通过代码示例来进行演示

+ 通过循环遍历List中是否含有5这个值
+ 有的换就打印包含，并打印下标，循环退出
+ 如果不包含，则打印不包含，并继续查找

```typescript
set myValues to {1, 2, 3, 4, 5, 6, 7}
repeat with i from 1 to count myValues
	if 5 contains item i of myValues then
		display dialog "Contain 5 and item is " & i & "."
		exit repeat
	else
		display dialog "Do not contain."
	end if
end repeat
```