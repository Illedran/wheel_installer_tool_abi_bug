workspace(name = "python_crosscompile")

load("@bazel_tools//tools/build_defs/repo:http.bzl", "http_archive")

# Python

# Use 0.29.0 over 0.31.0 to show regression.
#
# http_archive(
#     name = "rules_python",
#     sha256 = "d71d2c67e0bce986e1c5a7731b4693226867c45bfe0b7c5e0067228a536fc580",
#     strip_prefix = "rules_python-0.29.0",
#     url = "https://github.com/bazelbuild/rules_python/releases/download/0.29.0/rules_python-0.29.0.tar.gz",
# )

http_archive(
    name = "rules_python",
    sha256 = "c68bdc4fbec25de5b5493b8819cfc877c4ea299c0dcb15c244c5a00208cde311",
    strip_prefix = "rules_python-0.31.0",
    url = "https://github.com/bazelbuild/rules_python/releases/download/0.31.0/rules_python-0.31.0.tar.gz",
)

load("@rules_python//python:repositories.bzl", "py_repositories", "python_register_toolchains")

py_repositories()

python_register_toolchains(
    name = "python_3_12",
    python_version = "3.12",
)


load("@python_3_12//:defs.bzl", "interpreter")
load("@rules_python//python:pip.bzl", "pip_parse")

pip_parse(
    name = "pypi",
    python_interpreter_target = interpreter,
    requirements_lock = "@//:requirements.txt",
    download_only = True,
    experimental_target_platforms = ["linux_x86_64"],
    extra_pip_args = [
        "--platform", "manylinux_2_17_x86_64",
        "--platform", "manylinux2010_x86_64",  # for libclang
    ],
)

load("@pypi//:requirements.bzl", "install_deps")
install_deps()