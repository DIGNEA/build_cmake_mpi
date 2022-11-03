
# Github Action for CMake and MPI projects

Github Action template for building the Turing Optimisation Framework.


[![MIT License](https://img.shields.io/apm/l/atomic-design-ui.svg?)](https://github.com/tterb/atomic-design-ui/blob/master/LICENSEs)


## Authors

- [@amarrerod](https://www.github.com/amarrerod)


## Usage/Examples

```yaml
name: Build

on:
  push:
    branches: "**"
  pull_request:

env:
  # Customize the CMake build type here (Release, Debug, RelWithDebInfo, etc.)
  BUILD_TYPE: Release

jobs:
  build:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v2
      
      - name: Build Turing
        uses: dignea/build_cmake@master
        with:
          variant: env.BUILD_TYPE   
```

