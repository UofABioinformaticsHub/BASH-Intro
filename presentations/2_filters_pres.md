## Session 2: Filters

+++

## Last session

- Found our way around (`pwd`, `cd`, `ls`)
- Created new directories and files (`touch`, `mkdir`)
- Deleted directories and files (`rm `, `rmdir`)

+++

## Data Streams

- We gave a command either no arguments (e.g. `ls`, `pwd`)
- Or we specified a directory/file path as an argument
- Results were always printed to the terminal: `stdout`

+++

## Output Redirection

Today:

- We'll discover that we can redirect `stdout`
- Some commands can also accept `stdin`
- These commands are known as `filters`

+++

### Filters

![DataStreams](https://raw.githubusercontent.com/UofABioinformaticsHub/BASH-Intro/master/images/2-streams.png)

Many NGS tools use these streams:

e.g. Alignments to `stdout`, diagnostics to `stderr`

+++

### Filters

![](https://camo.githubusercontent.com/1652e94dd89d73b1e5ad43feabe12d5aac7e033b/68747470733a2f2f646f63732e676f6f676c652e636f6d2f64726177696e67732f642f3161444b397a716163677572465a537a6a704c4d5653676f64306a462d4b4648576553565f53554c387668452f7075623f773d39313626683d333534)
