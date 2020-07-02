load("@bazel_tools//tools/build_defs/repo:git.bzl", "git_repository") # , "new_git_repository")

git_repository(
    name = "obazl",
    remote = "https://github.com/mobileink/obazl",
    branch = "master",
    # commit = "e848f42ed169f69fd12d1dbacf49d5d6e38dbe15",
    # shallow_since = "1593486114 -0500"
)

load("@obazl//ocaml:deps.bzl",
     "ocaml_configure_tooling",
     "ocaml_register_toolchains")

ocaml_configure_tooling()

ocaml_register_toolchains(installation="host")

