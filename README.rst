======
S32cli
======

Currently this repo only contains a single file, which helps make it
easy to upload/sync files to Amazon s3.

Dependencies
++++++++++++

1. python-boto


Configuration
+++++++++++++

You can specify the s3 keyid and secret in three different ways:

1. Boto config file
-------------------

Standard ``~/.boto`` config, for example::

 [Credentials]
 aws_access_key_id = my-secret-key-id
 aws_secret_access_key = my-secret-access-key

2. Environment variables
------------------------

Set ``AWS_ACCESS_KEY_ID`` and ``AWS_SECRET_ACCESS_KEY`` environment
variables.

3. Command line args
--------------------

Specify ``-k`` and ``-a`` command line options. (Note that these
option will be visible to any other users on your system via the
process table).

Usage
+++++

The typical use case for this script is to backup a directory to s3.
So let's say we have a directory ``/foo`` which we want to backup to a
bucket named ``foo.bucket``::

 # Dry run
 ./scripts/backup2s3 -b foo.bucket -s /foo -d foo -n

 # For realz
 ./scripts/backup2s3 -b foo.bucket -s /foo -d foo

If you're not using ``~/.boto`` for configuration you'll either need
to use the cli args or the environment variables (see above).
