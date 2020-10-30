相同点：

- `<script>` 标签必须有 `src` 属性，不能是内联脚本；
- 文件的加载是异步的；
- 脚本中不能调用 `document.write()`。

不同点：

- `defer` 在 HTML 4 中定义，`async` 在 HTML 5 中定义；
- `defer` 使脚本在 HTML 解析完且触发 `DOMContentLoaded` 事件之前按照声明顺序执行，`async` 则是加载完立即执行。
