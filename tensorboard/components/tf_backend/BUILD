load("//tensorboard/defs:defs.bzl", "tensorboard_webcomponent_library")
load("//tensorboard/defs:web.bzl", "tf_web_library")

package(default_visibility = ["//tensorboard:internal"])

licenses(["notice"])  # Apache 2.0

tf_web_library(
    name = "tf_backend",
    srcs = [
        "backend.ts",
        "baseStore.ts",
        "canceller.ts",
        "environmentStore.ts",
        "experimentsStore.ts",
        "requestManager.ts",
        "router.ts",
        "runsStore.ts",
        "tf-backend.html",
        "tf-backend-polymer.ts",
        "urlPathHelpers.ts",
    ],
    path = "/tf-backend",
    visibility = ["//visibility:public"],
    deps = [
        ":type",
        "//tensorboard/components/tf_imports:lodash",
        "//tensorboard/components/tf_imports:plottable",
        "//tensorboard/components/tf_imports:polymer",
        "//tensorboard/components/vz_sorting",
    ],
)

tf_web_library(
    name = "type",
    srcs = [
        "type.ts",
    ],
    path = "/tf-backend",
)

tensorboard_webcomponent_library(
    name = "legacy",
    srcs = [":tf_backend"],
    destdir = "tf-backend",
    deps = [
        "//tensorboard/components/tf_imports:polymer_lib",
        "//tensorboard/components/tf_imports_google:lib",
        "//tensorboard/components/vz_sorting:legacy",
    ],
)
