```
oc login -u system:admin
oc new-project gitlab
oc adm policy add-scc-to-user anyuid -z gitlab-ce-user -n gitlab
oc adm policy add-scc-to-user privileged -z gitlab-runner-user -n gitlab
oc adm policy add-scc-to-group anyuid default
oc create -f gitlab.template.json
```
In web-interface we will to create new app gitlab in namespase's gitlab
```
chown -R chrony.input <gitlab-ce-etc>/ssh/*
```