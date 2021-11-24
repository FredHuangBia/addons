licenses(["notice"])  # Apache 2.0

package(default_visibility = ["//visibility:public"])

load("@org_tensorflow//tensorflow:tensorflow.bzl", tf_custom_op_library_tf2 = "tf_custom_op_library")

tf_custom_op_library_tf2(
    name = "_correlation_cost_ops.so",
    srcs = [
        "cc/kernels/correlation_cost_op.cc",
        "cc/kernels/correlation_cost_op.h",
        "cc/ops/correlation_cost_op.cc",
    ],
    cuda_deps = [
        "@cub_archive//:cub",
    ],
    gpu_srcs = [
        "cc/kernels/correlation_cost_op.h",
        "cc/kernels/correlation_cost_op_gpu.cu.cc",
    ],
)

tf_custom_op_library_tf2(
    name = "_embedding_bag_ops.so",
    srcs = [
        "cc/kernels/embedding_bag_ops.cc",
        "cc/kernels/embedding_bag_ops.h",
        "cc/ops/embedding_bag_ops.cc",
    ],
    gpu_srcs = [
        "cc/kernels/embedding_bag_ops.h",
        "cc/kernels/embedding_bag_ops_gpu.cu.cc",
        "cc/kernels/embedding_bag_backward_kernels.cu.cc",
    ],
)
