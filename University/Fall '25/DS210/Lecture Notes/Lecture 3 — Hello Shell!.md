>[!abstract]
>*This module introduces you to the command-line interface and essential shell commands that form the foundation of systems programming and software development. You'll learn to navigate the file system, manipulate files, and use the terminal effectively for Rust development.*

## KItchen Metaphor (Shell)

- **The waiter (the shell):** The interface that takes your orders. In the metaphor, you (the user) give your command to the shell (the waiter). For example, if you type `ls`, you are telling the waiter what you want.
- **The menu (the command list):** The restaurant's menu is the list of dishes you can order. Similarly, the shell's command set lists the operations you can request. The shell script menu is a list of commands you can use to interact with the system.
- **The kitchen (the kernel):** The part of the operating system that does the heavy work. It manages the hardware resources, executes processes, and performs the requested actions. Just as the customer is not allowed into the kitchen, the user programs don't directly access the kernel.
- **The chef and cooks (system calls):** The authorized personnel in the kitchen who perform the work. System calls are the official and secure way for the shell to pass your request to the kernel and get it executed.
- **The finished meal (the output):** The result of your command. The shell receives the output from the kernel and presents it to you, just as the waiter brings your food to your table.

## Navigating the Shell

- Use `Tab` for auto-completion
- Use `Up Arrow` to access command history
- Try `control-c` to abort something running or clear a line
- You can't click into a line to edit it, use left/right arrows (or vim, or copy-paste)

__Command__: An order to the command line, the first thing that is inputted into the shell

__Argument__: A specification to the command in the command line

__Options/Flags__: A special kind of argument usually starting with a dash and declared before other arguments

