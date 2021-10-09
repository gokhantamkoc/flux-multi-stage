# flux-multi-stage

A demo for multi-environment CI/CD system

## fluxctl

After pushing this template repository and if your cluster has the necessary access to the github repository you define in this command:

```
$ fluxctl install \
--git-user=${GHUSER} \
--git-email=${GHUSER}@users.noreply.github.com \
--git-path=acpt \
--manifest-generation=true \
--git-url=git@github.com:${GHUSER}/flux-multi-stage \
--namespace=flux | kubectl apply -f -
```

`flux-ctl` in the environments called `acpt` and `prod` will updated every 5 minutes.
