# hexo-theme-arknights (fork)

这里是原项目的分支，实现一些我个人博客需要的 feature。

原项目地址：[hexo-theme-arknights](https://github.com/Yue-plus/hexo-theme-arknights)

## 修改日志

不要直接使用，[InitializeGiscus.ts](https://github.com/weilycoder/hexo-theme-arknights/blob/main/source/js/_src/include/InitializeGiscus.ts) 中保存了我的 Giscus 配置，请修改/删除并**编译**后使用，否则我将可以操作你的评论。

若你没有 ts 编译条件，也可以直接修改/删除 [arknights.js(L722-L756)](https://github.com/weilycoder/hexo-theme-arknights/blob/main/source/js/arknights.js#L722-L756)。

修改日志一般按照同 feature 的最后一次提交标记，通常无交叉。

+ `1788c57`: 修改 404 页面；
+ `3c5be48`: 在侧栏增加 modified by；
+ `cec0793`: 使用 Giscus 作为评论系统；
+ `0107634`: 禁用鼠标动画；
+ `dd4698a`: 随博客主题更改 Giscus 主题；

以上修改也保存在 [Arknights Theme 修改日志](https://weilycoder.github.io/2025/03/30/theme-modify/)，有顺序差异。

+ `c12ffb5`: 在暗色模式下降低图片亮度；
+ `c968d52`: 修复侧边栏 `archives` 链接；
+ `bd806c3`: 在包含 `target` 标签时不应用 `Pjax`；
+ `7a2e20c`: 在侧边栏增加构建时间，可以在 `_config.yml` 中设置 `build_time`，也可以 `scripts` 文件夹下加入以下代码：
  ```js
  // scripts/update_build_time.js
  hexo.extend.filter.register('before_generate', function () {
    const now = new Date();
    const buildTime = now.toISOString();
    hexo.config.build_time = buildTime;
  });
  ```
+ `0b37af5`: 增加设置 `bin_paginator`，位于 `index_generator` 下；若启用，首页的跳转链接将维持在 $2$ 个，且保证可以在 $O(\log n)$ 次从一页跳到另一页。

## 许可证

原项目许可证采用 MIT 许可证，保留[链接](https://github.com/Yue-plus/hexo-theme-arknights/blob/main/LICENSE)。

我进行修改的部分继续采用 MIT 许可证，为此，我在本仓库的 LICENSE 文件上直接进行了修改以增加我的版权信息；如果这项行为不合适，请提醒我。
