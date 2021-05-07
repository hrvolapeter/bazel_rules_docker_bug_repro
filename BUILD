load("@io_bazel_rules_docker//container:container.bzl", "container_image")
load("@bazel_tools//tools/build_defs/pkg:pkg.bzl", "pkg_tar")

container_image(
    name = "image",
    base = "@gostatic//image",
    directory = "/specifieddir",
    tars = [
        ":bbb",
    ]
)

pkg_tar(
    name = "bbb",
    strip_prefix = ".",
    srcs = glob(["files/**"]),
)
