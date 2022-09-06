## lazygit
- 个人最常用命令行软件之一，摆脱输入命令困扰，一个字快！
- 不得不称赞太好用，用了就回不去了
### lazygit 是什么
#### git 的痛点
- 众所周知 Git 是一个强大的工具，但是其命令复杂性让人感到痛苦。 git commit 可能要输入一大串，还可能输入错误。当然 pull 和 push 当然还好，你也可以 alias敲几个字母（也需要记忆）
- 但是涉及到 rebase，特别是频繁 rebase，rename 等，命令输入就让人有点烦躁了
- 还有 git log 总感觉 不舒服
...
### lazygit做了什么
- lazygit 将复杂的命令行转为了终端 ui 操作，只需要记住几个快捷键，甚至都不用记忆，可以按 x 提示，然后使用，用多了自然就快了。
- 使用 lazygit 你仍然需要学习 git，知道 git 中各个操作代表什么！然后才能来 lazy！！！
![](https://cdn.jsdelivr.net/gh/matyle/tupic/img/20220904124536.png)


### 为什么使用
- 简化输入命令的次数
	- git pull push add commit rebase reset... pickcherry
- 简化 rebase，commit，tag 等操作
- every thing is Simple！！

>If you're a mere mortal like me and you're tired of hearing how powerful git is when in your daily life it's a powerful pain in your ass, lazygit might be for you.
>如果您像我一样只是凡人，并且厌倦了在日常生活中听到 git 的强大功能，而这对您来说是一种强大的痛苦，那么lazygit 可能适合您。

![](https://cdn.jsdelivr.net/gh/matyle/tupic/img/20220904084849.png)

### 个人使用演示视频

![](https://cdn.jsdelivr.net/gh/matyle/tupic/img/Video_22-09-04_10-49-02.gif)

![](https://cdn.jsdelivr.net/gh/matyle/tupic/img/lazygit_rec.gif)


### 开源地址及安装
>A simple terminal UI for git commands, written in Go with the [gocui](https://github.com/jroimartin/gocui "gocui") library.

<div class="rich-link-card-container"><a class="rich-link-card" href="https://github.com/jesseduffield/lazygit" target="_blank">
	<div class="rich-link-image-container">
		<div class="rich-link-image" style="background-image: url('https://opengraph.githubassets.com/889b7fcdc8b31e14b6b534170a27422af372a03073f8ac9a2beba0345dc1e02d/jesseduffield/lazygit')">
	</div>
	</div>
	<div class="rich-link-card-text">
		<h1 class="rich-link-card-title">GitHub - jesseduffield/lazygit: simple terminal UI for git commands</h1>
		<p class="rich-link-card-description">
		simple terminal UI for git commands. Contribute to jesseduffield/lazygit development by creating an account on GitHub.
		</p>
		<p class="rich-link-href">
		https://github.com/jesseduffield/lazygit
		</p>
	</div>
</a></div>

- 提供常用系统安装，更多系统安装参考 github 
 
```bash
// mac

brew install jesseduffield/lazygit/lazygit

//linux ubuntu 下面3步
LAZYGIT_VERSION=$(curl -s "https://api.github.com/repos/jesseduffield/lazygit/releases/latest" | grep -Po '"tag_name": "v\K[0-35.]+')


curl -Lo lazygit.tar.gz "https://github.com/jesseduffield/lazygit/releases/latest/download/lazygit_${LAZYGIT_VERSION}_Linux_x86_64.tar.gz"

sudo tar xf lazygit.tar.gz -C /usr/local/bin lazygit

//完成后输入 
lazygit

```

---
#blog #linux #terminal 
