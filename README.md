Produces version suffix based on the current branch - `${{ github.ref_name }}`.

```yaml
on:
  push:
    
jobs:
  print-suffix:
    runs-on: ubuntu-latest
    steps:
      - id: suffix
        uses: astorDev/suffix/@v1.0
      
      # branch:feature/one => Suffix is 'feature-one'
      # branch:"main" => Suffix is ''
      - run: echo "Suffix is '${{ steps.suffix.outputs.suffix }}'"
```

This action is a showcase from a [Versy](https://github.com/astorDev/versy) project.