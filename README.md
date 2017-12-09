```
$ chef -v
Chef Development Kit Version: 2.4.17
chef-client version: 13.6.4
delivery version: master (73ebb72a6c42b3d2ff5370c476be800fee7e5427)
berks version: 6.3.1
kitchen version: 1.19.2
inspec version: 1.45.13

$ kitchen test bad-poise-ruby
…
-----> Setting up <bad-poise-ruby-vagrant-1404>...
       Finished setting up <bad-poise-ruby-vagrant-1404> (0m0.00s).
-----> Verifying <bad-poise-ruby-vagrant-1404>...
       Preparing files for transfer
-----> Installing Busser (busser)
       ERROR:  While executing gem ... (Errno::EACCES)
           Permission denied @ dir_s_mkdir - /home/vagrant/.gem/specs
       sudo: /tmp/verifier/bin/busser: command not found
-----> Installing Busser plugin: busser-bats
       sudo: /tmp/verifier/bin/busser: command not found
>>>>>> ------Exception-------
>>>>>> Class: Kitchen::ActionFailed
>>>>>> Message: 1 actions failed.
>>>>>>     Verify failed on instance <bad-poise-ruby-vagrant-1404>.  Please see .kitchen/logs/bad-poise-ruby-vagrant-1404.log for more details

$ KITCHEN_YAML=.kitchen.chef12.yml kitchen test bad-poise-ruby
…
-----> Setting up <bad-poise-ruby-vagrant-1404>...
       Finished setting up <bad-poise-ruby-vagrant-1404> (0m0.00s).
-----> Verifying <bad-poise-ruby-vagrant-1404>...
       Preparing files for transfer
-----> Installing Busser (busser)
       ERROR:  While executing gem ... (Errno::EACCES)
           Permission denied @ dir_s_mkdir - /home/vagrant/.gem/specs
       sudo: /tmp/verifier/bin/busser: command not found
-----> Installing Busser plugin: busser-bats
       sudo: /tmp/verifier/bin/busser: command not found
>>>>>> ------Exception-------
>>>>>> Class: Kitchen::ActionFailed
>>>>>> Message: 1 actions failed.
>>>>>>     Verify failed on instance <bad-poise-ruby-vagrant-1404>.  Please see .kitchen/logs/bad-poise-ruby-vagrant-1404.log for more details

$ kitchen test no-poise-ruby-works
…
-----> Setting up <no-poise-ruby-works-vagrant-1404>...
       Finished setting up <no-poise-ruby-works-vagrant-1404> (0m0.00s).
-----> Verifying <no-poise-ruby-works-vagrant-1404>...
       Preparing files for transfer
-----> Installing Busser (busser)
Fetching: thor-0.19.0.gem (100%)
       Successfully installed thor-0.19.0
Fetching: busser-0.7.1.gem (100%)
       Successfully installed busser-0.7.1
       2 gems installed
-----> Installing Busser plugin: busser-bats
       Plugin bats installed (version 0.3.0)
-----> Running postinstall for bats plugin
       Installed Bats to /tmp/verifier/vendor/bats/bin/bats
       Suite path directory /tmp/verifier/suites does not exist, skipping.
       Transferring files to <no-poise-ruby-works-vagrant-1404>
-----> Running bats test suite
 ✓ it gets here!
       
       1 test, 0 failures
       Finished verifying <no-poise-ruby-works-vagrant-1404> (0m2.42s).
-----> Destroying <no-poise-ruby-works-vagrant-1404>...
       ==> default: Forcing shutdown of VM...
       ==> default: Destroying VM and associated drives...
       Vagrant instance <no-poise-ruby-works-vagrant-1404> destroyed.
       Finished destroying <no-poise-ruby-works-vagrant-1404> (0m4.72s).
       Finished testing <no-poise-ruby-works-vagrant-1404> (1m11.58s).
-----> Kitchen is finished. (1m12.29s)


$ KITCHEN_YAML=.kitchen.chef12.yml kitchen test no-poise-ruby-works
…
-----> Setting up <no-poise-ruby-works-vagrant-1404>...
       Finished setting up <no-poise-ruby-works-vagrant-1404> (0m0.00s).
-----> Verifying <no-poise-ruby-works-vagrant-1404>...
       Preparing files for transfer
-----> Installing Busser (busser)
Fetching: thor-0.19.0.gem (100%)
       Successfully installed thor-0.19.0
Fetching: busser-0.7.1.gem (100%)
       Successfully installed busser-0.7.1
       2 gems installed
-----> Installing Busser plugin: busser-bats
       Plugin bats installed (version 0.3.0)
-----> Running postinstall for bats plugin
       Installed Bats to /tmp/verifier/vendor/bats/bin/bats
       Suite path directory /tmp/verifier/suites does not exist, skipping.
       Transferring files to <no-poise-ruby-works-vagrant-1404>
-----> Running bats test suite
 ✓ it gets here!
       
       1 test, 0 failures
       Finished verifying <no-poise-ruby-works-vagrant-1404> (0m2.47s).
-----> Destroying <no-poise-ruby-works-vagrant-1404>...
       ==> default: Forcing shutdown of VM...
       ==> default: Destroying VM and associated drives...
       Vagrant instance <no-poise-ruby-works-vagrant-1404> destroyed.
       Finished destroying <no-poise-ruby-works-vagrant-1404> (0m4.68s).
       Finished testing <no-poise-ruby-works-vagrant-1404> (1m4.24s).
-----> Kitchen is finished. (1m4.93s)
```

