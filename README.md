# pypi-deployment
A reusable github action to package, deploy and and check code to PyPi & TestPyPi

## Basic usage

Please see [action.yaml()] for all details.

The following options can be passed:

1. `test_submission`: Bool, if true the package will be uploaded to TestPyPi instead of PyPi (default: false)
2. `wheels`: Bool, if true wheels will be created and uploaded (default: true)
3. `tests`: Bool, if true there will be an attempt to pull down the newly uploaded package and run tests. Please note this assumes testing via `pytest --pyargs inputs.package_name` (default: true)
4. `package_name`: Name of package on PyPi, only needed if testing package post-upload. Used for pip installing (default: 'MDAnalysis')
5. `module_name`: Name of package directory, only needed if testing package post-upload. Used for pytest pyargs. If unset will use `package_name` (default: null)

### Example

An example of how to use this workflow can be seen in [this action file](https://github.com/MDAnalysis/mda-xdrlib/blob/main/.github/workflows/deploy.yaml).

## Note
This currently only support pure Python packages. Future work will switch this action to using cibuildwheels.
