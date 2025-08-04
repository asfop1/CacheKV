# 更新日志

本文档记录了CacheKV的所有重要更改。

格式基于 [Keep a Changelog](https://keepachangelog.com/zh-CN/1.0.0/)，
版本号遵循 [语义化版本](https://semver.org/lang/zh-CN/)。

## [1.0.0] - 2024-08-04

### 🎉 首次发布

#### ✨ 新增功能
- **自动回填缓存**: 实现"若无则从数据源获取并回填缓存"核心模式
- **批量操作优化**: 高性能批量获取和设置，避免N+1查询问题
- **热点键自动续期**: 自动检测并延长热点数据的缓存时间
- **统计功能**: 完整的命中率统计、热点键检测、性能监控
- **分层配置系统**: 支持全局、组级、键级配置继承
- **统一键管理**: 标准化键生成、环境隔离、版本管理

#### 🏗️ 核心架构
- **CacheKV**: 核心缓存操作类
- **CacheKVFactory**: 工厂类，负责组件初始化
- **KeyManager**: 键管理器，统一键的创建和验证
- **ConfigManager**: 配置管理器，支持分层配置
- **KeyStats**: 统计管理，记录性能指标
- **RedisDriver**: Redis驱动，支持批量操作

#### 🚀 辅助函数
- `cache_kv_get()`: 单个缓存获取
- `cache_kv_get_multiple()`: 批量缓存获取
- `cache_kv_get_stats()`: 获取统计信息
- `cache_kv_get_hot_keys()`: 获取热点键列表

#### 📚 文档
- **完整文档**: 配置、架构、使用指南
- **快速开始**: 5分钟上手指南
- **配置参考**: 所有配置选项详解
- **统计功能**: 性能监控和热点键管理
- **API参考**: 完整的类和方法文档

#### 💡 技术特性
- **PHP 7.0+** 兼容
- **Redis** 批量操作优化
- **零配置** 开箱即用
- **热点数据** 自动续期
- **实时** 性能监控
- **环境隔离** 支持

#### 🏆 适用场景
- Web应用缓存
- API服务缓存
- 电商平台缓存
- 内容管理缓存
- 数据分析缓存
- 微服务架构缓存

### 📋 系统要求
- PHP >= 7.0
- ext-redis 扩展

### 📦 安装
```bash
composer require asfop1/cache-kv
```

### 🔗 链接
- [GitHub仓库](https://github.com/asfop1/CacheKV)
- [Packagist包](https://packagist.org/packages/asfop1/cache-kv)
- [问题反馈](https://github.com/asfop1/CacheKV/issues)
