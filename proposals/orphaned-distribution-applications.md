## Objective

Provide clarity about ownership and maintenance of applications which are currently
orphaned and primarily used by distributions of Kubeflow.

## Motivation

Since July, the Kubeflow community has been working on forming working groups to create greater
accountability for the different parts of Kubeflow.

Kubeflow is currently split between

  1. Individual Kubeflow applications (e.g. Pipelines, KFServing, notebooks, etc...)
  1. Distributions of Kubeflow (e.g. Kubeflow on GCP, Kubeflow on AWS, MiniKF, etc...)

Proposal #???? proposes moving ownership and responsibility of distributions outside of Kubeflow. 

Since July we have formed working groups to take ownership of all the major Kubeflow applications.

This leaves an open question about what to do about some of the remaining applications without clear owners; 
in particular

   * [Central Dashboard](https://github.com/kubeflow/community/issues/380)
   * [KFAM](https://github.com/kubeflow/kubeflow/tree/master/components/access-management)
   * [Pod Defaults Controller](https://github.com/kubeflow/community/issues/381)
   * [Profile Controller](https://github.com/kubeflow/kubeflow/tree/master/components/profile-controller)

## Proposal

There should be no further development of these applications within Kubeflow. Anyone interested in further developing these
components should fork the code and move development outside of Kubeflow.

Applications and distributions that depend on these components should do one of the following 

  1. Find a replacement or remove the dependency 
  1. Continue to maintain them outside of Kubeflow

## Alternatives Considered

An alternative would be to form one or more work groups to continue to maintain these applications.

Over the past 6 months, we have struggled to create accountability for these applications. For example, it
has been difficult to find individuals to take responsibility for releases and bug fixes.

None of these applications is AI or ML specific. These are generic applications aimed at building platforms out of loosely coupled applications.

   * Central Dashboard is a navigation bar for navigating among multiple applications
   * Pod Defaults Controller is an admission controller for setting pod defaults
   * Profile controller is a CR to simplify setting up new namespaces with specific access patterns

These applications are primarily used by Kubeflow distributions as opposed to individual applications. Since the plane (proposal #????) is to move responsibility for Kubeflow distributions outside of Kubeflow, it follows that any dependencies specific to the distributions should likewise move outside of Kubeflow.