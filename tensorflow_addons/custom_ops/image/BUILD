licenses(["notice"])  # Apache 2.0

package(default_visibility = ["//visibility:public"])

load("@org_tensorflow//tensorflow:tensorflow.bzl", tf_custom_op_library_tf2 = "tf_custom_op_library")

tf_custom_op_library_tf2(
    name = "_distort_image_ops.so",
    srcs = [
        "cc/kernels/adjust_hsv_in_yiq_op.cc",
        "cc/kernels/adjust_hsv_in_yiq_op.h",
        "cc/ops/distort_image_ops.cc",
    ],
    gpu_srcs = [
        "cc/kernels/adjust_hsv_in_yiq_op.h",
        "cc/kernels/adjust_hsv_in_yiq_op_gpu.cu.cc",
    ],
)

tf_custom_op_library_tf2(
    name = "_image_ops.so",
    srcs = [
        "cc/kernels/connected_components.cc",
        "cc/kernels/connected_components.h",
        "cc/kernels/euclidean_distance_transform_op.cc",
        "cc/kernels/euclidean_distance_transform_op.h",
        "cc/ops/image_ops.cc",
    ],
    gpu_srcs = [
        "cc/kernels/euclidean_distance_transform_op.h",
        "cc/kernels/euclidean_distance_transform_op_gpu.cu.cc",
    ],
)

tf_custom_op_library_tf2(
    name = "_resampler_ops.so",
    srcs = [
        "cc/kernels/resampler_ops.cc",
        "cc/kernels/resampler_ops.h",
        "cc/ops/resampler_ops.cc",
    ],
    gpu_srcs = [
        "cc/kernels/resampler_ops.h",
        "cc/kernels/resampler_ops_gpu.cu.cc",
    ],
)
