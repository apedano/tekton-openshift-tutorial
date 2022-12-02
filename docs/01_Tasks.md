## Tasks
1. ### Create the new project

   `oc new project pipeline-tutorial`

3. ### Add the task to the project
[Task hello-world-task-1](../tasks/hello-world-task-1.yaml)
This is the content
```yaml
apiVersion: tekton.dev/v1beta1  
kind: Task  
metadata:  
  name: hello-world-task-1  
spec:  
  params:  
  - name: greeting  
    type: string  
    default: "world"  
  description: Greeting Name  
  steps:  
  - name: hello  
    image: quay.io/buildah/stable:latest  
    imagePullPolicy: IfNotPresent  
    script: |  
      #!/bin/bash  
      echo "Hello $(params.greeting)"
```
To add the file

`oc apply -n pipeline-tutorial -f <path_to_task>/hello-world-task-1.yaml`

-----BEGIN OPENSSH PRIVATE KEY-----
b3BlbnNzaC1rZXktdjEAAAAABG5vbmUAAAAEbm9uZQAAAAAAAAABAAAAMwAAAAtzc2gtZW
QyNTUxOQAAACCpfgpjAeb5elIcwEie3e40QsPInUPFsJ9j96t8HUUdugAAAKBaipYzWoqW
MwAAAAtzc2gtZWQyNTUxOQAAACCpfgpjAeb5elIcwEie3e40QsPInUPFsJ9j96t8HUUdug
AAAEBXchIDIid1Mltore9UMN7g68c+R8hKWlwdmlM5noaiGKl+CmMB5vl6UhzASJ7d7jRC
w8idQ8Wwn2P3q3wdRR26AAAAG3BlZGFuby5hbGVzc2FuZHJvQGdtYWlsLmNvbQEC
-----END OPENSSH PRIVATE KEY-----