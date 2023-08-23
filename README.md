# pypi-deployment
A reusable github action to package, deploy and and check code to PyPi & TestPyPi

## Basic usage

Please see [action.yaml()] for all details.

The following options can be passed:

1. `token` (required): The relevant PyPi or TestPyPi upload token for the package.
2. `test_submission`: Bool, if true the package will be uploaded to TestPyPi instead of PyPi (default: false)
3. `wheels`: Bool, if true wheels will be created and uploaded (default: false)
4. `tests`: Bool, if true there will be an attempt to pull down the newly uploaded package and run tests. Please note this assumes testing via `pytest --pyargs inputs.package_name` (default: false)
5. `package_name`: The name of the package on PyPi. Note that this is only used for testing post-upload (default: '')

### Example

TODO: add example here

## Note
This currently only support pure Python packages. Future work will switch this action to using cibuildwheels.
