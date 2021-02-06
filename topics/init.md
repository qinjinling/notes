# Ubuntu 安装 node

建议使用 nvm，如果之前安装过 node，先卸载
```bash
sudo apt-get remove nodejs
#执行前请确认这个包是否存在这个位置
sudo rm -rf /usr/lib/node_moudles
#然后安装nvm
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.37.2/install.sh | bash
```

之后添加这两行到你的 .zshrc
```bash
export NVM_DIR="$HOME/.nvm"
source ~/.nvm/nvm.sh
```

``` bash
#设置镜像解决安装慢的问题 https://github.com/xhlwill/blog/issues/7
export NVM_NODEJS_ORG_MIRROR=https://npm.taobao.org/mirrors/node/
nvm install node
# npm
npm config set registry https://registry.npm.taobao.org
npm config set disturl https://npm.taobao.org/dist
# yarn
yarn config set registry https://registry.npm.taobao.org
yarn config set disturl https://npm.taobao.org/dist
```

