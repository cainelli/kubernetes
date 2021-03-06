package(default_visibility = ["//visibility:public"])

licenses(["notice"])

load(
    "@io_bazel_rules_go//go:def.bzl",
    "go_library",
    "go_test",
)

go_library(
    name = "go_default_library",
    srcs = [
        "thirdparty.go",
        "tprregistration_controller.go",
    ],
    tags = ["automanaged"],
    deps = [
        "//pkg/api:go_default_library",
        "//pkg/apis/extensions:go_default_library",
        "//pkg/client/informers/informers_generated/internalversion/extensions/internalversion:go_default_library",
        "//pkg/client/listers/extensions/internalversion:go_default_library",
        "//pkg/controller:go_default_library",
        "//pkg/registry/extensions/rest:go_default_library",
        "//pkg/registry/extensions/thirdpartyresourcedata:go_default_library",
        "//pkg/registry/extensions/thirdpartyresourcedata/storage:go_default_library",
        "//vendor:github.com/golang/glog",
        "//vendor:k8s.io/apimachinery/pkg/api/meta",
        "//vendor:k8s.io/apimachinery/pkg/apis/meta/v1",
        "//vendor:k8s.io/apimachinery/pkg/labels",
        "//vendor:k8s.io/apimachinery/pkg/runtime",
        "//vendor:k8s.io/apimachinery/pkg/runtime/schema",
        "//vendor:k8s.io/apimachinery/pkg/util/runtime",
        "//vendor:k8s.io/apimachinery/pkg/util/wait",
        "//vendor:k8s.io/apiserver/pkg/endpoints",
        "//vendor:k8s.io/apiserver/pkg/endpoints/handlers",
        "//vendor:k8s.io/apiserver/pkg/endpoints/request",
        "//vendor:k8s.io/apiserver/pkg/registry/generic",
        "//vendor:k8s.io/apiserver/pkg/registry/rest",
        "//vendor:k8s.io/apiserver/pkg/server",
        "//vendor:k8s.io/apiserver/pkg/server/storage",
        "//vendor:k8s.io/apiserver/pkg/storage/storagebackend",
        "//vendor:k8s.io/client-go/tools/cache",
        "//vendor:k8s.io/client-go/util/workqueue",
        "//vendor:k8s.io/kube-aggregator/pkg/apis/apiregistration",
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

go_test(
    name = "go_default_test",
    srcs = ["tprregistration_controller_test.go"],
    library = ":go_default_library",
    tags = ["automanaged"],
    deps = [
        "//pkg/apis/extensions:go_default_library",
        "//pkg/client/listers/extensions/internalversion:go_default_library",
        "//vendor:k8s.io/apimachinery/pkg/apis/meta/v1",
        "//vendor:k8s.io/apimachinery/pkg/runtime/schema",
        "//vendor:k8s.io/client-go/tools/cache",
        "//vendor:k8s.io/client-go/util/workqueue",
        "//vendor:k8s.io/kube-aggregator/pkg/apis/apiregistration",
    ],
)
