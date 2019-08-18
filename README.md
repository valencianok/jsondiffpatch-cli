# jsondiffpatch-cli
A Command Line wrapper for using the jsondiffpatch library

## How to use it

```cmd
jsondiffpatch-cli OPERATION A.json B.json OUTPUT.json
```
It requires the operation name and at least two json file paths. The third path is the output.

### diff
- File A: is the left side of the diff
- File B: is the right side of the diff
- Output: where the diff will be stored
```cmd
jsondiffpatch-cli diff left.json right.json left-right.diff.json
```

### patch
- File A: is the base file to apply the patch (in our example would be the left)
- File B: is the diff file to apply as patch
- Output: the result json after applying the patch
```cmd
jsondiffpatch-cli patch left.json left-right.diff.json.json output-left.json
```

### unpatch
- File A: is the base file to apply the patch (in our example would be the right)
- File B: is the diff file to apply as patch
- Output: the result json after applying the patch
```cmd
jsondiffpatch-cli unpatch right.json left-right.diff.json.json output-right.json
```

## Credits
This tool uses the [jsondiffpatch](https://github.com/benjamine/jsondiffpatch) library developed by Benjamin Eidelman