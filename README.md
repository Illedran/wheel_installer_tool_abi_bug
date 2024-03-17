# wheel_installer_tool_abi_bug

`$ bazel build //src:hello_world_with_tornado`

```
INFO: Repository pypi_tornado instantiated at:
  /home/illedran/proj/wheel_installer_tool_abi_bug/WORKSPACE:38:13: in <toplevel>
  /home/illedran/.cache/bazel/_bazel_illedran/527668b0d651ad7c51390aa36afa823c/external/pypi/requirements.bzl:77:20: in install_deps
Repository rule whl_library defined at:
  /home/illedran/.cache/bazel/_bazel_illedran/527668b0d651ad7c51390aa36afa823c/external/rules_python/python/pip_install/pip_repository.bzl:932:30: in <toplevel>
ERROR: An error occurred during the fetch of repository 'pypi_tornado':
   Traceback (most recent call last):
        File "/home/illedran/.cache/bazel/_bazel_illedran/527668b0d651ad7c51390aa36afa823c/external/rules_python/python/pip_install/pip_repository.bzl", line 803, column 31, in _whl_library_impl
                repo_utils.execute_checked(
        File "/home/illedran/.cache/bazel/_bazel_illedran/527668b0d651ad7c51390aa36afa823c/external/rules_python/python/private/repo_utils.bzl", line 145, column 29, in _execute_checked
                return _execute_internal(fail_on_error = True, *args, **kwargs)
        File "/home/illedran/.cache/bazel/_bazel_illedran/527668b0d651ad7c51390aa36afa823c/external/rules_python/python/private/repo_utils.bzl", line 86, column 13, in _execute_internal
                fail((
Error in fail: repo.execute: whl_library.ExtractWheel(pypi_tornado, /home/illedran/.cache/bazel/_bazel_illedran/527668b0d651ad7c51390aa36afa823c/external/pypi_tornado/tornado-6.4-cp38-abi3-manylinux_2_5_x86_64.manylinux1_x86_64.manylinux_2_17_x86_64.manylinux2014_x86_64.whl): end: failure:
  command: /home/illedran/.cache/bazel/_bazel_illedran/527668b0d651ad7c51390aa36afa823c/external/python_3_12_x86_64-unknown-linux-gnu/bin/python3 -m python.pip_install.tools.wheel_installer.wheel_installer --requirement tornado==6.4 --isolated --extra_pip_args "{\"arg\":[]}" --download_only --pip_data_exclude "{\"arg\":[]}" --environment "{\"arg\":{}}" --whl-file /home/illedran/.cache/bazel/_bazel_illedran/527668b0d651ad7c51390aa36afa823c/external/pypi_tornado/tornado-6.4-cp38-abi3-manylinux_2_5_x86_64.manylinux1_x86_64.manylinux_2_17_x86_64.manylinux2014_x86_64.whl --platform=abi3_linux_x86_64
  return code: 1
  working dir: <default: /home/illedran/.cache/bazel/_bazel_illedran/527668b0d651ad7c51390aa36afa823c/external/pypi_tornado>
  timeout: 600
  environment:
PYTHONPATH="/home/illedran/.cache/bazel/_bazel_illedran/527668b0d651ad7c51390aa36afa823c/external/rules_python:/home/illedran/.cache/bazel/_bazel_illedran/527668b0d651ad7c51390aa36afa823c/external/pypi__build:/home/illedran/.cache/bazel/_bazel_illedran/527668b0d651ad7c51390aa36afa823c/external/pypi__click:/home/illedran/.cache/bazel/_bazel_illedran/527668b0d651ad7c51390aa36afa823c/external/pypi__colorama:/home/illedran/.cache/bazel/_bazel_illedran/527668b0d651ad7c51390aa36afa823c/external/pypi__importlib_metadata:/home/illedran/.cache/bazel/_bazel_illedran/527668b0d651ad7c51390aa36afa823c/external/pypi__installer:/home/illedran/.cache/bazel/_bazel_illedran/527668b0d651ad7c51390aa36afa823c/external/pypi__more_itertools:/home/illedran/.cache/bazel/_bazel_illedran/527668b0d651ad7c51390aa36afa823c/external/pypi__packaging:/home/illedran/.cache/bazel/_bazel_illedran/527668b0d651ad7c51390aa36afa823c/external/pypi__pep517:/home/illedran/.cache/bazel/_bazel_illedran/527668b0d651ad7c51390aa36afa823c/external/pypi__pip:/home/illedran/.cache/bazel/_bazel_illedran/527668b0d651ad7c51390aa36afa823c/external/pypi__pip_tools:/home/illedran/.cache/bazel/_bazel_illedran/527668b0d651ad7c51390aa36afa823c/external/pypi__pyproject_hooks:/home/illedran/.cache/bazel/_bazel_illedran/527668b0d651ad7c51390aa36afa823c/external/pypi__setuptools:/home/illedran/.cache/bazel/_bazel_illedran/527668b0d651ad7c51390aa36afa823c/external/pypi__tomli:/home/illedran/.cache/bazel/_bazel_illedran/527668b0d651ad7c51390aa36afa823c/external/pypi__wheel:/home/illedran/.cache/bazel/_bazel_illedran/527668b0d651ad7c51390aa36afa823c/external/pypi__zipp"
CPPFLAGS=""
<stdout empty>
===== stderr start =====
Traceback (most recent call last):
  File "<frozen runpy>", line 198, in _run_module_as_main
  File "<frozen runpy>", line 88, in _run_code
  File "/home/illedran/.cache/bazel/_bazel_illedran/527668b0d651ad7c51390aa36afa823c/external/rules_python/python/pip_install/tools/wheel_installer/wheel_installer.py", line 205, in <module>
    main()
  File "/home/illedran/.cache/bazel/_bazel_illedran/527668b0d651ad7c51390aa36afa823c/external/rules_python/python/pip_install/tools/wheel_installer/wheel_installer.py", line 149, in main
    args = arguments.parser(description=__doc__).parse_args()
           ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
  File "/home/illedran/.cache/bazel/_bazel_illedran/527668b0d651ad7c51390aa36afa823c/external/python_3_12_x86_64-unknown-linux-gnu/lib/python3.12/argparse.py", line 1891, in parse_args
    args, argv = self.parse_known_args(args, namespace)
                 ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
  File "/home/illedran/.cache/bazel/_bazel_illedran/527668b0d651ad7c51390aa36afa823c/external/python_3_12_x86_64-unknown-linux-gnu/lib/python3.12/argparse.py", line 1924, in parse_known_args
    namespace, args = self._parse_known_args(args, namespace)
                      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
  File "/home/illedran/.cache/bazel/_bazel_illedran/527668b0d651ad7c51390aa36afa823c/external/python_3_12_x86_64-unknown-linux-gnu/lib/python3.12/argparse.py", line 2136, in _parse_known_args
    start_index = consume_optional(start_index)
                  ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
  File "/home/illedran/.cache/bazel/_bazel_illedran/527668b0d651ad7c51390aa36afa823c/external/python_3_12_x86_64-unknown-linux-gnu/lib/python3.12/argparse.py", line 2076, in consume_optional
    take_action(action, args, option_string)
  File "/home/illedran/.cache/bazel/_bazel_illedran/527668b0d651ad7c51390aa36afa823c/external/python_3_12_x86_64-unknown-linux-gnu/lib/python3.12/argparse.py", line 1984, in take_action
    argument_values = self._get_values(action, argument_strings)
                      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
  File "/home/illedran/.cache/bazel/_bazel_illedran/527668b0d651ad7c51390aa36afa823c/external/python_3_12_x86_64-unknown-linux-gnu/lib/python3.12/argparse.py", line 2522, in _get_values
    value = self._get_value(action, arg_string)
            ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
  File "/home/illedran/.cache/bazel/_bazel_illedran/527668b0d651ad7c51390aa36afa823c/external/python_3_12_x86_64-unknown-linux-gnu/lib/python3.12/argparse.py", line 2555, in _get_value
    result = type_func(arg_string)
             ^^^^^^^^^^^^^^^^^^^^^
  File "/home/illedran/.cache/bazel/_bazel_illedran/527668b0d651ad7c51390aa36afa823c/external/rules_python/python/pip_install/tools/wheel_installer/wheel.py", line 205, in from_string
    os=OS[os] if os != "*" else None,
       ~~^^^^
  File "/home/illedran/.cache/bazel/_bazel_illedran/527668b0d651ad7c51390aa36afa823c/external/python_3_12_x86_64-unknown-linux-gnu/lib/python3.12/enum.py", line 801, in __getitem__
    return cls._member_map_[name]
           ~~~~~~~~~~~~~~~~^^^^^^
KeyError: 'abi3'
===== stderr end =====
```

`$ bazel build //src:hello_world_with_libclang`

```
INFO: Repository pypi_libclang instantiated at:
  /home/illedran/proj/wheel_installer_tool_abi_bug/WORKSPACE:38:13: in <toplevel>
  /home/illedran/.cache/bazel/_bazel_illedran/527668b0d651ad7c51390aa36afa823c/external/pypi/requirements.bzl:77:20: in install_deps
Repository rule whl_library defined at:
  /home/illedran/.cache/bazel/_bazel_illedran/527668b0d651ad7c51390aa36afa823c/external/rules_python/python/pip_install/pip_repository.bzl:932:30: in <toplevel>
ERROR: An error occurred during the fetch of repository 'pypi_libclang':
   Traceback (most recent call last):
        File "/home/illedran/.cache/bazel/_bazel_illedran/527668b0d651ad7c51390aa36afa823c/external/rules_python/python/pip_install/pip_repository.bzl", line 803, column 31, in _whl_library_impl
                repo_utils.execute_checked(
        File "/home/illedran/.cache/bazel/_bazel_illedran/527668b0d651ad7c51390aa36afa823c/external/rules_python/python/private/repo_utils.bzl", line 145, column 29, in _execute_checked
                return _execute_internal(fail_on_error = True, *args, **kwargs)
        File "/home/illedran/.cache/bazel/_bazel_illedran/527668b0d651ad7c51390aa36afa823c/external/rules_python/python/private/repo_utils.bzl", line 86, column 13, in _execute_internal
                fail((
Error in fail: repo.execute: whl_library.ExtractWheel(pypi_libclang, /home/illedran/.cache/bazel/_bazel_illedran/527668b0d651ad7c51390aa36afa823c/external/pypi_libclang/libclang-17.0.6-py2.py3-none-manylinux2010_x86_64.whl): end: failure:
  command: /home/illedran/.cache/bazel/_bazel_illedran/527668b0d651ad7c51390aa36afa823c/external/python_3_12_x86_64-unknown-linux-gnu/bin/python3 -m python.pip_install.tools.wheel_installer.wheel_installer --requirement libclang==17.0.6 --isolated --extra_pip_args "{\"arg\":[]}" --download_only --pip_data_exclude "{\"arg\":[]}" --environment "{\"arg\":{}}" --whl-file /home/illedran/.cache/bazel/_bazel_illedran/527668b0d651ad7c51390aa36afa823c/external/pypi_libclang/libclang-17.0.6-py2.py3-none-manylinux2010_x86_64.whl --platform=none_linux_x86_64
  return code: 1
  working dir: <default: /home/illedran/.cache/bazel/_bazel_illedran/527668b0d651ad7c51390aa36afa823c/external/pypi_libclang>
  timeout: 600
  environment:
PYTHONPATH="/home/illedran/.cache/bazel/_bazel_illedran/527668b0d651ad7c51390aa36afa823c/external/rules_python:/home/illedran/.cache/bazel/_bazel_illedran/527668b0d651ad7c51390aa36afa823c/external/pypi__build:/home/illedran/.cache/bazel/_bazel_illedran/527668b0d651ad7c51390aa36afa823c/external/pypi__click:/home/illedran/.cache/bazel/_bazel_illedran/527668b0d651ad7c51390aa36afa823c/external/pypi__colorama:/home/illedran/.cache/bazel/_bazel_illedran/527668b0d651ad7c51390aa36afa823c/external/pypi__importlib_metadata:/home/illedran/.cache/bazel/_bazel_illedran/527668b0d651ad7c51390aa36afa823c/external/pypi__installer:/home/illedran/.cache/bazel/_bazel_illedran/527668b0d651ad7c51390aa36afa823c/external/pypi__more_itertools:/home/illedran/.cache/bazel/_bazel_illedran/527668b0d651ad7c51390aa36afa823c/external/pypi__packaging:/home/illedran/.cache/bazel/_bazel_illedran/527668b0d651ad7c51390aa36afa823c/external/pypi__pep517:/home/illedran/.cache/bazel/_bazel_illedran/527668b0d651ad7c51390aa36afa823c/external/pypi__pip:/home/illedran/.cache/bazel/_bazel_illedran/527668b0d651ad7c51390aa36afa823c/external/pypi__pip_tools:/home/illedran/.cache/bazel/_bazel_illedran/527668b0d651ad7c51390aa36afa823c/external/pypi__pyproject_hooks:/home/illedran/.cache/bazel/_bazel_illedran/527668b0d651ad7c51390aa36afa823c/external/pypi__setuptools:/home/illedran/.cache/bazel/_bazel_illedran/527668b0d651ad7c51390aa36afa823c/external/pypi__tomli:/home/illedran/.cache/bazel/_bazel_illedran/527668b0d651ad7c51390aa36afa823c/external/pypi__wheel:/home/illedran/.cache/bazel/_bazel_illedran/527668b0d651ad7c51390aa36afa823c/external/pypi__zipp"
CPPFLAGS=""
<stdout empty>
===== stderr start =====
Traceback (most recent call last):
  File "<frozen runpy>", line 198, in _run_module_as_main
  File "<frozen runpy>", line 88, in _run_code
  File "/home/illedran/.cache/bazel/_bazel_illedran/527668b0d651ad7c51390aa36afa823c/external/rules_python/python/pip_install/tools/wheel_installer/wheel_installer.py", line 205, in <module>
    main()
  File "/home/illedran/.cache/bazel/_bazel_illedran/527668b0d651ad7c51390aa36afa823c/external/rules_python/python/pip_install/tools/wheel_installer/wheel_installer.py", line 149, in main
    args = arguments.parser(description=__doc__).parse_args()
           ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
  File "/home/illedran/.cache/bazel/_bazel_illedran/527668b0d651ad7c51390aa36afa823c/external/python_3_12_x86_64-unknown-linux-gnu/lib/python3.12/argparse.py", line 1891, in parse_args
    args, argv = self.parse_known_args(args, namespace)
                 ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
  File "/home/illedran/.cache/bazel/_bazel_illedran/527668b0d651ad7c51390aa36afa823c/external/python_3_12_x86_64-unknown-linux-gnu/lib/python3.12/argparse.py", line 1924, in parse_known_args
    namespace, args = self._parse_known_args(args, namespace)
                      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
  File "/home/illedran/.cache/bazel/_bazel_illedran/527668b0d651ad7c51390aa36afa823c/external/python_3_12_x86_64-unknown-linux-gnu/lib/python3.12/argparse.py", line 2136, in _parse_known_args
    start_index = consume_optional(start_index)
                  ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
  File "/home/illedran/.cache/bazel/_bazel_illedran/527668b0d651ad7c51390aa36afa823c/external/python_3_12_x86_64-unknown-linux-gnu/lib/python3.12/argparse.py", line 2076, in consume_optional
    take_action(action, args, option_string)
  File "/home/illedran/.cache/bazel/_bazel_illedran/527668b0d651ad7c51390aa36afa823c/external/python_3_12_x86_64-unknown-linux-gnu/lib/python3.12/argparse.py", line 1984, in take_action
    argument_values = self._get_values(action, argument_strings)
                      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
  File "/home/illedran/.cache/bazel/_bazel_illedran/527668b0d651ad7c51390aa36afa823c/external/python_3_12_x86_64-unknown-linux-gnu/lib/python3.12/argparse.py", line 2522, in _get_values
    value = self._get_value(action, arg_string)
            ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
  File "/home/illedran/.cache/bazel/_bazel_illedran/527668b0d651ad7c51390aa36afa823c/external/python_3_12_x86_64-unknown-linux-gnu/lib/python3.12/argparse.py", line 2555, in _get_value
    result = type_func(arg_string)
             ^^^^^^^^^^^^^^^^^^^^^
  File "/home/illedran/.cache/bazel/_bazel_illedran/527668b0d651ad7c51390aa36afa823c/external/rules_python/python/pip_install/tools/wheel_installer/wheel.py", line 205, in from_string
    os=OS[os] if os != "*" else None,
       ~~^^^^
  File "/home/illedran/.cache/bazel/_bazel_illedran/527668b0d651ad7c51390aa36afa823c/external/python_3_12_x86_64-unknown-linux-gnu/lib/python3.12/enum.py", line 801, in __getitem__
    return cls._member_map_[name]
           ~~~~~~~~~~~~~~~~^^^^^^
KeyError: 'none'
===== stderr end =====
```