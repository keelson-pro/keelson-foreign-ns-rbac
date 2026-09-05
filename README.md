# Keelson Foreign Namespace RBAC

An add-on for [Keelson](https://github.com/keelson-pro/keelson). It grants the
Keelson ServiceAccount the workload permissions it needs in a namespace Keelson
isn't deployed in.

If you're running a strict namespace list and want tight least-privilege
permissions for Keelson rather than leaning on the `ClusterRole`, then deploy
one of these in each namespace on Keelson's namespace list except its own.
Keelson's own namespace is covered by a `Role` and `RoleBinding` that are
deployed with Keelson by default. The permissions are the same set the core
bundle grants Keelson in its own namespace.


## Configuration

| Kaptain Config Token                    | Default        | Purpose                                                               |
|-----------------------------------------|----------------|-----------------------------------------------------------------------|
| `KeelsonForeignNsRbac/KeelsonNamespace` | none, required | The namespace Keelson itself runs in and where its ServiceAccount is. |


# License

Keelson is MIT licensed except for `*.md` Markdown docs which are CC-BY-SA-4.0
For more detail see [LICENSE.md](https://github.com/keelson-pro/.github/blob/main/LICENSE.md).
