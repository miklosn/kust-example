`dev` and `prod` environemnts roots in:
* `k8s/env/dev`
* `k8s/env/prod`

(The referenced `base` should be remote)

Output env manifests with:
`kustomize build k8s/env/dev`
`kustomize build k8s/env/prod`

Run with:
`skaffold dev` for dev
`skaffold dev -p prod` for prod

