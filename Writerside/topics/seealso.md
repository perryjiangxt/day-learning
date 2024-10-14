# seealso

## 示例

md文件中添加
```
<seealso>
       <category ref="related">
           <a href="Links.topic">Topic about links</a>
           <a href="Some_other.topic"/>
       </category>
       <category ref="external">
           <a href="https://www.google.com">Google</a>
           <a href="https://www.jetbrains.com"/>
       </category>
</seealso>

```

category ref值需要提前在c.list中定义
```
<!DOCTYPE categories SYSTEM "https://resources.jetbrains.com/writerside/1.0/categories.dtd">
<categories>
    <category id="related" name="Related topics" order="1"/>
    <category id="external" name="External resources" order="2"/>
</categories>
```