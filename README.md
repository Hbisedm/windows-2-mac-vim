# Windows2Mac&Vim

> 换了环境，只能用Windows，所以配置各种工作流软件，适应Windows的Mac化操作和Vim的操作。

## 静默文本OCR

[STranslate](https://github.com/zggsong/stranslate)

![](./assets/1.png)
## 改键

一开始使用 `PowerToys` 进行改键，后发现太难用了，而且改的规则有很多[问题]( https://eli-ven.github.io/posts/shortcuts/)。后面改为使用[AutoHotkey](https://www.autohotkey.com/)进行改键。这是我的配置[配置](./assets/maps.ahk)。但是`PowerToys`里面的`PowerToys Run`功能很强大，我只使用3个插件， 提升我的工作开发效率：

- ClipboardManager
- Everything
- Translator

> 将软件放到开机启动目录下`{C:\Users\username\AppData\Roaming\Microsoft\Windows\Start Menu\Programs\Startup}`

## 配置终端 

cygwin   安装时选个zsh

配置终端样式 

- cygwin/zsh/on-my-zsh/p10k
- [字体](https://github.com/romkatv/powerlevel10k?tab=readme-ov-file#meslo-nerd-font-patched-for-powerlevel10k)

![[2.png]]

## 配置输入法-rime

在 Windows 下的 rime（小狼毫）现在也可以配置 vim_mode 了。  

为了使用切换应用后，可以切换对应的大小写模式。需要下载[每夜构建的版本](https://github.com/rime/weasel/releases/tag/latest)

weasel.custom.yaml  
```yaml
patch:  
  'app_options/+':  
    code.exe: # 这里是应用可执行文件的名字，带后缀  
      inline_preedit: false # 在输入法中预编辑，防止 vscode vim 中输入法闪烁  
      ascii_mode: true  
      vim_mode: true
```

推荐：一个输入法方案-[四叶草](https://github.com/fkxxyz/rime-cloverpinyin)


## 窗口切换-[window-switcher](https://github.com/sigoden/window-switcher)

配置

```ini
# Whether to show trayicon, yes/no
trayicon = yes 

[switch-windows]

# Hotkey to switch windows
hotkey = alt+`

# List of hotkey conflict apps
# e.g. game1.exe,game2.exe
blacklist =

# Ignore minimal windows
ignore_minimal = no

[switch-apps]

# Whether to enable switching apps
enable = yes

# Hotkey to switch apps
hotkey = alt+tab

# Ignore minimal windows
ignore_minimal = no
```

## VSCoode

vim配置

- [settings.json](../assets/settings.json)
- [keysbindings.json](../assets/keysbindings.json)