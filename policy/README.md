# Continuum Package Policy

These are example Continuum policy documents that retire old versions
of Continuum packages.

Retiring a package does not immediately upgrade existing jobs to the
new package version.  Jobs will be upgraded on their next deploy.
These policies should not be imported into a cluster without
considering the impact to existing jobs.  Jobs may need to be tested
for compatibilty with the latest version of the package.

APC's `policy import` command allows you to import these policies into
your cluster.

```console
$ apc policy import policy/ruby-2-0-security-update
```

Carefully examine all policy documents before importing and compare to
any custom packages that exist in your Continuum cluster.

To check for existing jobs using a package you can use the
`--filter-packages` argument to APC.

```console
$ apc job list -l -ns / --filter-by-package /apcera/pkg/runtimes::python-2.7.8
```
