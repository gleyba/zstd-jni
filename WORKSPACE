load("@bazel_tools//tools/build_defs/repo:http.bzl", "http_archive")

# Rules JVM external

rules_jvm_external_version = "4.2"

rules_jvm_external_sha = "cd1a77b7b02e8e008439ca76fd34f5b07aecb8c752961f9640dea15e9e5ba1ca"

http_archive(
    name = "rules_jvm_external",
    sha256 = rules_jvm_external_sha,
    strip_prefix = "rules_jvm_external-%s" % rules_jvm_external_version,
    url = "https://github.com/bazelbuild/rules_jvm_external/archive/%s.zip" % rules_jvm_external_version,
)

# Maven deps

load("@rules_jvm_external//:defs.bzl", "maven_install")

maven_install(
    artifacts = [
        "com.google.protobuf:protobuf-java:3.21.1",
        "com.google.guava:guava:31.0.1-jre",
    ],
    repositories = [
        "https://repo1.maven.org/maven2",
    ],
)