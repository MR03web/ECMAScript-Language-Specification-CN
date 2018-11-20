# 4.1 Web Scripting Web脚本语言

A web browser provides an ECMAScript host environment for client-side computation including, for instance, objects that represent windows, menus, pop-ups, dialog boxes, text areas, anchors, frames, history, cookies, and input/output. Further, the host environment provides a means to attach scripting code to events such as change of focus, page and image loading, unloading, error and abort, selection, form submission, and mouse actions. Scripting code appears within the HTML and the displayed page is a combination of user interface elements and fixed and computed text and images. The scripting code is reactive to user interaction, and there is no need for a main program.

web浏览器为客户端运算提供了一个宿主环境，例如：代表windows、menus、pop-ups、dialog boxes、text areas、anchors、frames、history、cookies和input/output的对象。提供连接脚本代码和诸如改变焦点、页面和图片的加载、卸载、错误和放弃，选择，表单提交和鼠标行为的方法。脚本代码出现在HTML中时，呈现出的页面是一个用户接口元素与固定和计
算出的文本和图片的集合。脚本代码直接响应用户的交互动作，而不需要一个主程序控制。

A web server provides a different host environment for server-side computation including objects representing requests, clients, and files; and mechanisms to lock and share data. By using browser-side and server-side scripting together, it is possible to distribute computation between the client and server while providing a customized user interface for a Web-based application.

web服务器为了服务端运算提供了一个完全不一样的宿主环境，包括的对象例如：requests、clients、files。以及数据锁定和分享的机制。通过浏览器端脚本及服务端脚本的配合使用，在为基于web方式的应用程序提供定制的用户接口，可以将计算分散到客户端和服务端进行。

Each Web browser and server that supports ECMAScript supplies its own host environment, completing the ECMAScript execution environment.

每一种支持ECMAScript的web浏览器和服务器都将它们自身的宿主环境作为ECMAScript的补充，以此使ECMAScript的执行环境变得完整。
