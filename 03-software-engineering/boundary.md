# 工程边界 / Engineering Boundary

## 一句话理解 / One-line Summary

工程中的边界决定开发是否能成功、是否能交付、是否能长期维护。  
Engineering boundaries decide whether development can succeed, be delivered, and remain maintainable.

## 核心观点 / Core Idea

很多软件项目失败，不一定是因为不会写代码，而是因为边界没切清楚。

常见边界：

- 需求边界 / Requirement Boundary
- 领域边界 / Domain Boundary
- 交付边界 / Delivery Boundary
- 完成度边界 / Definition of Done
- 责任边界 / Responsibility Boundary
- 技术边界 / Technical Boundary

## 例子 / Example

模糊需求：

> 做一个权限系统。

更清晰的边界：

> 第一版只支持后台用户的角色权限，不支持字段级权限，不支持多租户，不支持外部 OAuth，只需要满足管理员、运营、财务三个角色的菜单和接口访问控制。

## 判断模板 / Thinking Template

```text
1. 这件事属于哪个模块？
2. 它不属于哪个模块？
3. 当前版本必须交付什么？
4. 哪些可以后置？
5. 怎样算完成？
6. 谁负责验证？
```

## 我的理解 / My Understanding

把模糊的想法，切成有边界、可验证、可交付的结构，是软件工程的核心能力之一。
