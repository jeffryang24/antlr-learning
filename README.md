# Learning ANTLR4

Learn parsing using ANTLR4. Don't be serious about the shell script. I just learn how to make a better shell script for the project automation.

## How to use this repository?

You can install ANTLR4 using `antlr4_l` script inside this repository.

```bash
antlr4_l install
```

To uninstall it, just issuing

```bash
antlr4_l uninstall
```

Or if you already have ANTLR4 inside your rig, you can just use `antlr4_l` to execute the grammar.

```bash
antlr4_l --lang=Python3 --out=python/output [antlr4-arguments]
```

## Is `antlr4_l` script portable?

Yes, you can copy it to another ANTLR4 project for helping you generating grammar. This script is just a wrapper btw..

## Experimental

If you want to use restricted mode (the `antlr4_l` command will be restrictly available through your project subdirectory), just issuing below command.

```bash
# If you use default install, then below command 
# is not required.
antlr4_l lite-install     # Generate activation script

source antlr4_l_activate

# To deactivate current environment
antlr4_l_stop
```

In the future, this script will handle multi ANTLR version (I hope I have free time to fulfill it. Hahaha...)
