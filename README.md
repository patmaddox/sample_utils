## Usage

* `aplay`  – looks for a file called `out.wav` and plays it
* `keepit` - moves `out.wav` to a uniquely-named file under `keepers/`

## Dependencies

```
brew install sox fswatch
```

## Tip

* To stop playing audio: ctrl-c
* To kill the auto-player: ctrl-z followed by `kill %`
