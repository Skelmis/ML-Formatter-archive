ML Formatter
------------

** Moved to: ** https://github.com/ateaspace/ML-Formatter

A simple set of scripts that take act as a middle man for media 
intake during  machine learning pipelines. 

Given input arguments, this program aims to produce
the required output format for specific use cases. 

Currently:
 - DeepSpeech

### Usage

```shell
> python -m formatter
```

To view all arguments
```shell
> python -m formatter --help
usage: __main__.py [-h] [-v | -q] [--dont-shuffle] [--train TRAIN] [--test TEST] [--val VAL] [--parser {deepspeech}] [--media_type {wav}]
                   [--transcript_type {txt}] [--media MEDIA] [--transcript TRANSCRIPT] [--output OUTPUT]

Given a set of media, create and output to the required spec of certain ML programs

optional arguments:
  -h, --help            show this help message and exit
  -v, --verbose
  -q, --quiet
  --dont-shuffle        Don't shuffle before splitting into runs
  --train TRAIN         Training part of train/test/val split. Out of 1
  --test TEST           Testing part of train/test/val split. Out of 1
  --val VAL             Validation part of train/test/val split. Out of 1
  --parser {deepspeech}
                        The format you wish to receive as output
  --media_type {wav}    The file extension of media files
  --transcript_type {txt}
                        The file extension of text transcript files
  --media MEDIA         Path to the directory containing media files
  --transcript TRANSCRIPT
                        Path to files containing text transcripts
  --output OUTPUT       Path to directory to use as an output folder
```

Example usage
```shell
> python -m formatter --media ./media --transcript ./transcripts --output ./output --verbose
```
