## Install CRC CodeReadyContainer
[Link to CRC](https://console.redhat.com/openshift/create/local)


1. ### Install CRC following the instructions from the link above
   * **Important**: Make sure Hyper-V is active on Windows and no other VM are installed (e.g. VirtualBox)
   *
2. ### Setup crc
   * `crc setup`
   * `crc start`
3. ### Cluster ready
   Now the cluster should be up and running, we can also login by using the token for developer
   `oc login --token=sha256~_*** --server=https://127.0.0.1:6443`
4. ### Install the Red Hat Openshift Pipelines



