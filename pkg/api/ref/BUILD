package(default_visibility = ["//visibility:public"])

licenses(["notice"])

load(
    "@io_bazel_rules_go//go:def.bzl",
    "go_library",
    "go_test",
)

go_test(
    name = "go_default_test",
    srcs = ["ref_test.go"],
    library = ":go_default_library",
    tags = ["automanaged"],
    deps = [
        "//pkg/api:go_default_library",
        "//vendor:k8s.io/apimachinery/pkg/apis/meta/v1",
        "//vendor:k8s.io/apimachinery/pkg/runtime",
        "//vendor:k8s.io/apimachinery/pkg/runtime/schema",
    ],
)

go_library(
    name = "go_default_library",
    srcs = ["ref.go"],
    tags = ["automanaged"],
    deps = [
        "//pkg/api:go_default_library",
        "//vendor:k8s.io/apimachinery/pkg/api/meta",
        "//vendor:k8s.io/apimachinery/pkg/runtime",
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
