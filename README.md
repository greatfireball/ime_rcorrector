# ime_rcorrector
Docker image for the Rcorrector RNA-seq correction pipeline

## Prerequisities

In order to run this container you'll need docker installed.

* [Windows](https://docs.docker.com/windows/started)
* [OS X](https://docs.docker.com/mac/started/)
* [Linux](https://docs.docker.com/linux/started/)

## Usage

The docker image provides the [Rcorrector](https://github.com/mourisl/Rcorrector) tool. It will run the `run_rcorrector.pl` command as entrypoint.
Therefore, running a container is as easy as:

```
docker run --rm greatfireball/ime_rcorrector --version
```

Just provide all required parameters via command line.
Default working directory is `/data`.
Therefore, input data should be mounted using `/data` volume.

Running the the example command from the [README.md](https://github.com/mourisl/Rcorrector/blob/master/README.md):

```
docker run --user $(id -u):$(id -g) --rm -v $PWD:/data greatfireball/ime_rcorrector -1 /opt/rcorrector/Sample/sample_read1.fq -2 /opt/rcorrector/Sample/sample_read2.fq
```

## Releases

The master branch contains a rolling release.
The develop branch is used for further development.
Specific tags are used for different Rcorrector releases. Latest release is [![](https://images.microbadger.com/badges/version/greatfireball/ime_rcorrector:v1.0.3.1.svg)](https://microbadger.com/images/greatfireball/ime_rcorrector:v1.0.3.1 "Get your own version badge on microbadger.com").

| Version/Branch | Commit in Docker Repo | Image |
| -------------- | --------------------- | ----- |
| [![](https://images.microbadger.com/badges/version/greatfireball/ime_rcorrector:master.svg)](https://microbadger.com/images/greatfireball/ime_rcorrector:master "Get your own version badge on microbadger.com") | [![](https://images.microbadger.com/badges/commit/greatfireball/ime_rcorrector:master.svg)](https://microbadger.com/images/greatfireball/ime_rcorrector:master "Get your own commit badge on microbadger.com") | [![](https://images.microbadger.com/badges/image/greatfireball/ime_rcorrector:master.svg)](https://microbadger.com/images/greatfireball/ime_rcorrector:master "Get your own image badge on microbadger.com") |
| [![](https://images.microbadger.com/badges/version/greatfireball/ime_rcorrector:develop.svg)](https://microbadger.com/images/greatfireball/ime_rcorrector:develop "Get your own version badge on microbadger.com") | [![](https://images.microbadger.com/badges/commit/greatfireball/ime_rcorrector:develop.svg)](https://microbadger.com/images/greatfireball/ime_rcorrector:develop "Get your own commit badge on microbadger.com") | [![](https://images.microbadger.com/badges/image/greatfireball/ime_rcorrector:develop.svg)](https://microbadger.com/images/greatfireball/ime_rcorrector:develop "Get your own image badge on microbadger.com") |
| [![](https://images.microbadger.com/badges/version/greatfireball/ime_rcorrector:v1.0.3.1.svg)](https://microbadger.com/images/greatfireball/ime_rcorrector:v1.0.3.1 "Get your own version badge on microbadger.com") | [![](https://images.microbadger.com/badges/commit/greatfireball/ime_rcorrector:v1.0.3.1.svg)](https://microbadger.com/images/greatfireball/ime_rcorrector:v1.0.3.1 "Get your own commit badge on microbadger.com") | [![](https://images.microbadger.com/badges/image/greatfireball/ime_rcorrector:v1.0.3.1.svg)](https://microbadger.com/images/greatfireball/ime_rcorrector:v1.0.3.1 "Get your own image badge on microbadger.com") |

## Contributing

Please read [CONTRIBUTING.md](CONTRIBUTING.md) for details on our code of conduct, and the process for submitting pull requests to us.

## Author

- **Frank Förster** - *Initial work* - [greatfireball](https://github.com/greatfireball)

See also the list of [contributors](https://github.com/greatfireball/ime_rcorrector/contributors) who participated in this project.

## License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details.
