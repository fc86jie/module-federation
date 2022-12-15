# module-federation

## 使用方法

使用以下步骤运行，由于 vite 是按需编译，所以 app2 必须先打包启动，无法 2 个 App 同时是开发模式

```bash
pnpm run build:app2
pnpm run preview:app2
```

新建一个终端

```bash
pnpm run dev:app1
```

Both `app1` and `app2` are independently deployed apps:

- `app1`: http://localhost:3001
- `app2`: http://localhost:3002

### 引入 app1 中的远程组件样式丢失？

app2 中的 vite.config.ts 配置项 build.cssCodeSplit 设置为 false
