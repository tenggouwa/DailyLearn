## InnerText NodeValue TextContent的区别
+ NodeValue 
  + 会输出一个数组
  + 里面代表了内容
+ InnerText
  + 输出可展示文本内容
  + display:none不展示
  + innerText和innerHtml是经过文本解析后展现的 所以会忽略对应的不需要被展示的内容
+ TextContent
  + 输出所有文本 包括样式
  + 不显示缩进信息