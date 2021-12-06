This file contains some of the commands run during the DAC21 tutorial. It assumes that you have a working build of SystemArchitect 
and the yaml file in this directory.

Check that your tools are in your PATH. 
```
which cglci
```

Generate a Dotfile output of the YAML file and convert it to a PNG image.
```
cgcli --ir BasicRV32I.yaml --dot BasicRV32I.yaml.dot
dot -Tpng BasicRV32I.yaml.dot > BasicRV32I.png
```

Run StoneCutter on a sample stonecutter file.
```
sccomp --keep ./SAMPLE/RTL/stonecutter/BasicRV32I.ISA.sc
```
