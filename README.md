# My Project

全栈 Web 应用项目，采用 React + TypeScript 前端、NestJS 后端、PostgreSQL 数据库架构。

## 功能特性

- **前端**：React + TypeScript 构建现代化用户界面
- **后端**：NestJS 提供高性能 RESTful API
- **数据库**：PostgreSQL 企业级关系型数据库
- **类型安全**：全栈 TypeScript 开发，确保类型一致性
- **代码规范**：ESLint 配置统一代码风格
- **模块化架构**：清晰的目录结构，便于维护和扩展

## 快速开始

### 环境要求

- Node.js >= 18.x
- npm 或 yarn
- PostgreSQL >= 14

### 安装

```bash
# 克隆项目
git clone git@github.com:XL332058/my-project.git
cd my-project

# 安装依赖
npm install
```

### 配置

```bash
# 复制环境变量文件
cp .env.example .env

# 编辑 .env 文件，配置数据库连接等信息
```

### 运行

```bash
# 启动开发服务器
npm run start:dev

# 构建生产版本
npm run build

# 启动生产服务器
npm run start:prod
```

## 使用示例

### API 请求示例

```typescript
// 获取用户列表
const response = await fetch('/api/users');
const users = await response.json();

// 创建新用户
const newUser = await fetch('/api/users', {
  method: 'POST',
  headers: {
    'Content-Type': 'application/json',
  },
  body: JSON.stringify({
    name: '张三',
    email: 'zhangsan@example.com',
  }),
});
```

### React 组件示例

```tsx
import React from 'react';

interface UserProps {
  name: string;
  email: string;
}

const UserCard: React.FC<UserProps> = ({ name, email }) => {
  return (
    <div className="user-card">
      <h3>{name}</h3>
      <p>{email}</p>
    </div>
  );
};

export default UserCard;
```

## 配置说明

### 环境变量

| 变量名 | 说明 | 默认值 |
|--------|------|--------|
| `DATABASE_URL` | PostgreSQL 连接字符串 | - |
| `PORT` | 服务器端口 | 3000 |
| `NODE_ENV` | 运行环境 | development |
| `JWT_SECRET` | JWT 密钥 | - |

### 项目结构

```
my-project/
├── src/                    # 源代码目录
│   ├── client/            # React 前端代码
│   ├── server/            # NestJS 后端代码
│   └── shared/            # 前后端共享代码
├── public/                # 静态资源
├── tests/                 # 测试文件
├── .env.example           # 环境变量示例
├── .eslintrc.js           # ESLint 配置
├── tsconfig.json          # TypeScript 配置
└── package.json           # 项目依赖
```

## 贡献指南

### 开发规范

- 使用 2 空格缩进
- 变量名使用 camelCase
- 函数名使用动词开头（如 `getUserById`）
- 组件文件使用 PascalCase 命名
- API 路由使用 kebab-case
- 代码注释使用中文

### 提交规范

- 使用语义化的提交信息
- 每次提交只做最小必要的修改
- 修改代码前先阅读相关文件

### 开发流程

1. Fork 本仓库
2. 创建特性分支：`git checkout -b feature/amazing-feature`
3. 提交更改：`git commit -m 'feat: 添加某个功能'`
4. 推送到分支：`git push origin feature/amazing-feature`
5. 创建 Pull Request

## 许可证

MIT License

Copyright (c) 2024

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
