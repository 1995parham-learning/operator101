# Operator 101

## Introduction

I am using this repository for learning how I can write a Kubernetes operator.

How to initialize?

```bash
operator-sdk init --domain parham.home --repo github.com/1995parham-learning/operator101
operator-sdk create api --group hello --version v1alpha1 --kind Helloer --resource --controller
```

How to run?

```bash
make build
```

You need to have OLM on your cluster to better use operators:

```bash
operator-sdk olm install
```

Then you can bundle the operator and install it:

```bash
make bundle
operator-sdk run bundle
```
