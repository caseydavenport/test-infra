package(default_visibility = ["//visibility:public"])

licenses(["notice"])

load(
    "@io_bazel_rules_go//go:def.bzl",
    "go_library",
    "go_test",
)

go_test(
    name = "go_default_test",
    srcs = ["update_config_test.go"],
    library = ":go_default_library",
    tags = ["automanaged"],
    deps = [
        "//prow/github:go_default_library",
        "//prow/github/fakegithub:go_default_library",
        "//prow/kube:go_default_library",
        "//vendor:github.com/Sirupsen/logrus",
    ],
)

go_library(
    name = "go_default_library",
    srcs = ["update_config.go"],
    tags = ["automanaged"],
    deps = [
        "//prow/github:go_default_library",
        "//prow/kube:go_default_library",
        "//prow/plugins:go_default_library",
        "//vendor:github.com/Sirupsen/logrus",
    ],
)

filegroup(
    name = "package-srcs",
    srcs = glob(["**"]),
    tags = ["automanaged"],
    visibility = ["//visibility:private"],
)

filegroup(
    name = "all-srcs",
    srcs = [":package-srcs"],
    tags = ["automanaged"],
)
