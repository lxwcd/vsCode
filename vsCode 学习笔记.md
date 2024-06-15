vsCode 使用笔记

# 资源
> [官方文档](https://code.visualstudio.com/docs)

# 界面介绍
> [user interface](https://code.visualstudio.com/docs/getstarted/userinterface)

# 配置
> [settings](https://code.visualstudio.com/docs/getstarted/userinterface#_settings)

Visual Studio Code (VSCode) 提供了灵活的配置系统，允许用户根据自己的需要自定义编辑器的行为和外观。主要的配置文件包括：

1. **settings.json** - 这是VSCode最常用的配置文件，用于存储编辑器设置，如主题、字体大小、自动保存等。这些设置可以在用户级别或工作区级别进行配置。
   - **位置**：
     - 用户设置：`%APPDATA%\Code\User\settings.json` (Windows) 或 `~/.config/Code/User/settings.json` (Linux/Mac)。
     - 工作区设置：在工作区文件夹中的`.vscode/settings.json`。

2. **keybindings.json** - 用于自定义键盘快捷键。用户可以覆盖默认的快捷键或添加新的快捷键绑定。
   - **位置**：
     - 用户快捷键：`%APPDATA%\Code\User\keybindings.json` (Windows) 或 `~/.config/Code/User/keybindings.json` (Linux/Mac)。

3. **launch.json** - 与调试相关的配置文件，用于配置调试会话的参数，比如启动的程序、调试器的路径等。
   - **位置**：位于`.vscode`文件夹内的`launch.json`文件，这个文件夹通常位于项目的根目录中。

4. **tasks.json** - 用于定义项目中的任务，比如编译项目、运行测试等。VSCode可以通过这些定义的任务来执行外部命令。
   - **位置**：跟`launch.json`一样，位于`.vscode/tasks.json`。

5. **extensions.json** - 推荐的插件列表，新加入工作区的成员可以看到推荐安装的插件，便于团队成员保持一致的开发环境设置。
   - **位置**：位于`.vscode/extensions.json`。

这些配置文件让VSCode变得非常灵活，用户可以通过修改这些文件来实现高度个性化的编辑器配置。
可以通过在VSCode中按下`Ctrl + ,`快捷键，或是在命令面板(`Ctrl + Shift + P`)中查找并打开`打开设置(JSON)`来访问`settings.json`文件。
对于其他配置文件，如`keybindings.json`、`launch.json`等，你可以在`.vscode`文件夹中找到它们（如果文件夹或文件不存在，可能需要手动创建）。


## settings.json
> 参考配置：[mirror-vscode](https://github.com/Imymirror/mirror-vscode)
> [settings.json](https://github.com/lxwcd/vsCode/blob/main/settings.json)

期望效果：
- 编辑区域使用 vim 快捷键，尽量和其他地方 vim 快捷键配置一致
- 其他区域自定义快捷键

### 相关插件
#### Vim (VSCodeVim)
> [VSCodeVim](https://github.com/VSCodeVim/Vim)

编辑器使用 vim 快捷键

#### Which Key (vscode-which-key)
> [vscode-which-key](https://github.com/VSpaceCode/vscode-which-key)

定制其他区域的快捷键

### 