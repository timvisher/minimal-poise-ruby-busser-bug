Until I can get past omnitruck being down…

This is (essentially) what happens when you `kitchen test bad-poise-ruby`

```
-----> Setting up <example-vagrant-1404>...
       Finished setting up <example-vagrant-1404> (0m0.00s).
-----> Verifying <example-vagrant-1404>...
       Preparing files for transfer
-----> Installing Busser (busser)
       ERROR:  While executing gem ... (Errno::EACCES)
           Permission denied @ dir_s_mkdir - /home/vagrant/.gem/specs
       sudo: /tmp/verifier/bin/busser: command not found
-----> Installing Busser plugin: busser-bats
       sudo: /tmp/verifier/bin/busser: command not found
```

I will post a full log once I have one.
