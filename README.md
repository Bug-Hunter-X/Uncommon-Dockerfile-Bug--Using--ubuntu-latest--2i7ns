# Uncommon Dockerfile Bug: Using `ubuntu:latest`

This example demonstrates the issue of using `ubuntu:latest` in a Dockerfile. This tag pulls the latest version of Ubuntu, which can lead to unexpected build failures due to changes in the base image.

**Problem:**
Using `ubuntu:latest` leads to non-deterministic builds.  Each build might pull a different version of Ubuntu, potentially introducing inconsistencies and breaking your application.

**Solution:**
Specify a specific Ubuntu version (e.g., `ubuntu:22.04` or a long-term support release) to guarantee consistent builds.