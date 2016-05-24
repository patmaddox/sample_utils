## Usage

* `aplay`  – looks for a file called `out.wav` and plays it
* `keepit` - moves `out.wav` to a uniquely-named file under `keepers/`
* `gospectral` and `gotime` – these configure the `CDP_OVERWRITE_FILE` environment
variable which CDP uses to allow overwriting a single filename. If you're
going to run a bunch of spectral commands, you may want to use `gospectral`
beforehand. These should be run with `$()` to execute their contents e.g.
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
