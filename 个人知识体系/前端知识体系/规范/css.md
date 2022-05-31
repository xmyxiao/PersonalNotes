# css 开发规范

+ 使用 BEM 命名规范
参考地址 [BEM规范](https://juejin.cn/post/6844903672162304013)

``` sass
  .back{ // 代表了更高级别的抽象或组件
    &__element{ // 代表 .block 的后代，用于形成一个完整的 .block 的整体
      &--modifier{ // 代表 .block 的不同状态或不同版本

      }
    }
  }
```

当需要明确关联性的模块关系时，应当使用 BEM 格式
