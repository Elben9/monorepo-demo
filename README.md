# monorepo-demo

通过pnpm create vite创建普通Ts项目

通过 npm init vue@3 快速搭建vue3项目

通过pnpm-workspace.yaml配置工作区的package

公共项目通过index.ts入口文件暴露所有导出的内容，在package.json中设置main: index.ts 设置name（后续package中需要用name找到对应的公共部分）

在package项目中通过pnpm add @elben/apis （或其他pkg name） 来导入公共组件或Ts

packages/h5-client 使用了公共Ts方法和公共Vue组件作为测试

pnpm run dev --filter <name> 来运行packages中的任意项目
