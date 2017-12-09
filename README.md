This is what happens when you `kitchen test bad-poise-ruby`

```
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
```

And `KITCHEN_YAML=.kitchen.chef12.yml kitchen test bad-poise-ruby`

```

```
