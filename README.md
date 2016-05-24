## Usage

* `aplay`  – looks for a file called `out.wav` and plays it
* `keepit` - moves `out.wav` to a uniquely-named file under `keepers/`

### Filename utils

* `wavout` and `anaout` – can be used as outfile arguments, to overwrite the
temporary outfile if desired (CDP doesn't overwrite files)
* `gospectral` and `gotime` – alternate options to `wavout` and `anaout`.
`gospectral` and `gotime` configure the `CDP_OVERWRITE_FILE` environment
variable which CDP uses to allow overwriting a single filename. If you're
going to run a bunch of spectral commands, you may want to use `gospectral`
beforehand.

The filename utils should be run with `$()` to execute their contents e.g.
`$(gospectral)`.

### Example workflow

1. Start `aplay`
2. Use [CDP](http://www.composersdesktop.com) to create a sample via the command-line.
e.g. `rm -f out.wav && modify revecho 1 whoa.wav out.wav 52 .90 0.71 16`
3. Do you like it? `keepit`

## Dependencies

```
brew install sox fswatch
```

## Tips

* To stop playing audio: ctrl-c
* To kill the auto-player: ctrl-z followed by `kill %`
