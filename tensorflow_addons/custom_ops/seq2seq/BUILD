licenses(["notice"])  # Apache 2.0

package(default_visibility = ["//visibility:public"])

load("@org_tensorflow//tensorflow:tensorflow.bzl", tf_custom_op_library_tf2 = "tf_custom_op_library")

tf_custom_op_library_tf2(
    name = "_beam_search_ops.so",
    srcs = [
        "cc/kernels/beam_search_ops.cc",
        "cc/kernels/beam_search_ops.h",
        "cc/ops/beam_search_ops.cc",
    ],
    gpu_srcs = [
        "cc/kernels/beam_search_ops.h",
        "cc/kernels/beam_search_ops_gpu.cu.cc",
    ],
)
