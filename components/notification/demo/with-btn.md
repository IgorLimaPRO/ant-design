# 自定义关闭按钮

- order: 3

自定义关闭按钮的样式和文字。

---

````jsx
var Notification = require('antd/lib/notification');

if(!Notification.notification){
  Notification.notification = Notification.newInstance({
    prefixCls: 'ant-notification',
    style: {
      top: 0,
      right: 0
    }
  });
}

var btn = <button className="ant-btn ant-btn-primary ant-btn-sm">自定义关闭按钮</button>;

var openNotification = function() {
  var args = {
    message: "这是标题",
    description: "这是提示框的文案这是提示框示框的文案这是提示是提示框的文案这是提示框的文案",
    btn: btn
  }; 
  Notification.show(args);
}

React.render(
  <div>
    <button className="ant-btn ant-btn-primary" onClick={openNotification}>自定义关闭按钮</button>
  </div>,
document.getElementById('components-notification-demo-with-btn'));
````