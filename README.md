Leesp!
=====

Wrote myself a Scheme in 48 hours, fancy that... (from the book of a remarkably similar name!).

Thanks to @bodil for the inspiration to try my hand at building a Lisp, and thank you to Jonathan Tang and everyone that has contributed to the WikiBook in what ever capacity.

To try your own hand at this head on over to [the book](https://en.wikibooks.org/wiki/Write_Yourself_a_Scheme_in_48_Hours) and get cracking.

Binary for OSX is available on the Releases page. Compiled using: ```The Glorious Glasgow Haskell Compilation System, version 7.6.3``` on OSX 10.8.

Other platforms may happily compile for themselves (as I'm too lazy for VMs/Docker/Vagrant right now). The following compiler flags should suffice:

```
ghc --make -package parsec -XExistentialQuantification -o leespOmg main.hs
```

Once you have a happy binary, you can either use the REPL (YES IT HAS A REPL! Omg, you have no idea how exciting it was to build a language that has it's own REPL... seriously... no idea) *ahem* by just running the binary thus:

```
./leespOmg
```

Or alternately you can pass strings directly in for evaluation, however this process is a little weird because you have to escape everything like a champ and it becomes insufferable very quickly when dealing with strings:

```
./leespOmg "(cons \"foo\" `(bar #\b)"
```

car, cdr, and friends are there. As well as _cons_, _if_, _cond_, _case_, a whole bunch of mathematical operations, comparison functions, atoms, and a handful of string functions: _string-ref_, _string-set!_, _string-length_.
