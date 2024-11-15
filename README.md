# Fortran Development and Debugging Template for VSCode

This repository provides a template for setting up a Fortran development and debugging environment using [Visual Studio Code (VSCode)](https://code.visualstudio.com/) and the [Modern Fortran extension](https://marketplace.visualstudio.com/items?itemName=fortran-lang.linter-gfortran). It includes necessary configuration files and instructions for compiling, running, and debugging Fortran programs in VSCode using gfortran and gdb.

## Quickstart

1. Clone this repository:
```bash
git clone https://github.com/tornikeo/fortran-vscode-template.git
cd fortran-vscode-template
```

2. **Install Required Extensions in VSCode:**

    * Modern Fortran (installs C/C++ support)
    Alternatively: Fortran Breakpoint Support (also requires C/C++ support). Press `Ctrl+Shift+P` and paste
    ```sh
    ext install fortran-lang.linter-gfortran
    ```

3. **Open the Project in VSCode:**
    * Launch VSCode and open this folder (File > Open Folder...).
4. Check that fortran compiler `gfortran` works
    ```sh
    gfortran --version # ... GNU Fortran (Ubuntu 12.2.0-3ubuntu1) 12.2.0
    ```
## Repository Contents
- `hello.f90`: A simple "Hello, World!" Fortran program, which can be debugged step-by-step in VSCode.
- `.vscode/tasks.json`: Defines a task for building Fortran code with gfortran.
- `.vscode/launch.json`: Configures the VSCode debugger to use gdb for debugging Fortran programs.

## Running the Code
### Compile and Run

To compile and run the code:

1. Build the Program:
    - From the VSCode menu, go to Terminal > Run Task... and select the "gfbuild" task.
    - This will compile hello.f90 with debugging flags for gdb.

1. Run the Program:
    - Open the VSCode terminal and run the compiled binary manually:
```sh
./hello.exe
```

## Debugging
1. Set Breakpoints:
    * Open hello.f90 in the editor and set breakpoints by clicking to the left of any line where you'd like the debugger to pause.
1. Start Debugging:
    * Go to Run > Start Debugging in the VSCode menu.
    The debugger should pause at any set breakpoints, allowing you to step through the code, inspect variables, and analyze the call stack.
    * Alernatively, press the `F5` key on your keyboard.

For a detailed walkthrough, refer to the VSCode Fortran Debugging Tutorial.

## License

This repository is licensed under the MIT License. See the LICENSE file for details