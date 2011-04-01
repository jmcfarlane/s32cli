======
S32cli
======

Currently this repo only contains a single file, which helps make it
easy to upload/sync files to Amazon s3.

Dependencies
++++++++++++

1. python-boto


Usage
+++++
You can specify the s3 keyid and secret in either of two ways:

1. Set AWS_ACCESS_KEY_ID and AWS_SECRET_ACCESS_KEY environment variables.

2. Specify -k and -a command line options. (Note that these option will be visible to any other users on your system via the process table).
