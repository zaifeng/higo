## 说明

这是一个练习项目

主要用来测试`go install`命令如何使用

## Get 及复习到的知识

- 版本号要负责语义化版本要求

  - 主版本.次版本.修订版本
  - 版本号前要加 v

- git tag 相关命令

  - 新建 tag

  ```
      git tag -a v0.1.0 -C "first tag"
  ```

  - 推送至远程

  ```
      git push origin v0.1.0
      git push origin --tags
  ```

  - 删除 tag

  ```
      git tag -d v0.1.0 v0.2.0                // 删除本地
      git push origin --delete tag v0.1.0     // 删除远程
  ```

- 提交后的操作

  - 只增不删（也就是说，即便你删除远程分支，依然可以通过命令来安装,可能出于兼容性考虑）
  - `go install` 安装的是`tag`，不是`release`

- `git remote`调整命令
  - 直接修改
  ```
      git remote set-url origin git@github.com:user/repo.git
  ```
  - 删除后添加
  ```
      git remote rm origin
      git remote add origin git@github.com:user/repo.git
  ```
