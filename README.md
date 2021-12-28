# test-operator
Test Operator using operator-sdk 1.15

```bash
operator-sdk init --domain rbt.com --repo github.com/ravitri/test-operator
Writing kustomize manifests for you to edit...
Writing scaffold for you to edit...
Get controller runtime:
$ go get sigs.k8s.io/controller-runtime@v0.10.0
go: downloading k8s.io/apimachinery v0.22.1
go: downloading k8s.io/client-go v0.22.1
go: downloading k8s.io/api v0.22.1
Update dependencies:
$ go mod tidy
Next: define a resource with:
$ operator-sdk create api
```

```bash
operator-sdk create api --group rbtgroup --version v1alpha1 --kind RBTResource --resource --controller
Writing kustomize manifests for you to edit...
Writing scaffold for you to edit...
api/v1alpha1/rbtresource_types.go
controllers/rbtresource_controller.go
Update dependencies:
$ go mod tidy
Running make:
$ make generate
go: creating new go.mod: module tmp
Downloading sigs.k8s.io/controller-tools/cmd/controller-gen@v0.7.0
go: downloading golang.org/x/tools v0.1.5
go: downloading github.com/fatih/color v1.12.0
go: downloading k8s.io/api v0.22.2
go: downloading k8s.io/apimachinery v0.22.2
go: downloading k8s.io/apiextensions-apiserver v0.22.2
go: downloading github.com/gobuffalo/flect v0.2.3
go get: added sigs.k8s.io/controller-tools v0.7.0
/home/travi/go/src/github.com/ravitri/test-operator/bin/controller-gen object:headerFile="hack/boilerplate.go.txt" paths="./..."
Next: implement your new API and generate the manifests (e.g. CRDs,CRs) with:
$ make manifests
```
