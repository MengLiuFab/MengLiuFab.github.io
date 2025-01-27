### 如何设置 VS Code 以进行数据科学工作
English version can be found [here](https://mengliufab.github.io/2025/01/27/How-to-set-up-vscode-for-python-DS.md)
---

## **1. 安装 VS Code**
1. 从[这里](https://code.visualstudio.com/)下载并安装 VS Code。
2. 从[这里](https://docs.conda.io/en/latest/miniconda.html)下载并安装 Miniconda。
3. 从[这里](https://git-scm.com/)下载并安装 Git。

---

## **2. 安装 Python 扩展**
如果你习惯使用Matlab，特别是类似 Matlab 的并排代码编辑器，下文会很有用：

1. **安装 Python 扩展**：
   - 点击屏幕左侧的扩展市场图标（左边第四个图标）。
   - 搜索 `Python` 并安装 Microsoft 提供的 Python 扩展。此扩展将启用 Python 的语法高亮和调试功能。
   - 确保扩展已安装，可以在“已安装”标签中查看。
   - 安装此扩展时，还会自动下载 `Pylance` 和 `Python Debugger`。

2. **安装 Jupyter 扩展**：
   - 安装 `Jupyter` 扩展以支持在 VS Code 中运行 Jupyter Notebook。
   - 此扩展还包括 `Jupyter Slide Show`，可将 Jupyter Notebook 在右侧显示为工作区。

---

## **3. 在 VS Code 中运行 Jupyter Notebook 并启用并排代码编辑器**
现在可以在 VS Code 中运行 Jupyter Notebook，并使用并排代码编辑器进行代码和输出查看。这类似于 Matlab 的 Live Editor。

### **运行步骤**：
1. 在想运行的代码单元开头添加以下标记：
   ```python
   #%%
   ```
   按下 `Shift + Enter` 可以运行该单元。运行后，代码编辑器的右侧会显示输出内容，这与 Matlab 的 Live Editor 行为相似。

2. **其他快捷操作**：
   - 如果要运行整个 Notebook，可以按下 `Ctrl + Shift + P`，然后输入 `Run All Cells`，即可运行 Notebook 中的所有单元。
   - 如果对 Python 此刻使用的解释器感到困惑（即你当前python所处的环境），可以点击屏幕左下角显示的解释器名称（如 `Python 3.8.8 64-bit ('base': conda)`），选择想要使用的解释器。Notebook 使用的解释器也会显示在并排代码编辑器的右上角，你可以点击名称进行更改。

---

## **其他工具与设置**

### **代码格式化工具**
1. 选择一个格式化工具，参考 [官方指南](https://code.visualstudio.com/docs/python/formatting)。
   - 我使用的是 `black formatter`。
2. 设置默认格式化工具：
   - 按下 `Ctrl + Shift + P`，输入 `Preference: Open Settings (UI)`。
   - 搜索 `formatter`，将默认格式化工具更改为 `Black Formatter`。
3. 启用“保存时格式化”功能：
   - 按下 `Ctrl + Shift + P`，输入 `Preference: Open Settings (UI)`。
   - 搜索 `format on save` 并勾选此选项。该功能可以让你在保存文件时自动格式化代码。

### **代码检查工具**
1. 选择一个代码检查工具，参考 [官方指南](https://code.visualstudio.com/docs/python/linting)。
   - 我使用的是 `pylint`。

### **使用终端**
1. 在 VS Code 中打开终端：
   - 按下 `` Ctrl + ` ``，终端会出现在屏幕底部。
   - 或点击顶部菜单中的 **Terminal** 选项。
2. 使用终端中的 `conda` 命令安装软件包、创建环境和管理环境。
3. 终端中修改环境后，重启或重新打开并排代码编辑器以查看更改效果。
4. 如果你改变了环境中的依赖包，记得重启或重新打开并排代码编辑器。

