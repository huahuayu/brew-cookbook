# brew-cookbook(working in progress)
mac包管理工具brew cookbook, brew烹饪书, brew by examples

## brew faq
https://docs.brew.sh/FAQ  

## brew help
```
shiming@pro ➜  ~ brew --help
Example usage:
  brew search [TEXT|/REGEX/]  # 搜索软件
  brew info [FORMULA...]      # 查看已安装的软件信息
  brew install FORMULA...     # 安装软件
  brew update                 # 从github上fetch最新的Homebrew和软件包信息，并安装最新的Homebrew版本
  brew upgrade [FORMULA...]   # 更新brew已安装的软件到最新版
  brew uninstall FORMULA...   # 卸载软件
  brew list [FORMULA...]      # 查看所有已安装的软件

Troubleshooting:
  brew config                 # 显示brew版本信息、系统版本信息等等，提交bug前运行brew config可帮助开发者定位问题
  brew doctor                 # 检查潜在的系统问题
  brew install --verbose --debug FORMULA

Contributing:
  brew create [URL [--no-fetch]]
  brew edit [FORMULA...]

Further help:
  brew commands
  brew help [COMMAND]
  man brew
  https://docs.brew.sh
 ```
 
## brew uninstall
## brew doctor
`brew doctor`的作用是健康检查，有问题就会列出来并给出解决方法：  
``` bash
shiming@pro ➜  ~ brew doctor
Please note that these warnings are just used to help the Homebrew maintainers
with debugging if you file an issue. If everything you use Homebrew for is
working fine: please don't worry or file an issue; just ignore this. Thanks!

Warning: The following directories do not exist:
/usr/local/sbin

You should create these directories and change their ownership to your account.
  sudo mkdir -p /usr/local/sbin
  sudo chown -R $(whoami) /usr/local/sbin

Warning: You have unlinked kegs in your Cellar.
Leaving kegs unlinked can lead to build-trouble and cause brews that depend on
those kegs to fail to run properly once built. Run `brew link` on these:
  python@2
  python
  mtr
 ```
 
## 查看已安装的包信息
``` zsh
shiming@pro ➜  .dotfile git:(master) brew info nvm
nvm: stable 0.34.0, HEAD
Manage multiple Node.js versions
https://github.com/creationix/nvm
/usr/local/Cellar/nvm/0.34.0 (7 files, 141.7KB) *
  Built from source on 2019-03-13 at 14:07:40
From: https://github.com/Homebrew/homebrew-core/blob/master/Formula/nvm.rb
==> Options
--HEAD
	Install HEAD version
==> Caveats
Please note that upstream has asked us to make explicit managing
nvm via Homebrew is unsupported by them and you should check any
problems against the standard nvm install method prior to reporting.

You should create NVM's working directory if it doesn't exist:

  mkdir ~/.nvm

Add the following to ~/.zshrc or your desired shell
configuration file:

  export NVM_DIR="$HOME/.nvm"
  [ -s "/usr/local/opt/nvm/nvm.sh" ] && . "/usr/local/opt/nvm/nvm.sh"  # This loads nvm
  [ -s "/usr/local/opt/nvm/etc/bash_completion" ] && . "/usr/local/opt/nvm/etc/bash_completion"  # This loads nvm bash_completion

You can set $NVM_DIR to any location, but leaving it unchanged from
/usr/local/opt/nvm will destroy any nvm-installed Node installations
upon upgrade/reinstall.

Type `nvm help` for further information.

Bash completion has been installed to:
  /usr/local/etc/bash_completion.d
==> Analytics
install: 27,929 (30 days), 81,630 (90 days), 291,433 (365 days)
install_on_request: 27,273 (30 days), 79,122 (90 days), 279,022 (365 days)
build_error: 0 (30 days)
```
