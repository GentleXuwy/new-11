# ajax

1. **Ajax介绍**

   “Asynchronous JavaScript and XML”(异步JavaScript和XML)的缩写）是一组Web开发技术，它使用客户端上的各种Web技术来创建异步web应用程序.使用Ajax，Web应用程序可以异步（在后台）从服务器发送和检索数据，而不会干扰现有页面的显示和行为。通过将数据交换层与表示层分离，Ajax 允许网页以及扩展的 Web 应用程序动态更改内容，而无需重新加载整个页面。在实践中，现代实现通常使用JSON而不是XML。

   Ajax不是一种技术，而是一个编程概念。HTML 和 CSS 可以组合使用来标记和设置信息样式。JavaScript 可以修改网页以动态显示，并允许用户与新信息进行交互。内置的 XMLHttpRequest 对象用于在网页上执行 Ajax，允许网站将内容加载到屏幕上而无需刷新页面。Ajax不是一种新技术，也不是一种新语言。相反，它是以新方式使用的现有技术。

   后来，AJAX 这个词就成为 JavaScript 脚本发起 HTTP 通信的代名词，也就是说，只要用脚本发起通信，就可以叫做 AJAX 通信。W3C 也在2006年发布了它的国际标准.

2. **技术实现**

   - 用于演示的HTML（或 XHTML）和 CSS
   - 文档对象模型（DOM），用于动态显示数据并与之交互
   - 用于数据交换的 JSON 或 XML，以及用于 XML 操作的 XSLT
   - 用于异步通信的XMLHttpRequest对象
   - 将这些技术结合在一起的JavaScript

3. **能力**

   - 无刷新更改网页内容
   - 无刷新翻页
   - 在页面加载后从服务器请求数据
   - 在后台向服务器发送数据
   - 使用js自动提交表单
   - 使用js上传文件
   - 等等...

# es6 promise

1. **介绍**

   promise 是ES6引入的进行异步编程新的解决方案，从语法上来说它就是个构造函数，从功能上来说，promise对象用来封装异步的任务，并且可以对结果进行处理。promise的最大好处在于支持链式操作并可以解决回调地狱的问题，且它在指定回调和错误处理这块更加灵活与方便。

    Promise是[Es6](https://so.csdn.net/so/search?q=Es6&spm=1001.2101.3001.7020)新增的构造器，用来提优化异步代码的写法，Promise中文意为承诺，承诺它一段时间后返回给你最终的结果。

2. **promise的基本工作流程**

   首先要通过 new promise() 创建一个对象，在 promise 内部封装异步操作，如果异步操作成功则调用 resolve() 函数，resolve一调则将 promise 的状态该为成功即 fullfilled。成功在调 then 方法时，调用的是第一个参数，即第一个回调函数中的代码，让它返回一个新的 promise 对象。then 方法的返回对象也是一个新的 promise 对象。 如果 promise 对象的操作失败了，则调 reject() 将状态设置为失败，调用reject 时，失败之后将调用 then 方法当中的第二个回调函数，并且返回一个 promise

3. **三个状态**

   - 待定（pending）: 初始状态，既没有被兑现，也没有被拒绝。
   - 已兑现（fulfilled）: 意味着操作成功完成。
   - 已拒绝（rejected）: 意味着操作失败。