# DSH 旋律启动器 v0.5.4

本版本继续修复启动阶段 Profile 读取失败的问题。

## What's Changed

- 在 `profile:read` 和 Profile 路径构造入口增加运行时类型校验，避免旧数据中的数组直接传入 `path.join()`。
- 启动器读取设置时会把旧的路径数组、非法 Profile 名称和启动参数修复后持久化，后续启动不再反复触发同一错误。
- 对 Profile 清单中的非法插件条目进行过滤，避免损坏的 `dsh.profile.bundles` 阻塞 Profile 加载。
- 当仍存在无法修复的设置时，错误信息会明确指出是 DSH_HOME 还是 Profile 名称异常，并给出重新选择入口。
- 增加 IPC、Profile 清单和设置迁移测试。

**Full Changelog**: https://github.com/rirko/dsh-melody-launcher/compare/v0.5.3...v0.5.4
