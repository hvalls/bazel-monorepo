load("@build_bazel_rules_nodejs//:index.bzl", "nodejs_binary")
load("@npm//mocha:index.bzl", "mocha_test")

nodejs_binary(
    name = "service",
    entry_point = "server.js",
    data = [
      "@npm//express",
    ]
)

mocha_test(
    name = "unit_tests",
    args = ["**/*.spec.js"],
    data = glob(["*.spec.js"])
)

