"""
@generated
cargo-raze crate build file.

DO NOT EDIT! Replaced on runs of cargo-raze
"""

# buildifier: disable=load
load(
    "@io_bazel_rules_rust//rust:rust.bzl",
    "rust_binary",
    "rust_library",
    "rust_test",
)

# buildifier: disable=load
load("@bazel_skylib//lib:selects.bzl", "selects")

package(default_visibility = [
    # Public for visibility by "@raze__crate__version//" targets.
    #
    # Prefer access through "//wasm_bindgen/raze", which limits external
    # visibility to explicit Cargo.toml dependencies.
    "//visibility:public",
])

licenses([
    "notice",  # MIT from expression "MIT OR Apache-2.0"
])

# Generated targets

# buildifier: leave-alone
rust_library(
    name = "remove_dir_all",
    crate_type = "lib",
    deps = [
    ] + selects.with_or({
        # cfg(windows)
        (
            "@io_bazel_rules_rust//rust/platform:i686-pc-windows-gnu",
            "@io_bazel_rules_rust//rust/platform:x86_64-pc-windows-gnu",
        ): [
            "@rules_rust_wasm_bindgen__winapi__0_3_9//:winapi",
        ],
        "//conditions:default": [],
    }),
    srcs = glob(["**/*.rs"]),
    crate_root = "src/lib.rs",
    edition = "2015",
    rustc_flags = [
        "--cap-lints=allow",
    ],
    version = "0.5.3",
    tags = [
        "cargo-raze",
        "manual",
    ],
    crate_features = [
    ],
    aliases = {
    },
)
