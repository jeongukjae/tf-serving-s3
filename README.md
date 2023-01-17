# tf-serving-s3

Custom TensorFlow Serving image built with TensorFlow IO for AWS S3 filesystem support.

**Check [GitHub Packages](https://github.com/jeongukjae/tf-serving-s3/pkgs/containers/tf-serving-s3) for the Docker images.**

## Usage

The usage is exactly the same as the official TensorFlow Serving image.
For more details, please refer to the [TensorFlow Serving with Docker](https://www.tensorflow.org/tfx/serving/docker).
But you need to use the image from GitHub Packages instead of the official image.

## What is the differences/details?

Check this blog post: <>

## How to build the image?

```bash
docker build -t ghcr.io/jeongukjae/tf-serving-s3:2.11.0-devel -f Dockerfile.devel .
docker build -t ghcr.io/jeongukjae/tf-serving-s3:2.11.0 -f Dockerfile .
```
