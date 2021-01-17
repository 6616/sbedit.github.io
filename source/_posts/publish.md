---
title: 开始部署
date: 2021-01-17 09:03:09
categories: 
- [一级分类A,子分类A2]
- [一级分类B]

tags: 
- 标签A
- 设置

---
## 生成token

## 部署到vercel

### 一键部署

### 设置忽略版本

git diff --quiet HEAD^ HEAD publish.md

## 部署到netlify

### 一键部署

## 部署到github pages

### 仓库名

https://sbedit.github.io

### 建立文件`.travis.yml`

> 内容

```
sudo: false
language: node_js
node_js:
  - 10 # use nodejs v10 LTS
cache: npm
branches:
  only:
    - master # build master branch only
script:
  - hexo generate # generate static files
deploy:
  provider: pages
  skip-cleanup: true
  github-token: $GH_TOKEN
  keep-history: true
  on:
    branch: master
  local-dir: public
```

### 注册并登陆https://travis-ci.com/dashboard

#### 允许读取所有仓库

#### 设置token

```
GH_TOKEN  内容等于个人token
```
