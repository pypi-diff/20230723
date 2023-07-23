# Comparing `tmp/topgrade-12.0.0.tar.gz` & `tmp/topgrade-12.0.1.tar.gz`

## Comparing `topgrade-12.0.0.tar` & `topgrade-12.0.1.tar`

### file list

```diff
@@ -1,102 +1,110 @@
--rw-r--r--   0        0        0     2128 1970-01-01 00:00:00.000000 topgrade-12.0.0/Cargo.toml
--rw-r--r--   0     1001      123     1503 2023-06-28 02:43:57.000000 topgrade-12.0.0/.github/ISSUE_TEMPLATE/bug_report.md
--rw-r--r--   0     1001      123      182 2023-06-28 02:43:57.000000 topgrade-12.0.0/.github/ISSUE_TEMPLATE/config.yml
--rw-r--r--   0     1001      123      580 2023-06-28 02:43:57.000000 topgrade-12.0.0/.github/ISSUE_TEMPLATE/feature_request.md
--rw-r--r--   0     1001      123      512 2023-06-28 02:43:57.000000 topgrade-12.0.0/.github/PULL_REQUEST_TEMPLATE.md
--rw-r--r--   0     1001      123     2275 2023-06-28 02:43:57.000000 topgrade-12.0.0/.github/workflows/release_pypi.yaml
--rw-r--r--   0     1001      123       27 2023-06-28 02:43:57.000000 topgrade-12.0.0/.gitignore
--rw-r--r--   0     1001      123      167 2023-06-28 02:43:57.000000 topgrade-12.0.0/.idea/vcs.xml
--rw-r--r--   0     1001      123     6290 2023-06-28 02:43:57.000000 topgrade-12.0.0/.idea/workspace.xml
--rw-r--r--   0     1001      123     1040 2023-06-28 02:43:57.000000 topgrade-12.0.0/.vscode/launch.json
--rw-r--r--   0     1001      123      187 2023-06-28 02:43:57.000000 topgrade-12.0.0/.vscode/tasks.json
--rw-r--r--   0     1001      123     1401 2023-06-28 02:43:57.000000 topgrade-12.0.0/.vscode/topgrade.code-snippets
--rw-r--r--   0     1001      123     5226 2023-06-28 02:43:57.000000 topgrade-12.0.0/CODE_OF_CONDUCT.md
--rw-r--r--   0     1001      123     4218 2023-06-28 02:43:57.000000 topgrade-12.0.0/CONTRIBUTING.md
--rw-r--r--   0     1001      123    71148 2023-06-28 02:43:57.000000 topgrade-12.0.0/Cargo.lock
--rw-r--r--   0     1001      123    35149 2023-06-28 02:43:57.000000 topgrade-12.0.0/LICENSE
--rw-r--r--   0     1001      123     4795 2023-06-28 02:43:57.000000 topgrade-12.0.0/README.md
--rw-r--r--   0     1001      123      242 2023-06-28 02:43:57.000000 topgrade-12.0.0/SECURITY.md
--rwxr-xr-x   0     1001      123     2640 2023-06-28 02:43:57.000000 topgrade-12.0.0/build-all.sh
--rw-r--r--   0     1001      123       91 2023-06-28 02:43:57.000000 topgrade-12.0.0/build.rs
--rw-r--r--   0     1001      123      280 2023-06-28 02:43:57.000000 topgrade-12.0.0/clippy.toml
--rw-r--r--   0     1001      123     4174 2023-06-28 02:43:57.000000 topgrade-12.0.0/config.example.toml
--rw-r--r--   0     1001      123       10 2023-06-28 02:44:08.000000 topgrade-12.0.0/dist/topgrade-12.0.0.tar.gz
--rw-r--r--   0     1001      123    16603 2023-06-28 02:43:57.000000 topgrade-12.0.0/doc/topgrade.afdesign
--rw-r--r--   0     1001      123    31029 2023-06-28 02:43:57.000000 topgrade-12.0.0/doc/topgrade.png
--rw-r--r--   0     1001      123    35141 2023-06-28 02:43:57.000000 topgrade-12.0.0/doc/topgrade_transparent.png
--rw-r--r--   0     1001      123      348 2023-06-28 02:43:57.000000 topgrade-12.0.0/pyproject.toml
--rw-r--r--   0     1001      123       16 2023-06-28 02:43:57.000000 topgrade-12.0.0/rustfmt.toml
--rw-r--r--   0     1001      123     9299 2023-06-28 02:43:57.000000 topgrade-12.0.0/src/command.rs
--rw-r--r--   0     1001      123    44719 2023-06-28 02:43:57.000000 topgrade-12.0.0/src/config.rs
--rw-r--r--   0     1001      123      566 2023-06-28 02:43:57.000000 topgrade-12.0.0/src/ctrlc/interrupted.rs
--rw-r--r--   0     1001      123      200 2023-06-28 02:43:57.000000 topgrade-12.0.0/src/ctrlc/mod.rs
--rw-r--r--   0     1001      123      572 2023-06-28 02:43:57.000000 topgrade-12.0.0/src/ctrlc/unix.rs
--rw-r--r--   0     1001      123      578 2023-06-28 02:43:57.000000 topgrade-12.0.0/src/ctrlc/windows.rs
--rw-r--r--   0     1001      123      871 2023-06-28 02:43:57.000000 topgrade-12.0.0/src/error.rs
--rw-r--r--   0     1001      123     1653 2023-06-28 02:43:57.000000 topgrade-12.0.0/src/execution_context.rs
--rw-r--r--   0     1001      123     7171 2023-06-28 02:43:57.000000 topgrade-12.0.0/src/executor.rs
--rw-r--r--   0     1001      123       34 2023-06-28 02:43:57.000000 topgrade-12.0.0/src/lib.rs
--rw-r--r--   0     1001      123    22717 2023-06-28 02:43:57.000000 topgrade-12.0.0/src/main.rs
--rw-r--r--   0     1001      123      993 2023-06-28 02:43:57.000000 topgrade-12.0.0/src/report.rs
--rw-r--r--   0     1001      123     2755 2023-06-28 02:43:57.000000 topgrade-12.0.0/src/runner.rs
--rw-r--r--   0     1001      123     1178 2023-06-28 02:43:57.000000 topgrade-12.0.0/src/self_renamer.rs
--rw-r--r--   0     1001      123     1723 2023-06-28 02:43:57.000000 topgrade-12.0.0/src/self_update.rs
--rw-r--r--   0     1001      123        0 2023-06-28 02:43:57.000000 topgrade-12.0.0/src/steps/bun.rs
--rw-r--r--   0     1001      123     6141 2023-06-28 02:43:57.000000 topgrade-12.0.0/src/steps/containers.rs
--rw-r--r--   0     1001      123      341 2023-06-28 02:43:57.000000 topgrade-12.0.0/src/steps/emacs.el
--rw-r--r--   0     1001      123     2854 2023-06-28 02:43:57.000000 topgrade-12.0.0/src/steps/emacs.rs
--rw-r--r--   0     1001      123    24323 2023-06-28 02:43:57.000000 topgrade-12.0.0/src/steps/generic.rs
--rw-r--r--   0     1001      123     9975 2023-06-28 02:43:57.000000 topgrade-12.0.0/src/steps/git.rs
--rw-r--r--   0     1001      123     1513 2023-06-28 02:43:57.000000 topgrade-12.0.0/src/steps/go.rs
--rw-r--r--   0     1001      123      541 2023-06-28 02:43:57.000000 topgrade-12.0.0/src/steps/kakoune.rs
--rw-r--r--   0     1001      123      288 2023-06-28 02:43:57.000000 topgrade-12.0.0/src/steps/mod.rs
--rw-r--r--   0     1001      123     7868 2023-06-28 02:43:57.000000 topgrade-12.0.0/src/steps/node.rs
--rw-r--r--   0     1001      123     1027 2023-06-28 02:43:57.000000 topgrade-12.0.0/src/steps/os/android.rs
--rw-r--r--   0     1001      123    10400 2023-06-28 02:43:57.000000 topgrade-12.0.0/src/steps/os/archlinux.rs
--rw-r--r--   0     1001      123      793 2023-06-28 02:43:57.000000 topgrade-12.0.0/src/steps/os/dragonfly.rs
--rw-r--r--   0     1001      123     1220 2023-06-28 02:43:57.000000 topgrade-12.0.0/src/steps/os/freebsd.rs
--rw-r--r--   0     1001      123    30202 2023-06-28 02:43:57.000000 topgrade-12.0.0/src/steps/os/linux.rs
--rw-r--r--   0     1001      123     2788 2023-06-28 02:43:57.000000 topgrade-12.0.0/src/steps/os/macos.rs
--rw-r--r--   0     1001      123      473 2023-06-28 02:43:57.000000 topgrade-12.0.0/src/steps/os/mod.rs
--rw-r--r--   0     1001      123      788 2023-06-28 02:43:57.000000 topgrade-12.0.0/src/steps/os/openbsd.rs
--rw-r--r--   0     1001      123      211 2023-06-28 02:43:57.000000 topgrade-12.0.0/src/steps/os/os_release/amazon_linux
--rw-r--r--   0     1001      123      258 2023-06-28 02:43:57.000000 topgrade-12.0.0/src/steps/os/os_release/arch
--rw-r--r--   0     1001      123      311 2023-06-28 02:43:57.000000 topgrade-12.0.0/src/steps/os/os_release/arch32
--rw-r--r--   0     1001      123      284 2023-06-28 02:43:57.000000 topgrade-12.0.0/src/steps/os/os_release/artix
--rw-r--r--   0     1001      123      393 2023-06-28 02:43:57.000000 topgrade-12.0.0/src/steps/os/os_release/centos
--rw-r--r--   0     1001      123      307 2023-06-28 02:43:57.000000 topgrade-12.0.0/src/steps/os/os_release/clearlinux
--rw-r--r--   0     1001      123      267 2023-06-28 02:43:57.000000 topgrade-12.0.0/src/steps/os/os_release/debian
--rw-r--r--   0     1001      123      186 2023-06-28 02:43:57.000000 topgrade-12.0.0/src/steps/os/os_release/deepin
--rw-r--r--   0     1001      123      199 2023-06-28 02:43:57.000000 topgrade-12.0.0/src/steps/os/os_release/exherbo
--rw-r--r--   0     1001      123      769 2023-06-28 02:43:57.000000 topgrade-12.0.0/src/steps/os/os_release/fedora
--rwxr-xr-x   0     1001      123      580 2023-06-28 02:43:57.000000 topgrade-12.0.0/src/steps/os/os_release/fedoraremixforwsl
--rw-r--r--   0     1001      123      307 2023-06-28 02:43:57.000000 topgrade-12.0.0/src/steps/os/os_release/garuda
--rw-r--r--   0     1001      123      190 2023-06-28 02:43:57.000000 topgrade-12.0.0/src/steps/os/os_release/gentoo
--rw-r--r--   0     1001      123      209 2023-06-28 02:43:57.000000 topgrade-12.0.0/src/steps/os/os_release/manjaro
--rw-r--r--   0     1001      123      170 2023-06-28 02:43:57.000000 topgrade-12.0.0/src/steps/os/os_release/manjaro-arm
--rw-r--r--   0     1001      123      308 2023-06-28 02:43:57.000000 topgrade-12.0.0/src/steps/os/os_release/mint
--rw-r--r--   0     1001      123      410 2023-06-28 02:43:57.000000 topgrade-12.0.0/src/steps/os/os_release/nixos
--rw-r--r--   0     1001      123      275 2023-06-28 02:43:57.000000 topgrade-12.0.0/src/steps/os/os_release/opensuse
--rw-r--r--   0     1001      123      451 2023-06-28 02:43:57.000000 topgrade-12.0.0/src/steps/os/os_release/oracle
--rw-r--r--   0     1001      123      204 2023-06-28 02:43:57.000000 topgrade-12.0.0/src/steps/os/os_release/pclinuxos
--rwxr-xr-x   0     1001      123      355 2023-06-28 02:43:57.000000 topgrade-12.0.0/src/steps/os/os_release/pengwinonwsl
--rw-r--r--   0     1001      123       85 2023-06-28 02:43:57.000000 topgrade-12.0.0/src/steps/os/os_release/pureos
--rw-r--r--   0     1001      123      501 2023-06-28 02:43:57.000000 topgrade-12.0.0/src/steps/os/os_release/rhel
--rw-r--r--   0     1001      123      398 2023-06-28 02:43:57.000000 topgrade-12.0.0/src/steps/os/os_release/ubuntu
--rw-r--r--   0     1001      123      384 2023-06-28 02:43:57.000000 topgrade-12.0.0/src/steps/os/os_release/vanilla
--rw-r--r--   0     1001      123    16415 2023-06-28 02:43:57.000000 topgrade-12.0.0/src/steps/os/unix.rs
--rw-r--r--   0     1001      123     5469 2023-06-28 02:43:57.000000 topgrade-12.0.0/src/steps/os/windows.rs
--rw-r--r--   0     1001      123     3712 2023-06-28 02:43:57.000000 topgrade-12.0.0/src/steps/powershell.rs
--rw-r--r--   0     1001      123       32 2023-06-28 02:43:57.000000 topgrade-12.0.0/src/steps/remote/mod.rs
--rw-r--r--   0     1001      123     1981 2023-06-28 02:43:57.000000 topgrade-12.0.0/src/steps/remote/ssh.rs
--rw-r--r--   0     1001      123     6718 2023-06-28 02:43:57.000000 topgrade-12.0.0/src/steps/remote/vagrant.rs
--rw-r--r--   0     1001      123     5892 2023-06-28 02:43:57.000000 topgrade-12.0.0/src/steps/tmux.rs
--rw-r--r--   0     1001      123     1886 2023-06-28 02:43:57.000000 topgrade-12.0.0/src/steps/toolbx.rs
--rw-r--r--   0     1001      123       70 2023-06-28 02:43:57.000000 topgrade-12.0.0/src/steps/upgrade.kak
--rw-r--r--   0     1001      123      954 2023-06-28 02:43:57.000000 topgrade-12.0.0/src/steps/upgrade.vim
--rw-r--r--   0     1001      123     3972 2023-06-28 02:43:57.000000 topgrade-12.0.0/src/steps/vim.rs
--rw-r--r--   0     1001      123     6090 2023-06-28 02:43:57.000000 topgrade-12.0.0/src/steps/zsh.rs
--rw-r--r--   0     1001      123     4068 2023-06-28 02:43:57.000000 topgrade-12.0.0/src/sudo.rs
--rw-r--r--   0     1001      123     9572 2023-06-28 02:43:57.000000 topgrade-12.0.0/src/terminal.rs
--rw-r--r--   0     1001      123     8062 2023-06-28 02:43:57.000000 topgrade-12.0.0/src/utils.rs
--rw-r--r--   0        0        0     5477 1970-01-01 00:00:00.000000 topgrade-12.0.0/PKG-INFO
+-rw-r--r--   0        0        0     2128 1970-01-01 00:00:00.000000 topgrade-12.0.1/Cargo.toml
+-rw-r--r--   0     1001      123     1503 2023-07-23 12:09:10.000000 topgrade-12.0.1/.github/ISSUE_TEMPLATE/bug_report.md
+-rw-r--r--   0     1001      123      182 2023-07-23 12:09:10.000000 topgrade-12.0.1/.github/ISSUE_TEMPLATE/config.yml
+-rw-r--r--   0     1001      123      580 2023-07-23 12:09:10.000000 topgrade-12.0.1/.github/ISSUE_TEMPLATE/feature_request.md
+-rw-r--r--   0     1001      123      512 2023-07-23 12:09:10.000000 topgrade-12.0.1/.github/PULL_REQUEST_TEMPLATE.md
+-rw-r--r--   0     1001      123     2337 2023-07-23 12:09:10.000000 topgrade-12.0.1/.github/workflows/check-and-lint.yaml
+-rw-r--r--   0     1001      123      758 2023-07-23 12:09:10.000000 topgrade-12.0.1/.github/workflows/check-semver.yml
+-rw-r--r--   0     1001      123     1903 2023-07-23 12:09:10.000000 topgrade-12.0.1/.github/workflows/code-coverage.yml
+-rw-r--r--   0     1001      123      656 2023-07-23 12:09:10.000000 topgrade-12.0.1/.github/workflows/crates-publish.yml
+-rw-r--r--   0     1001      123     2132 2023-07-23 12:09:10.000000 topgrade-12.0.1/.github/workflows/release-cross.yml
+-rw-r--r--   0     1001      123     2297 2023-07-23 12:09:10.000000 topgrade-12.0.1/.github/workflows/release.yml
+-rw-r--r--   0     1001      123      419 2023-07-23 12:09:10.000000 topgrade-12.0.1/.github/workflows/test-config-creation.yml
+-rw-r--r--   0     1001      123      498 2023-07-23 12:09:10.000000 topgrade-12.0.1/.github/workflows/update_aur.yml
+-rw-r--r--   0     1001      123     1083 2023-07-23 12:09:10.000000 topgrade-12.0.1/.github/workflows/update_homebrew.yml
+-rw-r--r--   0     1001      123     2261 2023-07-23 12:09:10.000000 topgrade-12.0.1/.github/workflows/update_pypi.yml
+-rw-r--r--   0     1001      123       27 2023-07-23 12:09:10.000000 topgrade-12.0.1/.gitignore
+-rw-r--r--   0     1001      123     1040 2023-07-23 12:09:10.000000 topgrade-12.0.1/.vscode/launch.json
+-rw-r--r--   0     1001      123      187 2023-07-23 12:09:10.000000 topgrade-12.0.1/.vscode/tasks.json
+-rw-r--r--   0     1001      123     1401 2023-07-23 12:09:10.000000 topgrade-12.0.1/.vscode/topgrade.code-snippets
+-rw-r--r--   0     1001      123     5226 2023-07-23 12:09:10.000000 topgrade-12.0.1/CODE_OF_CONDUCT.md
+-rw-r--r--   0     1001      123     4344 2023-07-23 12:09:10.000000 topgrade-12.0.1/CONTRIBUTING.md
+-rw-r--r--   0     1001      123    71180 2023-07-23 12:09:10.000000 topgrade-12.0.1/Cargo.lock
+-rw-r--r--   0     1001      123    35149 2023-07-23 12:09:10.000000 topgrade-12.0.1/LICENSE
+-rw-r--r--   0     1001      123     4918 2023-07-23 12:09:10.000000 topgrade-12.0.1/README.md
+-rw-r--r--   0     1001      123      242 2023-07-23 12:09:10.000000 topgrade-12.0.1/SECURITY.md
+-rwxr-xr-x   0     1001      123     2640 2023-07-23 12:09:10.000000 topgrade-12.0.1/build-all.sh
+-rw-r--r--   0     1001      123       91 2023-07-23 12:09:10.000000 topgrade-12.0.1/build.rs
+-rw-r--r--   0     1001      123      280 2023-07-23 12:09:10.000000 topgrade-12.0.1/clippy.toml
+-rw-r--r--   0     1001      123     4635 2023-07-23 12:09:10.000000 topgrade-12.0.1/config.example.toml
+-rw-r--r--   0     1001      123       10 2023-07-23 12:09:22.000000 topgrade-12.0.1/dist/topgrade-12.0.1.tar.gz
+-rw-r--r--   0     1001      123    16603 2023-07-23 12:09:10.000000 topgrade-12.0.1/doc/topgrade.afdesign
+-rw-r--r--   0     1001      123    31029 2023-07-23 12:09:10.000000 topgrade-12.0.1/doc/topgrade.png
+-rw-r--r--   0     1001      123    35141 2023-07-23 12:09:10.000000 topgrade-12.0.1/doc/topgrade_transparent.png
+-rw-r--r--   0     1001      123      348 2023-07-23 12:09:10.000000 topgrade-12.0.1/pyproject.toml
+-rw-r--r--   0     1001      123       16 2023-07-23 12:09:10.000000 topgrade-12.0.1/rustfmt.toml
+-rw-r--r--   0     1001      123     9299 2023-07-23 12:09:10.000000 topgrade-12.0.1/src/command.rs
+-rw-r--r--   0     1001      123    44755 2023-07-23 12:09:10.000000 topgrade-12.0.1/src/config.rs
+-rw-r--r--   0     1001      123      566 2023-07-23 12:09:10.000000 topgrade-12.0.1/src/ctrlc/interrupted.rs
+-rw-r--r--   0     1001      123      200 2023-07-23 12:09:10.000000 topgrade-12.0.1/src/ctrlc/mod.rs
+-rw-r--r--   0     1001      123      572 2023-07-23 12:09:10.000000 topgrade-12.0.1/src/ctrlc/unix.rs
+-rw-r--r--   0     1001      123      578 2023-07-23 12:09:10.000000 topgrade-12.0.1/src/ctrlc/windows.rs
+-rw-r--r--   0     1001      123      871 2023-07-23 12:09:10.000000 topgrade-12.0.1/src/error.rs
+-rw-r--r--   0     1001      123     1908 2023-07-23 12:09:10.000000 topgrade-12.0.1/src/execution_context.rs
+-rw-r--r--   0     1001      123     7171 2023-07-23 12:09:10.000000 topgrade-12.0.1/src/executor.rs
+-rw-r--r--   0     1001      123       34 2023-07-23 12:09:10.000000 topgrade-12.0.1/src/lib.rs
+-rw-r--r--   0     1001      123    22717 2023-07-23 12:09:10.000000 topgrade-12.0.1/src/main.rs
+-rw-r--r--   0     1001      123      993 2023-07-23 12:09:10.000000 topgrade-12.0.1/src/report.rs
+-rw-r--r--   0     1001      123     2755 2023-07-23 12:09:10.000000 topgrade-12.0.1/src/runner.rs
+-rw-r--r--   0     1001      123     1178 2023-07-23 12:09:10.000000 topgrade-12.0.1/src/self_renamer.rs
+-rw-r--r--   0     1001      123     1723 2023-07-23 12:09:10.000000 topgrade-12.0.1/src/self_update.rs
+-rw-r--r--   0     1001      123        0 2023-07-23 12:09:10.000000 topgrade-12.0.1/src/steps/bun.rs
+-rw-r--r--   0     1001      123     6141 2023-07-23 12:09:10.000000 topgrade-12.0.1/src/steps/containers.rs
+-rw-r--r--   0     1001      123      341 2023-07-23 12:09:10.000000 topgrade-12.0.1/src/steps/emacs.el
+-rw-r--r--   0     1001      123     2849 2023-07-23 12:09:10.000000 topgrade-12.0.1/src/steps/emacs.rs
+-rw-r--r--   0     1001      123    24466 2023-07-23 12:09:10.000000 topgrade-12.0.1/src/steps/generic.rs
+-rw-r--r--   0     1001      123     9975 2023-07-23 12:09:10.000000 topgrade-12.0.1/src/steps/git.rs
+-rw-r--r--   0     1001      123     1513 2023-07-23 12:09:10.000000 topgrade-12.0.1/src/steps/go.rs
+-rw-r--r--   0     1001      123      541 2023-07-23 12:09:10.000000 topgrade-12.0.1/src/steps/kakoune.rs
+-rw-r--r--   0     1001      123      288 2023-07-23 12:09:10.000000 topgrade-12.0.1/src/steps/mod.rs
+-rw-r--r--   0     1001      123     7868 2023-07-23 12:09:10.000000 topgrade-12.0.1/src/steps/node.rs
+-rw-r--r--   0     1001      123     1027 2023-07-23 12:09:10.000000 topgrade-12.0.1/src/steps/os/android.rs
+-rw-r--r--   0     1001      123    10400 2023-07-23 12:09:10.000000 topgrade-12.0.1/src/steps/os/archlinux.rs
+-rw-r--r--   0     1001      123      862 2023-07-23 12:09:10.000000 topgrade-12.0.1/src/steps/os/dragonfly.rs
+-rw-r--r--   0     1001      123     1220 2023-07-23 12:09:10.000000 topgrade-12.0.1/src/steps/os/freebsd.rs
+-rw-r--r--   0     1001      123    31120 2023-07-23 12:09:10.000000 topgrade-12.0.1/src/steps/os/linux.rs
+-rw-r--r--   0     1001      123     2788 2023-07-23 12:09:10.000000 topgrade-12.0.1/src/steps/os/macos.rs
+-rw-r--r--   0     1001      123      473 2023-07-23 12:09:10.000000 topgrade-12.0.1/src/steps/os/mod.rs
+-rw-r--r--   0     1001      123      788 2023-07-23 12:09:10.000000 topgrade-12.0.1/src/steps/os/openbsd.rs
+-rw-r--r--   0     1001      123      211 2023-07-23 12:09:10.000000 topgrade-12.0.1/src/steps/os/os_release/amazon_linux
+-rw-r--r--   0     1001      123      258 2023-07-23 12:09:10.000000 topgrade-12.0.1/src/steps/os/os_release/arch
+-rw-r--r--   0     1001      123      311 2023-07-23 12:09:10.000000 topgrade-12.0.1/src/steps/os/os_release/arch32
+-rw-r--r--   0     1001      123      284 2023-07-23 12:09:10.000000 topgrade-12.0.1/src/steps/os/os_release/artix
+-rw-r--r--   0     1001      123      393 2023-07-23 12:09:10.000000 topgrade-12.0.1/src/steps/os/os_release/centos
+-rw-r--r--   0     1001      123      307 2023-07-23 12:09:10.000000 topgrade-12.0.1/src/steps/os/os_release/clearlinux
+-rw-r--r--   0     1001      123      267 2023-07-23 12:09:10.000000 topgrade-12.0.1/src/steps/os/os_release/debian
+-rw-r--r--   0     1001      123      186 2023-07-23 12:09:10.000000 topgrade-12.0.1/src/steps/os/os_release/deepin
+-rw-r--r--   0     1001      123      199 2023-07-23 12:09:10.000000 topgrade-12.0.1/src/steps/os/os_release/exherbo
+-rw-r--r--   0     1001      123      769 2023-07-23 12:09:10.000000 topgrade-12.0.1/src/steps/os/os_release/fedora
+-rwxr-xr-x   0     1001      123      580 2023-07-23 12:09:10.000000 topgrade-12.0.1/src/steps/os/os_release/fedoraremixforwsl
+-rw-r--r--   0     1001      123      307 2023-07-23 12:09:10.000000 topgrade-12.0.1/src/steps/os/os_release/garuda
+-rw-r--r--   0     1001      123      190 2023-07-23 12:09:10.000000 topgrade-12.0.1/src/steps/os/os_release/gentoo
+-rw-r--r--   0     1001      123      209 2023-07-23 12:09:10.000000 topgrade-12.0.1/src/steps/os/os_release/manjaro
+-rw-r--r--   0     1001      123      170 2023-07-23 12:09:10.000000 topgrade-12.0.1/src/steps/os/os_release/manjaro-arm
+-rw-r--r--   0     1001      123      308 2023-07-23 12:09:10.000000 topgrade-12.0.1/src/steps/os/os_release/mint
+-rw-r--r--   0     1001      123      410 2023-07-23 12:09:10.000000 topgrade-12.0.1/src/steps/os/os_release/nixos
+-rw-r--r--   0     1001      123      275 2023-07-23 12:09:10.000000 topgrade-12.0.1/src/steps/os/os_release/opensuse
+-rw-r--r--   0     1001      123      451 2023-07-23 12:09:10.000000 topgrade-12.0.1/src/steps/os/os_release/oracle
+-rw-r--r--   0     1001      123      204 2023-07-23 12:09:10.000000 topgrade-12.0.1/src/steps/os/os_release/pclinuxos
+-rwxr-xr-x   0     1001      123      355 2023-07-23 12:09:10.000000 topgrade-12.0.1/src/steps/os/os_release/pengwinonwsl
+-rw-r--r--   0     1001      123       85 2023-07-23 12:09:10.000000 topgrade-12.0.1/src/steps/os/os_release/pureos
+-rw-r--r--   0     1001      123      501 2023-07-23 12:09:10.000000 topgrade-12.0.1/src/steps/os/os_release/rhel
+-rw-r--r--   0     1001      123      306 2023-07-23 12:09:10.000000 topgrade-12.0.1/src/steps/os/os_release/solus
+-rw-r--r--   0     1001      123      398 2023-07-23 12:09:10.000000 topgrade-12.0.1/src/steps/os/os_release/ubuntu
+-rw-r--r--   0     1001      123      384 2023-07-23 12:09:10.000000 topgrade-12.0.1/src/steps/os/os_release/vanilla
+-rw-r--r--   0     1001      123    16411 2023-07-23 12:09:10.000000 topgrade-12.0.1/src/steps/os/unix.rs
+-rw-r--r--   0     1001      123     5469 2023-07-23 12:09:10.000000 topgrade-12.0.1/src/steps/os/windows.rs
+-rw-r--r--   0     1001      123     3712 2023-07-23 12:09:10.000000 topgrade-12.0.1/src/steps/powershell.rs
+-rw-r--r--   0     1001      123       32 2023-07-23 12:09:10.000000 topgrade-12.0.1/src/steps/remote/mod.rs
+-rw-r--r--   0     1001      123     1981 2023-07-23 12:09:10.000000 topgrade-12.0.1/src/steps/remote/ssh.rs
+-rw-r--r--   0     1001      123     6718 2023-07-23 12:09:10.000000 topgrade-12.0.1/src/steps/remote/vagrant.rs
+-rw-r--r--   0     1001      123     5892 2023-07-23 12:09:10.000000 topgrade-12.0.1/src/steps/tmux.rs
+-rw-r--r--   0     1001      123     1947 2023-07-23 12:09:10.000000 topgrade-12.0.1/src/steps/toolbx.rs
+-rw-r--r--   0     1001      123       70 2023-07-23 12:09:10.000000 topgrade-12.0.1/src/steps/upgrade.kak
+-rw-r--r--   0     1001      123      954 2023-07-23 12:09:10.000000 topgrade-12.0.1/src/steps/upgrade.vim
+-rw-r--r--   0     1001      123     3972 2023-07-23 12:09:10.000000 topgrade-12.0.1/src/steps/vim.rs
+-rw-r--r--   0     1001      123     7004 2023-07-23 12:09:10.000000 topgrade-12.0.1/src/steps/zsh.rs
+-rw-r--r--   0     1001      123     4068 2023-07-23 12:09:10.000000 topgrade-12.0.1/src/sudo.rs
+-rw-r--r--   0     1001      123     9572 2023-07-23 12:09:10.000000 topgrade-12.0.1/src/terminal.rs
+-rw-r--r--   0     1001      123     8062 2023-07-23 12:09:10.000000 topgrade-12.0.1/src/utils.rs
+-rw-r--r--   0        0        0     5600 1970-01-01 00:00:00.000000 topgrade-12.0.1/PKG-INFO
```

### Comparing `topgrade-12.0.0/Cargo.toml` & `topgrade-12.0.1/Cargo.toml`

 * *Files 4% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 [package]
 name = "topgrade"
 description = "Upgrade all the things"
 categories = ["os"]
 keywords = ["upgrade", "update"]
 license = "GPL-3.0"
 repository = "https://github.com/topgrade-rs/topgrade"
-version = "12.0.0"
+version = "12.0.1"
 authors = ["Roey Darwish Dror <roey.ghost@gmail.com>", "Thomas Schönauer <t.schoenauer@hgs-wt.at>"]
 exclude = ["doc/screenshot.gif"]
 edition = "2021"
 
 readme = "README.md"
 
 [[bin]]
@@ -33,15 +33,15 @@
 walkdir = "~2.3"
 console = "~0.15"
 lazy_static = "~1.4"
 chrono = "~0.4"
 glob = "~0.3"
 strum = { version = "~0.24", features = ["derive"] }
 thiserror = "~1.0"
-tempfile = "~3.2"
+tempfile = "~3.6"
 cfg-if = "~1.0"
 tokio = { version = "~1.18", features = ["process", "rt-multi-thread"] }
 futures = "~0.3"
 regex = "~1.7"
 semver = "~1.0"
 shell-words = "~1.1"
 color-eyre = "~0.6"
```

### Comparing `topgrade-12.0.0/.github/ISSUE_TEMPLATE/bug_report.md` & `topgrade-12.0.1/.github/ISSUE_TEMPLATE/bug_report.md`

 * *Files identical despite different names*

### Comparing `topgrade-12.0.0/.github/ISSUE_TEMPLATE/feature_request.md` & `topgrade-12.0.1/.github/ISSUE_TEMPLATE/feature_request.md`

 * *Files identical despite different names*

### Comparing `topgrade-12.0.0/.github/PULL_REQUEST_TEMPLATE.md` & `topgrade-12.0.1/.github/PULL_REQUEST_TEMPLATE.md`

 * *Files identical despite different names*

### Comparing `topgrade-12.0.0/.github/workflows/release_pypi.yaml` & `topgrade-12.0.1/.github/workflows/update_pypi.yml`

 * *Files 4% similar despite different names*

```diff
@@ -1,9 +1,8 @@
-# comment
-name: Publish to PyPi
+name: Update PyPi
 
 on:
   release:
     types: [published]
 
 permissions:
   contents: read
```

### Comparing `topgrade-12.0.0/.vscode/launch.json` & `topgrade-12.0.1/.vscode/launch.json`

 * *Files identical despite different names*

### Comparing `topgrade-12.0.0/.vscode/topgrade.code-snippets` & `topgrade-12.0.1/.vscode/topgrade.code-snippets`

 * *Files identical despite different names*

### Comparing `topgrade-12.0.0/CODE_OF_CONDUCT.md` & `topgrade-12.0.1/CODE_OF_CONDUCT.md`

 * *Files identical despite different names*

### Comparing `topgrade-12.0.0/CONTRIBUTING.md` & `topgrade-12.0.1/CONTRIBUTING.md`

 * *Files 13% similar despite different names*

```diff
@@ -1,20 +1,23 @@
 ## Contributing to `topgrade`
 
-Thank you for your interest in contributing to `topgrade`! We welcome and encourage
-contributions of all kinds, such as:
+Thank you for your interest in contributing to `topgrade`! 
+We welcome and encourage contributions of all kinds, such as:
 
 1. Issue reports or feature requests
 2. Documentation improvements
 3. Code (PR or PR Review)
 
+Please follow the [Karma Runner guidelines](http://karma-runner.github.io/6.2/dev/git-commit-msg.html)
+for commit messages.
+
 ## Adding a new `step`
 
-In `topgrade`'s term, package manager is called `step`. To add a new `step` to
-`topgrade`: 
+In `topgrade`'s term, package manager is called `step`.
+To add a new `step` to `topgrade`: 
 
 1. Add a new variant to 
    [`enum Step`](https://github.com/topgrade-rs/topgrade/blob/cb7adc8ced8a77addf2cb051d18bba9f202ab866/src/config.rs#L100)
 
    ```rust
    pub enum Step {
        // Existed steps
```

### Comparing `topgrade-12.0.0/Cargo.lock` & `topgrade-12.0.1/Cargo.lock`

 * *Files 1% similar despite different names*

```diff
@@ -620,15 +620,15 @@
 name = "filetime"
 version = "0.2.21"
 source = "registry+https://github.com/rust-lang/crates.io-index"
 checksum = "5cbc844cecaee9d4443931972e1289c8ff485cb4cc2767cb03ca139ed6885153"
 dependencies = [
  "cfg-if",
  "libc",
- "redox_syscall",
+ "redox_syscall 0.2.16",
  "windows-sys 0.48.0",
 ]
 
 [[package]]
 name = "flate2"
 version = "1.0.26"
 source = "registry+https://github.com/rust-lang/crates.io-index"
@@ -1492,21 +1492,30 @@
 source = "registry+https://github.com/rust-lang/crates.io-index"
 checksum = "fb5a58c1855b4b6819d59012155603f0b22ad30cad752600aadfcb695265519a"
 dependencies = [
  "bitflags",
 ]
 
 [[package]]
+name = "redox_syscall"
+version = "0.3.5"
+source = "registry+https://github.com/rust-lang/crates.io-index"
+checksum = "567664f262709473930a4bf9e51bf2ebf3348f2e748ccc50dea20646858f8f29"
+dependencies = [
+ "bitflags",
+]
+
+[[package]]
 name = "redox_users"
 version = "0.4.3"
 source = "registry+https://github.com/rust-lang/crates.io-index"
 checksum = "b033d837a7cf162d7993aded9304e30a83213c648b6e389db233191f891e5c2b"
 dependencies = [
  "getrandom",
- "redox_syscall",
+ "redox_syscall 0.2.16",
  "thiserror",
 ]
 
 [[package]]
 name = "regex"
 version = "1.7.3"
 source = "registry+https://github.com/rust-lang/crates.io-index"
@@ -1538,23 +1547,14 @@
 [[package]]
 name = "regex-syntax"
 version = "0.6.29"
 source = "registry+https://github.com/rust-lang/crates.io-index"
 checksum = "f162c6dd7b008981e4d40210aca20b4bd0f9b60ca9271061b07f78537722f2e1"
 
 [[package]]
-name = "remove_dir_all"
-version = "0.5.3"
-source = "registry+https://github.com/rust-lang/crates.io-index"
-checksum = "3acd125665422973a33ac9d3dd2df85edad0f4ae9b00dafb1a05e43a9f5ef8e7"
-dependencies = [
- "winapi",
-]
-
-[[package]]
 name = "reqwest"
 version = "0.11.18"
 source = "registry+https://github.com/rust-lang/crates.io-index"
 checksum = "cde824a14b7c14f85caff81225f411faacc04a2013f41670f41443742b1c1c55"
 dependencies = [
  "base64",
  "bytes",
@@ -1943,24 +1943,24 @@
 dependencies = [
  "quick-xml 0.23.1",
  "windows 0.39.0",
 ]
 
 [[package]]
 name = "tempfile"
-version = "3.2.0"
+version = "3.6.0"
 source = "registry+https://github.com/rust-lang/crates.io-index"
-checksum = "dac1c663cfc93810f88aed9b8941d48cabf856a1b111c29a40439018d870eb22"
+checksum = "31c0432476357e58790aaa47a8efb0c5138f137343f3b5f23bd36a27e3b0a6d6"
 dependencies = [
+ "autocfg",
  "cfg-if",
- "libc",
- "rand",
- "redox_syscall",
- "remove_dir_all",
- "winapi",
+ "fastrand",
+ "redox_syscall 0.3.5",
+ "rustix",
+ "windows-sys 0.48.0",
 ]
 
 [[package]]
 name = "termcolor"
 version = "1.2.0"
 source = "registry+https://github.com/rust-lang/crates.io-index"
 checksum = "be55cf8942feac5c765c2c993422806843c9a9a45d4d5c407ad6dd2ea95eb9b6"
@@ -2122,15 +2122,15 @@
  "indexmap",
  "toml_datetime",
  "winnow",
 ]
 
 [[package]]
 name = "topgrade"
-version = "12.0.0"
+version = "12.0.1"
 dependencies = [
  "cfg-if",
  "chrono",
  "clap",
  "clap_complete",
  "clap_mangen",
  "color-eyre",
```

### Comparing `topgrade-12.0.0/LICENSE` & `topgrade-12.0.1/LICENSE`

 * *Files identical despite different names*

### Comparing `topgrade-12.0.0/README.md` & `topgrade-12.0.1/README.md`

 * *Files 5% similar despite different names*

```diff
@@ -30,19 +30,21 @@
 [![Packaging status](https://repology.org/badge/vertical-allrepos/topgrade.svg)](https://repology.org/project/topgrade/versions)
 
 - Arch Linux: [AUR](https://aur.archlinux.org/packages/topgrade)
 - NixOS: [Nixpkgs](https://search.nixos.org/packages?show=topgrade)
 - Void Linux: [XBPS](https://voidlinux.org/packages/?arch=x86_64&q=topgrade)
 - macOS: [Homebrew](https://formulae.brew.sh/formula/topgrade) or [MacPorts](https://ports.macports.org/port/topgrade/)
 - Windows: [Scoop](https://github.com/ScoopInstaller/Main/blob/master/bucket/topgrade.json)
+- PyPi: [pip](https://pypi.org/project/topgrade/)
 
 Other systems users can either use `cargo install` or the compiled binaries from the release page.
 The compiled binaries contain a self-upgrading feature.
 
-Topgrade requires Rust 1.60 or above.
+> Currently, Topgrade requires Rust 1.65 or above. In general, Topgrade tracks 
+> the latest stable toolchain.
 
 ## Usage
 
 Just run `topgrade`.
 
 Visit the documentation at [topgrade-rs.github.io](https://topgrade-rs.github.io/) for more information.
```

#### html2text {}

```diff
@@ -12,36 +12,38 @@
 ## Installation [![Packaging status](https://repology.org/badge/vertical-
 allrepos/topgrade.svg)](https://repology.org/project/topgrade/versions) - Arch
 Linux: [AUR](https://aur.archlinux.org/packages/topgrade) - NixOS: [Nixpkgs]
 (https://search.nixos.org/packages?show=topgrade) - Void Linux: [XBPS](https://
 voidlinux.org/packages/?arch=x86_64&q=topgrade) - macOS: [Homebrew](https://
 formulae.brew.sh/formula/topgrade) or [MacPorts](https://ports.macports.org/
 port/topgrade/) - Windows: [Scoop](https://github.com/ScoopInstaller/Main/blob/
-master/bucket/topgrade.json) Other systems users can either use `cargo install`
-or the compiled binaries from the release page. The compiled binaries contain a
-self-upgrading feature. Topgrade requires Rust 1.60 or above. ## Usage Just run
-`topgrade`. Visit the documentation at [topgrade-rs.github.io](https://
-topgrade-rs.github.io/) for more information. > **Warning** > Work in Progress
-## Configuration See `config.example.toml` for an example configuration file.
-### Configuration Path #### `CONFIG_DIR` on each platform - **Windows**:
-`%APPDATA%` - **macOS** and **other Unix systems**: `${XDG_CONFIG_HOME:-
-~/.config}` `topgrade` will look for the configuration file in the following
-places, in order of priority: 1. `CONFIG_DIR/topgrade.toml` 2. `CONFIG_DIR/
-topgrade/topgrade.toml` If the file with higher priority is present, no matter
-it is valid or not, the other configuration files will be ignored. On the first
-run(no configuration file exists), `topgrade` will create a configuration file
-at `CONFIG_DIR/topgrade.toml` for you. ### Custom Commands Custom commands can
-be defined in the config file which can be run before, during, or after the
-inbuilt commands, as required. By default, the custom commands are run using a
-new shell according to the `$SHELL` environment variable on unix (falls back to
-`sh`) or `pwsh` on windows (falls back to `powershell`). On unix, if you want
-to run your command using an interactive shell, for example to source your
-shell's rc files, you can add `-i` at the start of your custom command. But
-note that this requires the command to exit the shell correctly or else the
-shell will hang indefinitely. ## Remote Execution You can specify a key called
+master/bucket/topgrade.json) - PyPi: [pip](https://pypi.org/project/topgrade/
+) Other systems users can either use `cargo install` or the compiled binaries
+from the release page. The compiled binaries contain a self-upgrading feature.
+> Currently, Topgrade requires Rust 1.65 or above. In general, Topgrade tracks
+> the latest stable toolchain. ## Usage Just run `topgrade`. Visit the
+documentation at [topgrade-rs.github.io](https://topgrade-rs.github.io/) for
+more information. > **Warning** > Work in Progress ## Configuration See
+`config.example.toml` for an example configuration file. ### Configuration Path
+#### `CONFIG_DIR` on each platform - **Windows**: `%APPDATA%` - **macOS** and
+**other Unix systems**: `${XDG_CONFIG_HOME:-~/.config}` `topgrade` will look
+for the configuration file in the following places, in order of priority: 1.
+`CONFIG_DIR/topgrade.toml` 2. `CONFIG_DIR/topgrade/topgrade.toml` If the file
+with higher priority is present, no matter it is valid or not, the other
+configuration files will be ignored. On the first run(no configuration file
+exists), `topgrade` will create a configuration file at `CONFIG_DIR/
+topgrade.toml` for you. ### Custom Commands Custom commands can be defined in
+the config file which can be run before, during, or after the inbuilt commands,
+as required. By default, the custom commands are run using a new shell
+according to the `$SHELL` environment variable on unix (falls back to `sh`) or
+`pwsh` on windows (falls back to `powershell`). On unix, if you want to run
+your command using an interactive shell, for example to source your shell's rc
+files, you can add `-i` at the start of your custom command. But note that this
+requires the command to exit the shell correctly or else the shell will hang
+indefinitely. ## Remote Execution You can specify a key called
 `remote_topgrades` in the configuration file. This key should contain a list of
 hostnames that have Topgrade installed on them. Topgrade will use `ssh` to run
 `topgrade` on remote hosts before acting locally. To limit the execution only
 to specific hosts use the `--remote-host-limit` parameter. ## Contribution ###
 Problems or missing features? Open a new issue describing your problem and if
 possible provide a solution. ### Missing a feature or found an unsupported
 tool/distro? Just let us now what you are missing by opening an issue. For
```

### Comparing `topgrade-12.0.0/build-all.sh` & `topgrade-12.0.1/build-all.sh`

 * *Files identical despite different names*

### Comparing `topgrade-12.0.0/config.example.toml` & `topgrade-12.0.1/config.example.toml`

 * *Files 14% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 # Include any additional configuration file(s)
 # [include] sections are processed in the order you write them
-# Files in $CONFIG_DIR/topgrade/topgrade.d/ are automatically included at the beginning of this file
+# Files in $CONFIG_DIR/topgrade.d/ are automatically included before this file
 [include]
 #paths = ["/etc/topgrade.toml"]
 
 [misc]
 # Don't ask for confirmations
 #assume_yes = true
 
@@ -19,25 +19,25 @@
 
 # Do not ask to retry failed steps (default: false)
 #no_retry = true
 
 # Sudo command to be used
 #sudo_command = "sudo"
 
-# Run `sudo -v` to cache credentials at the start of the run; this avoids a
-# blocking password prompt in the middle of a possibly-unattended run.
+# Run `sudo -v` to cache credentials at the start of the run
+# This avoids a blocking password prompt in the middle of an unattended run
 #pre_sudo = false
 
 # Run inside tmux
 #run_in_tmux = true
 
 # List of remote machines with Topgrade installed on them
 #remote_topgrades = ["toothless", "pi", "parnas"]
 
-# Arguments to pass SSH when upgrading remote systems
+# Arguments to pass to SSH when upgrading remote systems
 #ssh_arguments = "-o ConnectTimeout=2"
 
 # Path to Topgrade executable on remote machines
 #remote_topgrade_path = ".cargo/bin/topgrade"
 
 # Arguments to pass tmux when pulling Repositories
 #tmux_arguments = "-S /var/tmux.sock"
@@ -53,40 +53,36 @@
 
 # Skip sending a notification at the end of a run
 #skip_notify = true
 
 # Whether to self update (this is ignored if the binary has been built without self update support, available also via setting the environment variable TOPGRADE_NO_SELF_UPGRADE)
 #no_self_update = true
 
-[git]
-#max_concurrency = 5
-# Additional git repositories to pull
-#repos = [
-#    "~/src/*/",
-#    "~/.config/something"
-#]
-
-# Don't pull the predefined git repos
-#pull_predefined = false
-
-# Arguments to pass Git when pulling Repositories
-#arguments = "--rebase --autostash"
-
-[composer]
-#self_update = true
-
 # Commands to run before anything
 [pre_commands]
 #"Emacs Snapshot" = "rm -rf ~/.emacs.d/elpa.bak && cp -rl ~/.emacs.d/elpa ~/.emacs.d/elpa.bak"
 
+# Commands to run after anything
+[post_commands]
+#"Emacs Snapshot" = "rm -rf ~/.emacs.d/elpa.bak && cp -rl ~/.emacs.d/elpa ~/.emacs.d/elpa.bak"
+
 # Custom commands
 [commands]
 #"Python Environment" = "~/dev/.env/bin/pip install -i https://pypi.python.org/simple -U --upgrade-strategy eager jupyter"
 #"Custom command using interactive shell (unix)" = "-i vim_upgrade"
 
+[python]
+#enable_pip_review = true                         ###disabled by default
+#enable_pip_review_local = true                   ###disabled by default
+#enable_pipupgrade = true                         ###disabled by default
+#pipupgrade_arguments = "-y -u --pip-path pip"    ###disabled by default
+
+[composer]
+#self_update = true
+
 [brew]
 #greedy_cask = true
 #autoremove = true
 
 [linux]
 # Arch Package Manager to use. Allowed values: autodetect, aura, garuda_update, pacman, pamac, paru, pikaur, trizen, yay.
 #arch_package_manager = "pacman"
@@ -105,19 +101,27 @@
 #emerge_sync_flags = "-q"
 #emerge_update_flags = "-uDNa --with-bdeps=y world"
 #redhat_distro_sync = false
 #suse_dup = false
 #rpm_ostree = false
 #nix_arguments = "--flake"
 
-[python]
-#enable_pip_review = true                         ###disabled by default
-#enable_pip_review_local = true                   ###disabled by default
-#enable_pipupgrade = true                         ###disabled by default
-#pipupgrade_arguments = "-y -u --pip-path pip"    ###disabled by default
+[git]
+#max_concurrency = 5
+# Additional git repositories to pull
+#repos = [
+#    "~/src/*/",
+#    "~/.config/something"
+#]
+
+# Don't pull the predefined git repos
+#pull_predefined = false
+
+# Arguments to pass Git when pulling Repositories
+#arguments = "--rebase --autostash"
 
 [windows]
 # Manually select Windows updates
 #accept_all_updates = false
 #open_remotes_in_new_terminal = true
 #wsl_update_pre_release = true
 #wsl_update_use_web_download = true
@@ -127,18 +131,36 @@
 # manager such as Scoop or Cargo
 #self_rename = true
 
 [npm]
 # Use sudo if the NPM directory isn't owned by the current user
 #use_sudo = true
 
+[yarn]
+# Run `yarn global upgrade` with `sudo`
+#use_sudo = true
+
+[vim]
+# For `vim-plug`, execute `PlugUpdate!` instead of `PlugUpdate`
+#force_plug_update = true
+
 [firmware]
 # Offer to update firmware; if false just check for and display available updates
 #upgrade = true
 
+[vagrant]
+# Vagrant directories
+#directories = []
+
+# power on vagrant boxes if needed
+#power_on = true
+
+# Always suspend vagrant boxes instead of powering off
+#always_suspend = true
+
 [flatpak]
 # Use sudo for updating the system-wide installation
 #use_sudo = true
 
 [distrobox]
 #use_root = false
 #containers = ["archlinux-latest"]
```

### Comparing `topgrade-12.0.0/doc/topgrade.afdesign` & `topgrade-12.0.1/doc/topgrade.afdesign`

 * *Files identical despite different names*

### Comparing `topgrade-12.0.0/doc/topgrade.png` & `topgrade-12.0.1/doc/topgrade.png`

 * *Files identical despite different names*

### Comparing `topgrade-12.0.0/doc/topgrade_transparent.png` & `topgrade-12.0.1/doc/topgrade_transparent.png`

 * *Files identical despite different names*

### Comparing `topgrade-12.0.0/src/command.rs` & `topgrade-12.0.1/src/command.rs`

 * *Files identical despite different names*

### Comparing `topgrade-12.0.0/src/config.rs` & `topgrade-12.0.1/src/config.rs`

 * *Files 0% similar despite different names*

```diff
@@ -366,14 +366,16 @@
 }
 
 #[derive(Deserialize, Default, Debug, Merge)]
 #[serde(deny_unknown_fields)]
 pub struct Misc {
     pre_sudo: Option<bool>,
 
+    sudo_command: Option<SudoKind>,
+
     #[merge(strategy = crate::utils::merge_strategies::vec_prepend_opt)]
     git_repos: Option<Vec<String>>,
 
     predefined_git_repos: Option<bool>,
 
     #[merge(strategy = crate::utils::merge_strategies::vec_prepend_opt)]
     disable: Option<Vec<Step>>,
@@ -436,16 +438,14 @@
 pub struct ConfigFile {
     #[merge(strategy = crate::utils::merge_strategies::inner_merge_opt)]
     include: Option<Include>,
 
     #[merge(strategy = crate::utils::merge_strategies::inner_merge_opt)]
     misc: Option<Misc>,
 
-    sudo_command: Option<SudoKind>,
-
     #[merge(strategy = crate::utils::merge_strategies::commands_merge_opt)]
     pre_commands: Option<Commands>,
 
     #[merge(strategy = crate::utils::merge_strategies::commands_merge_opt)]
     post_commands: Option<Commands>,
 
     #[merge(strategy = crate::utils::merge_strategies::commands_merge_opt)]
@@ -1385,15 +1385,15 @@
             .windows
             .as_ref()
             .and_then(|windows| windows.open_remotes_in_new_terminal)
             .unwrap_or(false)
     }
 
     pub fn sudo_command(&self) -> Option<SudoKind> {
-        self.config_file.sudo_command
+        self.config_file.misc.as_ref().and_then(|misc| misc.sudo_command)
     }
 
     /// If `true`, `sudo` should be called after `pre_commands` in order to elevate at the
     /// start of the session (and not in the middle).
     pub fn pre_sudo(&self) -> bool {
         self.config_file
             .misc
```

### Comparing `topgrade-12.0.0/src/ctrlc/interrupted.rs` & `topgrade-12.0.1/src/ctrlc/interrupted.rs`

 * *Files identical despite different names*

### Comparing `topgrade-12.0.0/src/ctrlc/unix.rs` & `topgrade-12.0.1/src/ctrlc/unix.rs`

 * *Files identical despite different names*

### Comparing `topgrade-12.0.0/src/ctrlc/windows.rs` & `topgrade-12.0.1/src/ctrlc/windows.rs`

 * *Files identical despite different names*

### Comparing `topgrade-12.0.0/src/error.rs` & `topgrade-12.0.1/src/error.rs`

 * *Files identical despite different names*

### Comparing `topgrade-12.0.0/src/execution_context.rs` & `topgrade-12.0.1/src/execution_context.rs`

 * *Files 23% similar despite different names*

```diff
@@ -1,36 +1,41 @@
 #![allow(dead_code)]
 use crate::executor::RunType;
 use crate::git::Git;
 use crate::sudo::Sudo;
 use crate::utils::{require_option, REQUIRE_SUDO};
 use crate::{config::Config, executor::Executor};
 use color_eyre::eyre::Result;
+use std::env::var;
 use std::path::Path;
 use std::sync::Mutex;
 
 pub struct ExecutionContext<'a> {
     run_type: RunType,
     sudo: Option<Sudo>,
     git: &'a Git,
     config: &'a Config,
     /// Name of a tmux session to execute commands in, if any.
     /// This is used in `./steps/remote/ssh.rs`, where we want to run `topgrade` in a new
     /// tmux window for each remote.
     tmux_session: Mutex<Option<String>>,
+    /// True if topgrade is running under ssh.
+    under_ssh: bool,
 }
 
 impl<'a> ExecutionContext<'a> {
     pub fn new(run_type: RunType, sudo: Option<Sudo>, git: &'a Git, config: &'a Config) -> Self {
+        let under_ssh = var("SSH_CLIENT").is_ok() || var("SSH_TTY").is_ok();
         Self {
             run_type,
             sudo,
             git,
             config,
             tmux_session: Mutex::new(None),
+            under_ssh,
         }
     }
 
     pub fn execute_elevated(&self, command: &Path, interactive: bool) -> Result<Executor> {
         let sudo = require_option(self.sudo.as_ref(), REQUIRE_SUDO.to_string())?;
         Ok(sudo.execute_elevated(self, command, interactive))
     }
@@ -47,14 +52,18 @@
         &self.sudo
     }
 
     pub fn config(&self) -> &Config {
         self.config
     }
 
+    pub fn under_ssh(&self) -> bool {
+        self.under_ssh
+    }
+
     pub fn set_tmux_session(&self, session_name: String) {
         self.tmux_session.lock().unwrap().replace(session_name);
     }
 
     pub fn get_tmux_session(&self) -> Option<String> {
         self.tmux_session.lock().unwrap().clone()
     }
```

### Comparing `topgrade-12.0.0/src/executor.rs` & `topgrade-12.0.1/src/executor.rs`

 * *Files identical despite different names*

### Comparing `topgrade-12.0.0/src/main.rs` & `topgrade-12.0.1/src/main.rs`

 * *Files identical despite different names*

### Comparing `topgrade-12.0.0/src/report.rs` & `topgrade-12.0.1/src/report.rs`

 * *Files identical despite different names*

### Comparing `topgrade-12.0.0/src/runner.rs` & `topgrade-12.0.1/src/runner.rs`

 * *Files identical despite different names*

### Comparing `topgrade-12.0.0/src/self_renamer.rs` & `topgrade-12.0.1/src/self_renamer.rs`

 * *Files identical despite different names*

### Comparing `topgrade-12.0.0/src/self_update.rs` & `topgrade-12.0.1/src/self_update.rs`

 * *Files identical despite different names*

### Comparing `topgrade-12.0.0/src/steps/containers.rs` & `topgrade-12.0.1/src/steps/containers.rs`

 * *Files identical despite different names*

### Comparing `topgrade-12.0.0/src/steps/emacs.rs` & `topgrade-12.0.1/src/steps/emacs.rs`

 * *Files 3% similar despite different names*

```diff
@@ -1,8 +1,8 @@
-#[cfg(any(windows))]
+#[cfg(windows)]
 use std::env;
 use std::path::{Path, PathBuf};
 
 use color_eyre::eyre::Result;
 use etcetera::base_strategy::BaseStrategy;
 
 use crate::command::CommandExt;
```

### Comparing `topgrade-12.0.0/src/steps/generic.rs` & `topgrade-12.0.1/src/steps/generic.rs`

 * *Files 1% similar despite different names*

```diff
@@ -335,15 +335,15 @@
     if output.stdout.contains("False") {
         return Err(SkipStep("auto_activate_base is set to False".to_string()).into());
     }
 
     print_separator("Conda");
 
     let mut command = ctx.run_type().execute(conda);
-    command.args(["update", "--all"]);
+    command.args(["update", "--all", "-n", "base"]);
     if ctx.config().yes(Step::Conda) {
         command.arg("--yes");
     }
     command.status_checked()
 }
 
 pub fn run_mamba_update(ctx: &ExecutionContext) -> Result<()> {
@@ -356,15 +356,15 @@
     if output.stdout.contains("False") {
         return Err(SkipStep("auto_activate_base is set to False".to_string()).into());
     }
 
     print_separator("Mamba");
 
     let mut command = ctx.run_type().execute(mamba);
-    command.args(["update", "--all"]);
+    command.args(["update", "--all", "-n", "base"]);
     if ctx.config().yes(Step::Mamba) {
         command.arg("--yes");
     }
     command.status_checked()
 }
 
 pub fn run_pip3_update(ctx: &ExecutionContext) -> Result<()> {
@@ -716,15 +716,16 @@
     let bin = require("bin")?;
 
     print_separator("Bin");
     ctx.run_type().execute(bin).arg("update").status_checked()
 }
 
 pub fn spicetify_upgrade(ctx: &ExecutionContext) -> Result<()> {
-    let spicetify = require("spicetify")?;
+    // As of 04-07-2023 NixOS packages Spicetify with the `spicetify-cli` binary name
+    let spicetify = require("spicetify").or(require("spicetify-cli"))?;
 
     print_separator("Spicetify");
     ctx.run_type().execute(spicetify).arg("upgrade").status_checked()
 }
 
 pub fn run_ghcli_extensions_upgrade(ctx: &ExecutionContext) -> Result<()> {
     let gh = require("gh")?;
```

### Comparing `topgrade-12.0.0/src/steps/git.rs` & `topgrade-12.0.1/src/steps/git.rs`

 * *Files identical despite different names*

### Comparing `topgrade-12.0.0/src/steps/go.rs` & `topgrade-12.0.1/src/steps/go.rs`

 * *Files identical despite different names*

### Comparing `topgrade-12.0.0/src/steps/kakoune.rs` & `topgrade-12.0.1/src/steps/kakoune.rs`

 * *Files identical despite different names*

### Comparing `topgrade-12.0.0/src/steps/node.rs` & `topgrade-12.0.1/src/steps/node.rs`

 * *Files identical despite different names*

### Comparing `topgrade-12.0.0/src/steps/os/android.rs` & `topgrade-12.0.1/src/steps/os/android.rs`

 * *Files identical despite different names*

### Comparing `topgrade-12.0.0/src/steps/os/archlinux.rs` & `topgrade-12.0.1/src/steps/os/archlinux.rs`

 * *Files identical despite different names*

### Comparing `topgrade-12.0.0/src/steps/os/dragonfly.rs` & `topgrade-12.0.1/src/steps/os/dragonfly.rs`

 * *Files 9% similar despite different names*

```diff
@@ -6,14 +6,15 @@
 use std::process::Command;
 
 pub fn upgrade_packages(ctx: &ExecutionContext) -> Result<()> {
     let sudo = require_option(ctx.sudo().as_ref(), REQUIRE_SUDO.to_string())?;
     print_separator("DragonFly BSD Packages");
     ctx.execute(sudo)
         .args(["/usr/local/sbin/pkg", "upgrade"])
+        .arg(if ctx.config().yes(Step::System) { "-y" } else { "" })
         .status_checked()
 }
 
 pub fn audit_packages(ctx: &ExecutionContext) -> Result<()> {
     let sudo = require_option(ctx.sudo().as_ref(), REQUIRE_SUDO.to_string())?;
     println!();
     Command::new(sudo)
```

### Comparing `topgrade-12.0.0/src/steps/os/freebsd.rs` & `topgrade-12.0.1/src/steps/os/freebsd.rs`

 * *Files identical despite different names*

### Comparing `topgrade-12.0.0/src/steps/os/linux.rs` & `topgrade-12.0.1/src/steps/os/linux.rs`

 * *Files 5% similar despite different names*

```diff
@@ -252,14 +252,15 @@
         .execute(sudo)
         .arg("zypper")
         .arg(if ctx.config().suse_dup() {
             "dist-upgrade"
         } else {
             "update"
         })
+        .arg(if ctx.config().yes(Step::System) { "-y" } else { "" })
         .status_checked()?;
 
     Ok(())
 }
 
 fn upgrade_opensuse_tumbleweed(ctx: &ExecutionContext) -> Result<()> {
     let sudo = require_option(ctx.sudo().as_ref(), REQUIRE_SUDO.to_string())?;
@@ -268,24 +269,27 @@
         .args(["zypper", "refresh"])
         .status_checked()?;
 
     ctx.run_type()
         .execute(sudo)
         .arg("zypper")
         .arg("dist-upgrade")
+        .arg(if ctx.config().yes(Step::System) { "-y" } else { "" })
         .status_checked()?;
 
     Ok(())
 }
 
 fn upgrade_suse_micro(ctx: &ExecutionContext) -> Result<()> {
     let sudo = require_option(ctx.sudo().as_ref(), REQUIRE_SUDO.to_string())?;
     ctx.run_type()
         .execute(sudo)
-        .args(["transactional-update", "dup"])
+        .arg("transactional-update")
+        .arg(if ctx.config().yes(Step::System) { "-n" } else { "" })
+        .arg("dup")
         .status_checked()?;
 
     Ok(())
 }
 
 fn upgrade_openmandriva(ctx: &ExecutionContext) -> Result<()> {
     let sudo = require_option(ctx.sudo().as_ref(), REQUIRE_SUDO.to_string())?;
@@ -321,14 +325,15 @@
 
     command_update.status_checked()?;
 
     ctx.run_type()
         .execute(sudo)
         .arg(&which("apt-get").unwrap())
         .arg("dist-upgrade")
+        .arg(if ctx.config().yes(Step::System) { "-y" } else { "" })
         .status_checked()?;
 
     Ok(())
 }
 
 fn upgrade_vanilla(ctx: &ExecutionContext) -> Result<()> {
     let apx = require("apx")?;
@@ -495,15 +500,17 @@
     Ok(())
 }
 
 fn upgrade_solus(ctx: &ExecutionContext) -> Result<()> {
     let sudo = require_option(ctx.sudo().as_ref(), REQUIRE_SUDO.to_string())?;
     ctx.run_type()
         .execute(sudo)
-        .args(["eopkg", "upgrade"])
+        .arg("eopkg")
+        .arg(if ctx.config().yes(Step::System) { "-y" } else { "" })
+        .arg("upgrade")
         .status_checked()?;
 
     Ok(())
 }
 
 pub fn run_am(ctx: &ExecutionContext) -> Result<()> {
     let am = require("am")?;
@@ -538,23 +545,36 @@
     let string = String::from_utf8(output.stdout)?;
     let new_version = string.contains("version: 1");
 
     if new_version {
         ctx.run_type()
             .execute(&pacdef)
             .args(["package", "sync"])
+            .arg(if ctx.config().yes(Step::System) {
+                "--noconfirm"
+            } else {
+                ""
+            })
             .status_checked()?;
 
         println!();
         ctx.run_type()
             .execute(&pacdef)
             .args(["package", "review"])
             .status_checked()?;
     } else {
-        ctx.run_type().execute(&pacdef).arg("sync").status_checked()?;
+        ctx.run_type()
+            .execute(&pacdef)
+            .arg("sync")
+            .arg(if ctx.config().yes(Step::System) {
+                "--noconfirm"
+            } else {
+                ""
+            })
+            .status_checked()?;
 
         println!();
         ctx.run_type().execute(&pacdef).arg("review").status_checked()?;
     }
     Ok(())
 }
 
@@ -595,14 +615,19 @@
 }
 
 fn upgrade_clearlinux(ctx: &ExecutionContext) -> Result<()> {
     let sudo = require_option(ctx.sudo().as_ref(), REQUIRE_SUDO.to_string())?;
     ctx.run_type()
         .execute(sudo)
         .args(["swupd", "update"])
+        .arg(if ctx.config().yes(Step::System) {
+            "--assume=yes"
+        } else {
+            ""
+        })
         .status_checked()?;
 
     Ok(())
 }
 
 fn upgrade_exherbo(ctx: &ExecutionContext) -> Result<()> {
     let sudo = require_option(ctx.sudo().as_ref(), REQUIRE_SUDO.to_string())?;
@@ -1010,8 +1035,13 @@
         test_template(include_str!("os_release/deepin"), Distribution::Debian);
     }
 
     #[test]
     fn test_vanilla() {
         test_template(include_str!("os_release/vanilla"), Distribution::Vanilla);
     }
+
+    #[test]
+    fn test_solus() {
+        test_template(include_str!("os_release/solus"), Distribution::Solus);
+    }
 }
```

### Comparing `topgrade-12.0.0/src/steps/os/macos.rs` & `topgrade-12.0.1/src/steps/os/macos.rs`

 * *Files identical despite different names*

### Comparing `topgrade-12.0.0/src/steps/os/openbsd.rs` & `topgrade-12.0.1/src/steps/os/openbsd.rs`

 * *Files identical despite different names*

### Comparing `topgrade-12.0.0/src/steps/os/os_release/fedora` & `topgrade-12.0.1/src/steps/os/os_release/fedora`

 * *Files identical despite different names*

### Comparing `topgrade-12.0.0/src/steps/os/os_release/fedoraremixforwsl` & `topgrade-12.0.1/src/steps/os/os_release/fedoraremixforwsl`

 * *Files identical despite different names*

### Comparing `topgrade-12.0.0/src/steps/os/unix.rs` & `topgrade-12.0.1/src/steps/os/unix.rs`

 * *Files 0% similar despite different names*

```diff
@@ -151,15 +151,15 @@
                 .to_string(),
         )
         .require()?;
 
     print_separator("oh-my-bash");
 
     let mut update_script = oh_my_bash;
-    update_script.push_str("tools/upgrade.sh");
+    update_script.push_str("/tools/upgrade.sh");
 
     ctx.run_type().execute("bash").arg(update_script).status_checked()
 }
 
 pub fn run_oh_my_fish(ctx: &ExecutionContext) -> Result<()> {
     let fish = require("fish")?;
     HOME_DIR.join(".local/share/omf/pkg/omf/functions/omf.fish").require()?;
@@ -379,15 +379,15 @@
         if let Ok(Distribution::NixOS) = Distribution::detect() {
             return Err(SkipStep(String::from("Nix on NixOS must be upgraded via nixos-rebuild switch")).into());
         }
     }
 
     #[cfg(target_os = "macos")]
     {
-        if let Ok(..) = require("darwin-rebuild") {
+        if require("darwin-rebuild").is_ok() {
             return Err(SkipStep(String::from(
                 "Nix-darwin on macOS must be upgraded via darwin-rebuild switch",
             ))
             .into());
         }
     }
```

### Comparing `topgrade-12.0.0/src/steps/os/windows.rs` & `topgrade-12.0.1/src/steps/os/windows.rs`

 * *Files identical despite different names*

### Comparing `topgrade-12.0.0/src/steps/powershell.rs` & `topgrade-12.0.1/src/steps/powershell.rs`

 * *Files identical despite different names*

### Comparing `topgrade-12.0.0/src/steps/remote/ssh.rs` & `topgrade-12.0.1/src/steps/remote/ssh.rs`

 * *Files identical despite different names*

### Comparing `topgrade-12.0.0/src/steps/remote/vagrant.rs` & `topgrade-12.0.1/src/steps/remote/vagrant.rs`

 * *Files identical despite different names*

### Comparing `topgrade-12.0.0/src/steps/tmux.rs` & `topgrade-12.0.1/src/steps/tmux.rs`

 * *Files identical despite different names*

### Comparing `topgrade-12.0.0/src/steps/toolbx.rs` & `topgrade-12.0.1/src/steps/toolbx.rs`

 * *Files 4% similar despite different names*

```diff
@@ -48,14 +48,16 @@
             "-c",
             tb,
             "env",
             &topgrade_prefix,
             topgrade_path,
             "--only",
             "system",
+            "--no-self-update",
+            "--skip-notify",
         ];
         if ctx.config().yes(Step::Toolbx) {
             args.push("--yes");
         }
 
         ctx.run_type().execute(&toolbx).args(&args).status_checked()?;
     }
```

### Comparing `topgrade-12.0.0/src/steps/upgrade.vim` & `topgrade-12.0.1/src/steps/upgrade.vim`

 * *Files identical despite different names*

### Comparing `topgrade-12.0.0/src/steps/vim.rs` & `topgrade-12.0.1/src/steps/vim.rs`

 * *Files identical despite different names*

### Comparing `topgrade-12.0.0/src/steps/zsh.rs` & `topgrade-12.0.1/src/steps/zsh.rs`

 * *Files 15% similar despite different names*

```diff
@@ -161,14 +161,36 @@
         .execute(zsh)
         .args(["-i", "-c", "zimfw upgrade && zimfw update"])
         .status_checked()
 }
 
 pub fn run_oh_my_zsh(ctx: &ExecutionContext) -> Result<()> {
     require("zsh")?;
+
+    // When updating `oh-my-zsh` on a remote machine through topgrade, the
+    // following processes will be created:
+    //
+    // SSH -> ZSH -> ZSH ($SHELL) -> topgrade -> ZSH
+    //
+    // The first ZSH process, won't source zshrc (as it is a login shell),
+    // and thus it won't have the ZSH environment variable, as a result, the
+    // children processes won't get it either, so we source the zshrc and set
+    // the ZSH variable for topgrade here.
+    if ctx.under_ssh() {
+        let zshrc_path = zshrc().require()?;
+        let output = Command::new("zsh")
+            .args([
+                "-c",
+                // ` > /dev/null` is used in case the user's zshrc will have some stdout output.
+                format!("source {} > /dev/null && echo $ZSH", zshrc_path.display()).as_str(),
+            ])
+            .output_checked_utf8()?;
+        env::set_var("ZSH", output.stdout.trim());
+    }
+
     let oh_my_zsh = env::var("ZSH")
         .map(PathBuf::from)
         // default to `~/.oh-my-zsh`
         .unwrap_or(HOME_DIR.join(".oh-my-zsh"))
         .require()?;
 
     print_separator("oh-my-zsh");
```

### Comparing `topgrade-12.0.0/src/sudo.rs` & `topgrade-12.0.1/src/sudo.rs`

 * *Files identical despite different names*

### Comparing `topgrade-12.0.0/src/terminal.rs` & `topgrade-12.0.1/src/terminal.rs`

 * *Files identical despite different names*

### Comparing `topgrade-12.0.0/src/utils.rs` & `topgrade-12.0.1/src/utils.rs`

 * *Files identical despite different names*

### Comparing `topgrade-12.0.0/PKG-INFO` & `topgrade-12.0.1/PKG-INFO`

 * *Files 3% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: topgrade
-Version: 12.0.0
+Version: 12.0.1
 Classifier: Programming Language :: Rust
 Classifier: Programming Language :: Python :: Implementation :: CPython
 Classifier: Programming Language :: Python :: Implementation :: PyPy
 License-File: LICENSE
 Summary: Upgrade all the things
 Keywords: upgrade,update
 Author: Roey Darwish Dror <roey.ghost@gmail.com>, Thomas Schönauer <t.schoenauer@hgs-wt.at>
@@ -46,19 +46,21 @@
 [![Packaging status](https://repology.org/badge/vertical-allrepos/topgrade.svg)](https://repology.org/project/topgrade/versions)
 
 - Arch Linux: [AUR](https://aur.archlinux.org/packages/topgrade)
 - NixOS: [Nixpkgs](https://search.nixos.org/packages?show=topgrade)
 - Void Linux: [XBPS](https://voidlinux.org/packages/?arch=x86_64&q=topgrade)
 - macOS: [Homebrew](https://formulae.brew.sh/formula/topgrade) or [MacPorts](https://ports.macports.org/port/topgrade/)
 - Windows: [Scoop](https://github.com/ScoopInstaller/Main/blob/master/bucket/topgrade.json)
+- PyPi: [pip](https://pypi.org/project/topgrade/)
 
 Other systems users can either use `cargo install` or the compiled binaries from the release page.
 The compiled binaries contain a self-upgrading feature.
 
-Topgrade requires Rust 1.60 or above.
+> Currently, Topgrade requires Rust 1.65 or above. In general, Topgrade tracks 
+> the latest stable toolchain.
 
 ## Usage
 
 Just run `topgrade`.
 
 Visit the documentation at [topgrade-rs.github.io](https://topgrade-rs.github.io/) for more information.
```

#### html2text {}

```diff
@@ -1,8 +1,8 @@
-Metadata-Version: 2.1 Name: topgrade Version: 12.0.0 Classifier: Programming
+Metadata-Version: 2.1 Name: topgrade Version: 12.0.1 Classifier: Programming
 Language :: Rust Classifier: Programming Language :: Python :: Implementation
 :: CPython Classifier: Programming Language :: Python :: Implementation :: PyPy
 License-File: LICENSE Summary: Upgrade all the things Keywords: upgrade,update
 Author: Roey Darwish Dror
 ghost@gmail.com>, Thomas SchÃ¶nauer
 schoenauer@hgs-wt.at> Author-email: Roey Darwish Dror
 ghost@gmail.com>, Thomas SchÃ¶nauer
@@ -23,36 +23,38 @@
 ## Installation [![Packaging status](https://repology.org/badge/vertical-
 allrepos/topgrade.svg)](https://repology.org/project/topgrade/versions) - Arch
 Linux: [AUR](https://aur.archlinux.org/packages/topgrade) - NixOS: [Nixpkgs]
 (https://search.nixos.org/packages?show=topgrade) - Void Linux: [XBPS](https://
 voidlinux.org/packages/?arch=x86_64&q=topgrade) - macOS: [Homebrew](https://
 formulae.brew.sh/formula/topgrade) or [MacPorts](https://ports.macports.org/
 port/topgrade/) - Windows: [Scoop](https://github.com/ScoopInstaller/Main/blob/
-master/bucket/topgrade.json) Other systems users can either use `cargo install`
-or the compiled binaries from the release page. The compiled binaries contain a
-self-upgrading feature. Topgrade requires Rust 1.60 or above. ## Usage Just run
-`topgrade`. Visit the documentation at [topgrade-rs.github.io](https://
-topgrade-rs.github.io/) for more information. > **Warning** > Work in Progress
-## Configuration See `config.example.toml` for an example configuration file.
-### Configuration Path #### `CONFIG_DIR` on each platform - **Windows**:
-`%APPDATA%` - **macOS** and **other Unix systems**: `${XDG_CONFIG_HOME:-
-~/.config}` `topgrade` will look for the configuration file in the following
-places, in order of priority: 1. `CONFIG_DIR/topgrade.toml` 2. `CONFIG_DIR/
-topgrade/topgrade.toml` If the file with higher priority is present, no matter
-it is valid or not, the other configuration files will be ignored. On the first
-run(no configuration file exists), `topgrade` will create a configuration file
-at `CONFIG_DIR/topgrade.toml` for you. ### Custom Commands Custom commands can
-be defined in the config file which can be run before, during, or after the
-inbuilt commands, as required. By default, the custom commands are run using a
-new shell according to the `$SHELL` environment variable on unix (falls back to
-`sh`) or `pwsh` on windows (falls back to `powershell`). On unix, if you want
-to run your command using an interactive shell, for example to source your
-shell's rc files, you can add `-i` at the start of your custom command. But
-note that this requires the command to exit the shell correctly or else the
-shell will hang indefinitely. ## Remote Execution You can specify a key called
+master/bucket/topgrade.json) - PyPi: [pip](https://pypi.org/project/topgrade/
+) Other systems users can either use `cargo install` or the compiled binaries
+from the release page. The compiled binaries contain a self-upgrading feature.
+> Currently, Topgrade requires Rust 1.65 or above. In general, Topgrade tracks
+> the latest stable toolchain. ## Usage Just run `topgrade`. Visit the
+documentation at [topgrade-rs.github.io](https://topgrade-rs.github.io/) for
+more information. > **Warning** > Work in Progress ## Configuration See
+`config.example.toml` for an example configuration file. ### Configuration Path
+#### `CONFIG_DIR` on each platform - **Windows**: `%APPDATA%` - **macOS** and
+**other Unix systems**: `${XDG_CONFIG_HOME:-~/.config}` `topgrade` will look
+for the configuration file in the following places, in order of priority: 1.
+`CONFIG_DIR/topgrade.toml` 2. `CONFIG_DIR/topgrade/topgrade.toml` If the file
+with higher priority is present, no matter it is valid or not, the other
+configuration files will be ignored. On the first run(no configuration file
+exists), `topgrade` will create a configuration file at `CONFIG_DIR/
+topgrade.toml` for you. ### Custom Commands Custom commands can be defined in
+the config file which can be run before, during, or after the inbuilt commands,
+as required. By default, the custom commands are run using a new shell
+according to the `$SHELL` environment variable on unix (falls back to `sh`) or
+`pwsh` on windows (falls back to `powershell`). On unix, if you want to run
+your command using an interactive shell, for example to source your shell's rc
+files, you can add `-i` at the start of your custom command. But note that this
+requires the command to exit the shell correctly or else the shell will hang
+indefinitely. ## Remote Execution You can specify a key called
 `remote_topgrades` in the configuration file. This key should contain a list of
 hostnames that have Topgrade installed on them. Topgrade will use `ssh` to run
 `topgrade` on remote hosts before acting locally. To limit the execution only
 to specific hosts use the `--remote-host-limit` parameter. ## Contribution ###
 Problems or missing features? Open a new issue describing your problem and if
 possible provide a solution. ### Missing a feature or found an unsupported
 tool/distro? Just let us now what you are missing by opening an issue. For
```

