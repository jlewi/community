## Objective

Clarify ownership and processes related to Kubeflow releases.

## Motivation

Historically, Kubeflow did a minor release every quarter. Each release consisted of the latest
release of Kubeflow applications as well some applications developed outside of Kubeflow (e.g. Seldon).

Doing centralized releases has become untenable. No one in the community has demonstrated a willingness
and track record to continue to take on the cost of centralized releases going forward.

Through Kubeflow 1.0, releases were primarily driven by Google. In the Spring, Google announced it didn't want
to drive the 1.1 release and asked for volunteers. No one stepped up so Google ended up driving the 1.1 release. 
We again asked for volunteers to drive the 1.2 release. Unfortunately, this just isn't working see [https://github.com/kubeflow/kubeflow/issues/5224](https://github.com/kubeflow/kubeflow/issues/5224); the cut date for the release has come and gone. There are no clear timelines and no clear owner driving the release.

## Proposal

No more centralized Kubeflow releases. Going forward each work group will be responsible for releasing
and versioning their applications and publishing appropriate artifacts.

Owners of various distributions of Kubeflow(see #????) (e.g. Kubeflow on GCP, Kubeflow on AWS, MiniKF) will
be responsible for creating and releasing bundles of applications on whatever release cadence they choose.

## Alternatives Considered

The alternative would be to create a work group or release team to continue to drive centralized this.

We have tried this and it isn't working.
