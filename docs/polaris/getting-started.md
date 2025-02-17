# Getting Started on Polaris

## Logging Into Polaris

To log into Polaris:

ssh <username\>@polaris.alcf.anl.gov

Then, type in the password from your cryptocard/mobilepass token.


## Hardware Overview

An overview of the Polaris system including details on the compute node architecture is available on the [Machine Overview](./hardware-overview/machine-overview.md) page.

## Compiling Applications

Users are encouraged to read through the [Compiling and Linking Overview](./compiling-and-linking/compiling-and-linking-overview.md) page and corresponding pages depending on the target compiler and programming model.

## Submitting and Running Jobs

Users are encouraged to read through the [Job Scheduling and Execution](./queueing-and-running-jobs/job-and-queue-scheduling.md) page for information on using the Cobalt schedule and preparing job submission scripts. Some example job submission scripts are available on the [Example Job Scripts](./queueing-and-running-jobs/example-job-scripts.md) page as well.

## Lustre File Striping

In addition to the content above, here is a document on Lustre File Striping Basics. 

- [Lustre File Striping Basics](https://www.alcf.anl.gov/support-center/training-assets/file-systems-and-io-performance)

## Proxy

If the node you are on doesn’t have outbound network connectivity, add the following to your ~/.bash_profile file to access the proxy host

```
# proxy settings
export HTTP_PROXY="http://proxy-01.pub.alcf.anl.gov:3128"
export HTTPS_PROXY="http://proxy-01.pub.alcf.anl.gov:3128"
export http_proxy="http://proxy-01.pub.alcf.anl.gov:3128"
export https_proxy="http://proxy-01.pub.alcf.anl.gov:3128"
export ftp_proxy="http://proxy-01.pub.alcf.anl.gov:3128"
export no_proxy="admin,polaris-adminvm-01,localhost,*.cm.polaris.alcf.anl.gov,polaris-*,*.polaris.alcf.anl.gov,*.alcf.anl.gov"
```

## Getting Assistance

Please direct all questions, requests, and feedback to [support@alcf.anl.gov](mailto:support@alcf.anl.gov).
