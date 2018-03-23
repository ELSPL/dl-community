# Helpful Linux Commands


### get list of Jupyter Notebook sessions
```
jupyter notebook list
```

### list CPU GPU memory usage:  
```
htop
```

### see GPU usage
```
nvidia smi
```

### list number of lines in a file
`wc -l file.csv`  

If you use a Python variable inside a Jupyter shell command, need to put it inside brackets:  
`PATH = "data/bulldozers"`  
`!ls {PATH}`
 
### copying LOTS of files from one directory to another
#### `rsync`

https://askubuntu.com/questions/217764/argument-list-too-long-when-copying-files

