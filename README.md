# Oddity Gentoo overlay

[Oddity](https://github.com/LaT-SKY/Oddity) 的 Gentoo overlay. 当前提供二进制包 `games-util/oddity-bin`.

## 添加 overlay

```bash
eselect repository add oddity git https://github.com/LaT-SKY/oddity-overlay.git
emerge --sync oddity
```

## 安装

```bash
emerge games-util/oddity-bin
```

游戏运行需要 `umu-launcher` 和 Proton. `umu-launcher` 在 GURU overlay 中:

```bash
eselect repository enable guru
emerge --sync guru
emerge games-util/umu-launcher
```

Proton 仍需由用户准备, 并在 Oddity 设置中选择 Proton 目录.

## 版本

Overlay 只保留最新的 `oddity-bin` ebuild. 新版本由 Oddity 主仓库的 release workflow 自动推送.

## QA

`pkgcheck` 会在 push 和 pull request 时运行.
