# Socorro model

The AMI used for spinning up new instances is built using Packer (also in this
repo).  This AMI comes pre-installed with all of the bits and pieces required
to run pretty much every aspect of Socorro; however, by default, all of the
possible services are disabled.  There are a number of *roles* which determine
which aspects of the default AMI are activated - the details of this activation
process are still being worked on.

## Details

Performing a `terraform apply` on this repo will result in a small amount of
infrastructure being spun up in the `us-west-2` AWS zone.  The AWS access and
secret keys need to be supplied either as environment variables, or via
the `terraform.tfvars` file.