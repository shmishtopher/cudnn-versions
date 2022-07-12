# cuDNN-versions

We've all been there.  You're setting up a custom installation of Jax/Torch/TensorFlow and... Agh! The `cuDNN` version you installed doesn't match what your framework supports!  You hastily install a new cuDNN distribution and now you have missmatch with your `CUDA` toolkit, and a pretty big mess.  `cuDNN-versions` aims to ease some of this strain.  This repository provides a `scoop` bucket containing every `cuDNN` build, for every applicable `CUDA` version, so that you can easily search and install what you're looking for.

## Usage
This repo can be added like any other scoop bucket by running the following command.
```
scoop bucket add cudnn-versions https://github.com/shmishtopher/cudnn-versions
```

You should be able to search for `cuDNN` distributions with `scoop search`.
```
❯ scoop search cuDNNv8.2
Results from local buckets...

Name                            Version Source         Binaries
----                            ------- ------         --------
cuDNNv8.2.0-CUDAv10.2-windows10 8.2.0   cudnn-versions
cuDNNv8.2.0-CUDAv11.3-windows   8.2.0   cudnn-versions
cuDNNv8.2.1-CUDAv10.2-windows10 8.2.1   cudnn-versions
cuDNNv8.2.1-CUDAv11.3-windows   8.2.1   cudnn-versions
cuDNNv8.2.2-CUDAv10.2-windows10 8.2.2   cudnn-versions
cuDNNv8.2.2-CUDAv11.4-windows   8.2.2   cudnn-versions
cuDNNv8.2.4-CUDAv10.2-windows10 8.2.4   cudnn-versions
cuDNNv8.2.4-CUDAv11.4-windows   8.2.4   cudnn-versions
```

## Version Triples
Every `cuDNN` build is index by a target tripple that looks like `<CUDNN_VERSION>-<CUDA_VERSION>-<PLATFORM>`.

| Field         | Description                                | Example     |
| ------------- | ------------------------------------------ | ----------- |
| CUDNN_VERSION | The version of the cuDNN library           | cuDNNv8.4.1 |
| CUDA_VERSION  | The compatible CUDA toolkit version        | CUDAv11.6   |
| PLATFORM      | The platform the distribution is built for | windows10   |

## Contributing
Manifests in this bucket are created automatically by the `discover-versions.ps1` script in the root of this repository.  Any changes that you want to see should be made to that file.

## Help
For assistance, please open up an issue or contact me directly at `me@shmish.dev`.