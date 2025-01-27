# How I set up my VS code for Data Science

---

中文版请点击[这里](https://mengliufab.github.io/2025/01/27/How-to-set-up-vscode-for-python-DS-CN.html)

## 1. Install VS code
- Download and install VS code from [here](https://code.visualstudio.com/)
- Download and install Miniconda from [here](https://docs.conda.io/en/latest/miniconda.html)
- Download and install Git from [here](https://git-scm.com/)

## 2. Install Python extension
If you are miggarting from Matlab, or prefer a Matlab-like side-by-side code editor, following settings will be useful.
- Install Python extension for VS code. The extension marketplace can be accessed by clicking on the square icon on the left side of the screen, the fourth icon from the top.
Search `Python` and install the extension by Microsoft. This will enable Python syntax highlighting, debugging, and intellisense. Check the Installed tab to see if the extension is installed. It will also download `Pylance`, `Python Debugger`. 
- Install `Jupyter` extension for VS code. This will enable Jupyter notebook support in VS code. This will also include the `Jupyter Slide Show` extension, which will allow you to present your Jupyter notebook as a slide show.

## 3. Run Jupyter notebook in VS code with Side-by-Side code editor
Now you can run Jupyter notebook in VS code with side-by-side code editor. This will allow you to write code in one side and see the output in the other side. This is similar to Matlab's live editor. 
To do so, you need to add 
```python
#%%
```
in the beginning of the cell you want to run. This will allow you to run the cell by pressing `Shift + Enter`. And this will automatically show the right side of the code editor with the output. This behavior is similar to Matlab's live editor.
### Special notes 
- If you want to run the entire notebook, you can press `Ctrl + Shift + P` and type `Run All Cells`. This will run all the cells in the notebook.
- If you are confused about the interpreter, you can click on the bottom left corner of the screen where it says `Python 3.8.8 64-bit ('base': conda)` and select the interpreter you want to use. This will allow you to use different interpreters for different notebooks. However, the interpreter you used for the notebook will be on the right top corner of the side-by-side code editor. You can change the interpreter by clicking on the interpreter name.

## Others
- Choose a formatter, check the guide [here](https://code.visualstudio.com/docs/python/formatting). I use `black formatter` as my formatter. Remember to change default formatter by pressing `Ctrl + Shift + P` and typing `Preference:Open Setting (UI)`. Search `formatter` and change the default formatter to `Black Formatter`.
To let the formatter automatically format the code every time you save the file, you can check the `Format on Save` option in the settings. Press `Ctrl + Shift + P` and type `Preference:Open Setting (UI)`. Search `format on save` and check the box.

- Choose a linter, check the guide [here](https://code.visualstudio.com/docs/python/linting). I use `pylint` as my linter. 
  
- Use terminal in VS code. You can open the terminal by pressing `` Ctrl + ` ``. This will open the terminal in the bottom of the screen. You can also open the terminal by clicking on the **Terminal** tab on the top of the screen. This will allow you to run the terminal in the VS code. Use `conda` to install packages, create environments, and manage environments in the terminal as you need. Remember to restart or simply close the side by side code editor and open it again to see the changes you made in the terminal. If you changed the denpendent packages, you need to restart the kernel to see the changes.
