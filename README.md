# tf-serving-s3

Custom TensorFlow Serving image built with TensorFlow IO for AWS S3 filesystem support.

**Check [GitHub Packages](https://github.com/jeongukjae/tf-serving-s3/pkgs/container/tf-serving-s3) for the Docker images.**

## Usage

The usage is exactly the same as the official TensorFlow Serving image.
For more details, please refer to the [TensorFlow Serving with Docker](https://www.tensorflow.org/tfx/serving/docker).
But you need to use the image from GitHub Packages instead of the official image.

```bash
$ docker run \
    -p 8500:8500 \
    -p 8501:8501 \
    -e AWS_ACCESS_KEY_ID \
    -e AWS_SECRET_ACCESS_KEY \
    -e AWS_DEFAULT_REGION \
    -e MODEL_BASE_PATH=s3://BUCKET_NAME/PATH_TO_MODEL \
    -e MODEL_NAME=MODEL_NAME \
    ghcr.io/jeongukjae/tf-serving-s3:2.11.0
```

## What is the differences/details?

Check this blog post: <https://blog.ukjae.io/posts/enabling-s3-filesystem-support-for-tensorflow-serving/>

## How to build the image?

```bash
docker build -t ghcr.io/jeongukjae/tf-serving-s3:2.11.0-devel -f Dockerfile.devel .
docker build -t ghcr.io/jeongukjae/tf-serving-s3:2.11.0 -f Dockerfile .
```
