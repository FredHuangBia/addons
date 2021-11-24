licenses(["notice"])  # Apache 2.0

package(default_visibility = ["//visibility:public"])

load("@org_tensorflow//tensorflow:tensorflow.bzl", tf_custom_op_library_tf2 = "tf_custom_op_library")

tf_custom_op_library_tf2(
    name = "_skip_gram_ops.so",
    srcs = [
        "cc/kernels/skip_gram_kernels.cc",
        "cc/ops/skip_gram_ops.cc",
    ],
)

tf_custom_op_library_tf2(
    name = "_parse_time_op.so",
    srcs = select({
        "//tensorflow_addons:windows": [],
        "//conditions:default": [
            "cc/kernels/parse_time_kernel.cc",
            "cc/ops/parse_time_op.cc",
        ],
    }),
)
