# Tutorial: Install R and Jupyter for Visual Studio Code on macOS

## 1. Install Homebrew

Homebrew is an unofficial package manager for macOS (similar to `apt` for Debian/Ubuntu or `winget` on modern Windows).

1. Go to <https://brew.sh>
2. Copy the line under **Install Homebrew** header. At the time of writing it
   is as follows:  
   `/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"`
3. Open Terminal app.
   1. Press `⌘CMD + SPACE` to open Spotlight Search.
   2. Type *Terminal*.
   3. Select *Terminal.app* using `⏎ENTER`.
4. Paste the line from Homebrew website and press `⏎ENTER`.
5. Follow instructions on the screen (sorry, I did that years ago and I am not
   sure if there are any user actions required).

## 2. Install R and dependencies via Homebrew

1. Using the terminal install the following packages. The lines below are full
   commands, so you can paste and execute them one by one).
   - `brew install libxml2`
   - `brew install R`
   - `brew install jupyterlab` (optional)
   - `brew install rstudio` (optional)

## 3. Install required R packages

1. Still in Terminal, type `R` to enter **R Console**.
2. Install language server for R support in Visual Studio Code:  
   - `install.packages("languageserver")`
3. Install R kernel for Jupyter:
   - `install.packages('IRkernel')`
   - `IRkernel::installspec()`
4. Install Tidyverse:
   - `install.packages("tidyverse")`

## 4. Install Visual Studio Code

1. Go to the [official website](https://code.visualstudio.com/download) and
   download the app.
2. Move `Visual Studio Code.app` from `~/Downloads` directory to
   `/Applications`. You can use the following terminal command (paste and
   execute after downloading the file):  
   `mv ~/Downloads/"Visual Studio Code.app" /Applications/`
3. Open Visual Studio Code (either from Launchpad or `⌘CMD + SPACE` and type its
   name).

## 5. Install required extensions

1. Open extensions pane as shown on the picture below.
   ![image](https://code.visualstudio.com/assets/docs/editor/extension-marketplace/search-for-todo-extension.png)
2. Install the following extensions (paste each line in search prompt, it should
   list a single item as those are unique identifiers).
   - `reditorsupport.r`
   - `rdebugger.r-debugger`
   - `ms-toolsai.jupyter`
3. Open example Jupyter Notebook file and check if everything works. You may
   need to choose the correct kernel. Based on the example below, you would need
   to click on the button in the upper right corner saying
   "Python 3.8.8 64-bit ...". In your case it may say "Select kernel..." or show
   some other Python version.
   ![image](https://raw.githubusercontent.com/microsoft/vscode-jupyter/main/images/Jupyter%20README/notebookui.png?)
