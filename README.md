# concourse-demo
Concourse Demo files

* Install vagrant files

```
  vagrant init concourse/lite # creates ./Vagrantfile
  vagrant up                  # downloads the box and spins up the VM
```

* Get Fly CLI from 192.168.100.4:8080 
  + you can see the icons in on the right side at the bottom.
  + concourse image should be running with this IP address

* modify the uri of "pcf-hol" in gitcfsample.yml, it should be your github repository

* modify each parameters in "mysettings.yml", update them with your credentials

* run the command in below and see the pipeline can be shown in http://192.168.100.4:8080

```
fly set-pipeline -p <PIPELINE_NAME> -c gitcfsample.yml -l mysettings.yml
```

* initial job will be running automatically, and see the result of it.

* then, try to push the new code to your github repository, then you can see your pipeline <PIPELINE_NAME> is running automatically

