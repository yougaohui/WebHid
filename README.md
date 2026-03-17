# WebHID 最小 Demo

阶段 1 前期验证用：在浏览器中完成一次 **requestDevice → open → sendReport → 接收 Report** 的完整流程。

## 浏览器要求

- **推荐**：Chrome 或 Edge（支持 WebHID）。
- **安全限制**：页面必须在 **HTTPS** 或 **localhost** 下打开，否则 `navigator.hid` 不可用。

## 如何运行

1. 在项目根目录或本目录下启动一个本地 HTTP 服务（避免直接用 `file://` 打开，部分环境下 WebHID 会受限）。
2. 用 Chrome/Edge 打开该服务下的 `demo/index.html`。

示例（在项目根目录 `mouse-web` 下执行）：

```bash
npx serve demo
```

然后在浏览器访问：`http://localhost:3000`（或终端提示的地址），进入 `index.html` 页面。

或只服务当前目录：

```bash
cd demo && npx serve .
```

## 使用步骤

1. 点击 **「选择设备」**：弹出系统 HID 设备选择框，选择目标鼠标（或接收器）。
2. 设备连接成功后，点击 **「发送 Report」**：发送一条测试 Report（reportId=0，8 字节测试数据）。
3. 若设备有响应，会通过 `inputreport` 事件在页面下方日志中自动显示收到的 Report（reportId、长度、十六进制数据）。

## 产出与验收

- 验收标准：在 Chrome 下能选择设备、打开、发送一条 Report、收到一条 Report 并展示在页面。
- 设备 filters 与 `doc/阶段产出与参考/阶段1-前期验证/设备清单与filters配置.md` 一致，实机验证后填写 `doc/阶段产出与参考/阶段1-前期验证/WebHID验证报告.md`。
