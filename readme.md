# autoautoAug v0.1

## Description
Execute [Augustus'](https://github.com/Gaius-Augustus/Augustus) `autoAug.pl` automatically if no `--singleCPU` option is set.

`autoautoAug` is tested with Augustus 3.2.2 and 2.5.5

## Dependencies
- Augustus: [https://github.com/Gaius-Augustus/Augustus](https://github.com/Gaius-Augustus/Augustus)
- Parallel::Loops: [https://metacpan.org/pod/Parallel::Loops](https://metacpan.org/pod/Parallel::Loops)

## Usage
```
autoautoAug [options] -opt <autoAug.pl_options>
```

__Mandatory:__
```
-opt STR        STR is a file containing all autoAug.pl options in the first line sperated by space without
                the calling of the autoAug.pl script
```

__Options: [default]__
```
-t INT          Number of parallel executed aug-scripts [2]
-speed          Execute all aug-scripts from one batch in parallel [off]
                Overrides -t
-acp STR        STR is the Augustus config path to locate autoAug.pl [automatic from bash variables]
-log STR        STR is the prefix for log (STR.log) and error (STR.err) files [autoautoAug]
                STR.log will be used to extract the command that will run after a aug-script
                batch is finished
-h or -help     Print this help and exit
```
