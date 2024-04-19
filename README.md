# Muse
![img](https://github.com/alexandrebarachant/muse-lsl/blob/master/blinks.png?raw=true)

## Getting Started

### Creating virtual env
``` 
    pip install virtualenv
    python -m venv muse
    source muse/bin/activate
```

## Muse LSL
A Python package for streaming, visualizing, and recording EEG data from the Muse devices developed by InteraXon.

### Installation
Install Muse LSL with pip

```
    pip install muselsl

    # for Mac
    brew install labstreaminglayer/tap/lsl

    # for Windows
    conda install -c conda-forge liblsl
```
### Setting up a stream
To print a list of available muses:

```
    muselsl list
```

To connect to a specific Muse you can pass the name of the device as an argument. Device names can be found on the inside of the left earpiece (e.g. Muse-41D2):

```
    muselsl stream --name YOUR_DEVICE_NAME
```

### Working with Streaming Data

Once an LSL stream is created, you have access to the following commands.
The process running the `stream` command must be kept alive in order to maintain the LSL stream. 
These following commands should be run in another terminal or second process

To view data:
```
    muselsl view
```

If the visualization freezes or is laggy, you can also try the alternate version 2 of the viewer. 
```
    muselsl view --version 2
```

To record EEG data into a CSV:
```
    muselsl record --duration 60  
```

## Reference 
> https://github.com/alexandrebarachant/muse-lsl/blob/master/README.md




















