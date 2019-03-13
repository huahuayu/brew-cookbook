# brew-cookbook(working in progress)
mac包管理工具brew cookbook, brew烹饪书, brew by examples

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
