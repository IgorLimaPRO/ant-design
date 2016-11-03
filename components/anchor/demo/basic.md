---
order: 0
title:
  zh-CN: 基本
  en-US: Basic
---

## zh-CN

最简单的用法。

## en-US

The simplest usage.

```jsx
import { Anchor } from 'antd';
const { AnchorLink } = Anchor;

ReactDOM.render(
  <Anchor>
    <AnchorLink href="#components-anchor-demo-basic" title="基本" />
    <AnchorLink href="#components-anchor-demo-independ" title="独立使用" />
  </Anchor>
, mountNode);
```