load("@io_bazel_rules_kotlin//kotlin:jvm.bzl", "kt_jvm_binary")

package(default_visibility = ["//visibility:private"])

licenses(["notice"])

kt_jvm_binary(
    name = "run_project",
    srcs = ["main/Main.kt"],
    # This javaagent is needed to install
    # `kotlinx.coroutines.debug.internal.DebugProbesImpl` which is needed for
    # debugging coroutines.
    jvm_flags = ["-javaagent:$(location @kotlinx_coroutines//jar)"],
    main_class = "main.Main",
    deps = ["@kotlinx_coroutines//jar"],
)
