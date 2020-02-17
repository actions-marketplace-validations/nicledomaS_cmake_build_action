# Cmake build action

### Example workflow
```yaml
name: C/C++ CI

on: [push]

jobs:
  ubuntu-build:
    runs-on: ubuntu-latest
    steps:
    - name: Checkout
      uses: actions/checkout@v2.0.0
    - name: Build project
      uses: nicledomaS/cmake_build_action@master
      with:
        submodule_update: ON
        run_tests: ON
        unit_test_build: -Dtest=ON
```
