提取短信验证码中的数字在AppleScript中有多种方法，今后会持续更新，方法从简单到难，当然也各有优缺点，和针对性。



# 第一种方法：暴力法

顾名思义就是真的很暴力，但是限制就是字符是死的，不能够变通。

下面用代码示例解释：

+ 比如我要对这一段手机验证码进行提取处理：`您 Apple ID 的验证码为：556954"`

```
set AppleScript's text item delimiters to "验证码为："
```

只需要将验证码前面的内容设置为分割的标志，然后内容就会被分割成几个部分
如果说验证码后面还有其他文本干扰，我们可以对分割后的内容进行二次分割

```typescript
set verifyContents to "您 Apple ID 的验证码为：556954"
set AppleScript's text item delimiters to "验证码为："
text items of verifyContents
display dialog item 2 of text items of verifyContents
set AppleScript's text item delimiters to "验证码为："
```

![在这里插入图片描述](https://raw.githubusercontent.com/shengjsang/PicS/master/20225c74afa4f81b47a287980463486c6d96.png)

![在这里插入图片描述](https://raw.githubusercontent.com/shengjsang/PicS/master/2022dd444c84f65c4623a21a6e5a33304375.png)
