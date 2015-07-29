# Motion

- order: 1
- nodemos: true

---

Ant Design 提供了一些预设的组件动画展现和缓动函数。

<div id="components-motion-demo-basic"></div>

## 组件动画

通过设置组件的 `transitionName` 指定组件动画。

| 组件         | 中文名              | 采用动画                                        |
|--------------|---------------------|-------------------------------------------------|
| popover      | 气泡浮出层          | `zoom-up` `zoom-down` `zoom-left` `zoom-right`  |
| popconfirm   | 气泡确认框          | `zoom-up` `zoom-down` `zoom-left` `zoom-right`  |
| tooltip      | 文字提示框          | `zoom-up` `zoom-down` `zoom-left` `zoom-right`  |
| modal        | 弹出框              | `zoom`                                          |
| confirm      | 弹出确认框          | `zoom`                                          |
| message      | 信息提示条          | `move-up`                                       |
| dropdown     | 下拉菜单            | `slide-up`                                      |
| select       | 选择框              | `slide-up`                                      |
| datepicker   | 日期选择框          | `slide-up`                                      |

## 缓动函数

在以上组件的动画不适合时，请用以下缓动。

|名称               |参数                                      |说明与适用                  |
|-------------------|------------------------------------------|---------------------------|
|@ease-out          | `cubic-bezier(0.215, 0.61, 0.355, 1);`   |默认后缓动；适合元素展开时；    |
|@ease-in           | `cubic-bezier(0.55, 0.055, 0.675, 0.19);`|默认前缓动；适合元素关闭时；    |
|@ease-in-out       | `cubic-bezier(0.645, 0.045, 0.355, 1);`  |默认前后缓动；适合元素移动；    |
|@ease-out-back     | `cubic-bezier(0.18, 0.89, 0.32, 1.28);`  |结束回动；适合弹出框出现时；    |
|@ease-in-back      | `cubic-bezier(0.6, -0.3, 0.74, 0.05);`   |开始回动；适合弹出框关闭；     |
|@ease-in-out-back  | `cubic-bezier(0.68, -0.55, 0.27, 1.55);` |前后回动；                   |
|@ease-out-circ     | `cubic-bezier(0.08, 0.82, 0.17, 1);`     |圆形后缓动；适合元素展开时；    |
|@ease-in-circ      | `cubic-bezier(0.6, 0.04, 0.98, 0.34);`   |圆形前缓动；适合元素关闭时；    |
|@ease-in-out-circ  | `cubic-bezier(0.78, 0.14, 0.15, 0.86);`  |圆形缓动；适合元素移动；       |


`````jsx
var cssAnimation = require('css-animation');
var motions = [];
motions = motions.concat([[{
  name: '淡入',
  value: 'fade',
  direction: 'enter',
  type: '渐隐'
}, {
  name: '淡出',
  value: 'fade',
  direction: 'leave',
  type: '渐隐'
}]]);
motions = motions.concat([[{
  name: '中心放大',
  value: 'zoom',
  direction: 'enter',
  type: '缩放'
}, {
  name: '中心缩小',
  value: 'zoom',
  direction: 'leave',
  type: '缩放'
}, {
  name: '上方放大',
  value: 'zoom-up',
  direction: 'enter',
  type: '缩放'
}, {
  name: '上方缩小',
  value: 'zoom-up',
  direction: 'leave',
  type: '缩放'
}, {
  name: '下方放大',
  value: 'zoom-down',
  direction: 'enter',
  type: '缩放'
}, {
  name: '下方缩小',
  value: 'zoom-down',
  direction: 'leave',
  type: '缩放'
}, {
  name: '左方放大',
  value: 'zoom-left',
  direction: 'enter',
  type: '缩放'
}, {
  name: '左方缩小',
  value: 'zoom-left',
  direction: 'leave',
  type: '缩放'
}, {
  name: '右方放大',
  value: 'zoom-right',
  direction: 'enter',
  type: '缩放'
}, {
  name: '右方缩小',
  value: 'zoom-right',
  direction: 'leave',
  type: '缩放'
}]]);
motions = motions.concat([[{
  name: '上方滑入',
  value: 'move-up',
  direction: 'enter',
  type: '移动'
}, {
  name: '上方滑出',
  value: 'move-up',
  direction: 'leave',
  type: '移动'
}, {
  name: '下方滑入',
  value: 'move-down',
  direction: 'enter',
  type: '移动'
}, {
  name: '下方滑出',
  value: 'move-down',
  direction: 'leave',
  type: '移动'
}, {
  name: '左方滑入',
  value: 'move-left',
  direction: 'enter',
  type: '移动'
}, {
  name: '左方滑出',
  value: 'move-left',
  direction: 'leave',
  type: '移动'
}, {
  name: '右方滑入',
  value: 'move-right',
  direction: 'enter',
  type: '移动'
}, {
  name: '右方滑入',
  value: 'move-right',
  direction: 'leave',
  type: '移动'
}]]);
motions = motions.concat([[{
  name: '上方展开',
  value: 'slide-up',
  direction: 'enter',
  type: '伸缩'
}, {
  name: '上方缩回',
  value: 'slide-up',
  direction: 'leave',
  type: '伸缩'
}, {
  name: '下方展开',
  value: 'slide-down',
  direction: 'enter',
  type: '伸缩'
}, {
  name: '下方缩回',
  value: 'slide-down',
  direction: 'leave',
  type: '伸缩'
}, {
  name: '左方展开',
  value: 'slide-left',
  direction: 'enter',
  type: '伸缩'
}, {
  name: '左方缩回',
  value: 'slide-left',
  direction: 'leave',
  type: '伸缩'
}, {
  name: '右方展开',
  value: 'slide-right',
  direction: 'enter',
  type: '伸缩'
}, {
  name: '右方缩回',
  value: 'slide-right',
  direction: 'leave',
  type: '伸缩'
}]]);
motions = motions.concat([[{
  name: '摇摆',
  value: 'swing',
  direction: 'enter',
  type: '其他'
}]]);
var leave='-leave';
var Test = React.createClass({
  handleChange(e) {
    var value = e.target.value;
    if(value){
      this.demoNode.style.visibility='';
      cssAnimation(this.demoNode, value, () => {
        if(value.slice(-leave.length)===leave){
          this.demoNode.style.visibility='hidden';
        }
      });
    }
  },

  componentDidMount() {
    this.demoNode = React.findDOMNode(this.refs.demo);
  },

  render() {
    var options = [<option value="">请选择预设动画</option>].concat(motions.map(function (m) {
      var opts = m.map(function (m2) {
        return <option value={m2.value + "-" + m2.direction}>{m2.name + " " + m2.value}</option>
      });
      return <optgroup label={m[0].type}>{opts}</optgroup>;
    }));
    return <div>
      <div className="motion-container">
        <div ref="demo" className="motion-example">栗子</div>
      </div>
      <div className="motion-select">
        <select onChange={this.handleChange}>{options}</select>
      </div>
    </div>;
  }
});

React.render(<Test/>, document.getElementById('components-motion-demo-basic'));
`````

<style>
.motion-container {
  height: 150px;
  line-height: 150px;
  text-align: center;
  margin-bottom: 20px;
}
.motion-example {
  background: #4AAFDE;
  width: 140px;
  height: 140px;
  line-height: 140px;
  font-size: 18px;
  color: #fff;
  text-align: center;
  display: inline-block !important;
  border-radius: 8px;
  font-weight: bold;
}
.motion-select {
  text-align: center;
}
</style>
