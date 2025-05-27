# Shinny Linux Kernel Patches

用于维护 Linux 内核的补丁集。

## 编译说明

- 要求编译时携带 `LOCALVERSION`
  - 版本号为当前 Git 仓库的对应版本短 commit ID（commit ID 前 7 位）
  - 编译命令：`make -j$(nproc) LOCALVERSION="-$(git rev-parse --short=7 master)" bindeb-pkg`
- 要求编译时禁用 `CONFIG_BQL`
  - ref: https://shinnytech.atlassian.net/wiki/spaces/BACK/pages/2059665636/vpn
