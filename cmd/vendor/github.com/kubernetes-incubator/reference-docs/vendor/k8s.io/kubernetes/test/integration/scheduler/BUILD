package(default_visibility = ["//visibility:public"])

load(
    "@io_bazel_rules_go//go:def.bzl",
    "go_library",
    "go_test",
)

go_test(
    name = "go_default_test",
    size = "large",
    srcs = [
        "extender_test.go",
        "main_test.go",
        "predicates_test.go",
        "priorities_test.go",
        "scheduler_test.go",
    ],
    importpath = "k8s.io/kubernetes/test/integration/scheduler",
    library = ":go_default_library",
    tags = ["integration"],
    deps = [
        "//vendor/k8s.io/api/core/v1:go_default_library",
        "//vendor/k8s.io/apimachinery/pkg/api/errors:go_default_library",
        "//vendor/k8s.io/apimachinery/pkg/api/resource:go_default_library",
        "//vendor/k8s.io/apimachinery/pkg/apis/meta/v1:go_default_library",
        "//vendor/k8s.io/apimachinery/pkg/util/wait:go_default_library",
        "//vendor/k8s.io/apiserver/pkg/util/feature:go_default_library",
        "//vendor/k8s.io/client-go/informers:go_default_library",
        "//vendor/k8s.io/client-go/kubernetes:go_default_library",
        "//vendor/k8s.io/client-go/kubernetes/typed/core/v1:go_default_library",
        "//vendor/k8s.io/client-go/listers/core/v1:go_default_library",
        "//vendor/k8s.io/client-go/rest:go_default_library",
        "//vendor/k8s.io/client-go/tools/cache:go_default_library",
        "//vendor/k8s.io/client-go/tools/record:go_default_library",
        "//vendor/k8s.io/kubernetes/pkg/api:go_default_library",
        "//vendor/k8s.io/kubernetes/pkg/api/testapi:go_default_library",
        "//vendor/k8s.io/kubernetes/pkg/features:go_default_library",
        "//vendor/k8s.io/kubernetes/plugin/cmd/kube-scheduler/app:go_default_library",
        "//vendor/k8s.io/kubernetes/plugin/cmd/kube-scheduler/app/options:go_default_library",
        "//vendor/k8s.io/kubernetes/plugin/pkg/scheduler:go_default_library",
        "//vendor/k8s.io/kubernetes/plugin/pkg/scheduler/algorithm:go_default_library",
        "//vendor/k8s.io/kubernetes/plugin/pkg/scheduler/algorithmprovider:go_default_library",
        "//vendor/k8s.io/kubernetes/plugin/pkg/scheduler/api:go_default_library",
        "//vendor/k8s.io/kubernetes/plugin/pkg/scheduler/core:go_default_library",
        "//vendor/k8s.io/kubernetes/plugin/pkg/scheduler/factory:go_default_library",
        "//vendor/k8s.io/kubernetes/plugin/pkg/scheduler/schedulercache:go_default_library",
        "//vendor/k8s.io/kubernetes/test/e2e/framework:go_default_library",
        "//vendor/k8s.io/kubernetes/test/integration/framework:go_default_library",
        "//vendor/k8s.io/kubernetes/test/utils:go_default_library",
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

go_library(
    name = "go_default_library",
    srcs = ["util.go"],
    importpath = "k8s.io/kubernetes/test/integration/scheduler",
    deps = [
        "//vendor/k8s.io/api/core/v1:go_default_library",
        "//vendor/k8s.io/apimachinery/pkg/api/errors:go_default_library",
        "//vendor/k8s.io/apimachinery/pkg/api/resource:go_default_library",
        "//vendor/k8s.io/apimachinery/pkg/apis/meta/v1:go_default_library",
        "//vendor/k8s.io/apimachinery/pkg/util/uuid:go_default_library",
        "//vendor/k8s.io/apimachinery/pkg/util/wait:go_default_library",
        "//vendor/k8s.io/client-go/informers:go_default_library",
        "//vendor/k8s.io/client-go/kubernetes:go_default_library",
        "//vendor/k8s.io/client-go/kubernetes/typed/core/v1:go_default_library",
        "//vendor/k8s.io/client-go/listers/core/v1:go_default_library",
        "//vendor/k8s.io/client-go/rest:go_default_library",
        "//vendor/k8s.io/client-go/tools/record:go_default_library",
        "//vendor/k8s.io/kubernetes/pkg/api:go_default_library",
        "//vendor/k8s.io/kubernetes/pkg/api/testapi:go_default_library",
        "//vendor/k8s.io/kubernetes/plugin/pkg/scheduler:go_default_library",
        "//vendor/k8s.io/kubernetes/plugin/pkg/scheduler/algorithmprovider:go_default_library",
        "//vendor/k8s.io/kubernetes/plugin/pkg/scheduler/factory:go_default_library",
        "//vendor/k8s.io/kubernetes/test/integration/framework:go_default_library",
    ],
)
