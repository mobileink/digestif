load("@bazel_tools//tools/build_defs/repo:git.bzl", "git_repository") # , "new_git_repository")

git_repository(
    name = "obazl",
    branch = "master",
    # commit = "214d4bb0e4b88f2949bf590070c0faccb097fc79",
    remote = "https://github.com/mobileink/obazl",
    # shallow_since = "1592257503 -0500"
)

load("@obazl//ocaml:deps.bzl",
     "ocaml_configure_tooling",
     "ocaml_register_toolchains")

ocaml_configure_tooling()

ocaml_register_toolchains(installation="host")

