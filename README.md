# Go Paketo Buildpack

## `https://hub.docker.com/r/initializbuildpacks/go`

The Go Securepack offers a comprehensive suite of collaborating buildpacks tailor-made for crafting Go-based applications. This ensemble of buildpacks comprises:
- [Go Distribution CNB](https://github.com/initializ-buildpacks/go-dist)
- [Go Mod Vendor CNB](https://github.com/initializ-buildpacks/go-mod-vendor)
- [Go Build CNB](https://github.com/initializ-buildpacks/go-build)

The buildpack extends its support to crafting applications utilizing either the built-in [Go modules](https://golang.org/cmd/go/#hdr-Module_maintenance) functionality for efficient management of dependencies.. Usage examples can be found in the
[`samples` repository under the `go` directory](https://github.com/initializ-buildpacks/samples/tree/main/go).

#### The Go buildpack is compatible with the following builder(s):
- [Securepacks Initz Builder](https://github.com/initializ-buildpacks/Securepack)

This buildpack also includes the following utility buildpacks:
- [Git CNB](https://github.com/initializ-buildpacks/git)
- [Procfile CNB](https://github.com/initializ-buildpacks/procfile)
- [Environment Variables CNB](https://github.com/initializ-buildpacks/environment-variables)
- [Image Labels CNB](https://github.com/initializ-buildpacks/image-labels)
- [CA Certificates CNB](https://github.com/initializ-buildpacks/ca-certificates)

Check out the [Go Securepack docs](<docs/url>) for more information.

† To build with the static buildpackless builder, use the following command:

```
pack build \
  --builder initializbuildpacks/securepacks-initzbuilder \
  --buildpack initializbuildpacks/go \
  --env "CGO_ENABLED=0" \
  --env "BP_GO_BUILD_FLAGS=-buildmode=default"
  <app-name>
```
