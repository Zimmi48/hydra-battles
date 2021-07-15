# Snippets coq+rst

The script `extract_snippets.py` extract snippets block in coq+rst files.\
This script has been developed in python3.9 and use [alectryon](https://github.com/cpitclaudel/alectryon),
to transform "coq+rst" to "latex" file.

###### Note (01/07/2021)
Please use the branch [rst+latex](https://github.com/cpitclaudel/alectryon/tree/rst+latex) in alectryon projet.
And install this alectryon version with:
```shell
~/alectryon $ pip install .
```

## Snippet Block
A snippet blocs is a block formed by this template:
```coq
(* begin snippet NAME *)
    ...
(* end snippet NAME *)
```

## Script
The script has been developed in python3.9.

The script take coq file, extract snippets blocks, and make directory with name of coq file. 
Make latex files with name of snippets, in directory.
Now you can include your snippet file in your main latex file (using `\input{foo/snippet1}` in LaTeX).

## Usage
```shell
$ python extract_snippets.py foo.v
$ ls -l foo/
snippet1.tex  snippet2.tex
```

For more informations do `python extract_snippets -h`
