# playground-gradle-bom-dep-manage

A sample project managing the dependencies using BoM.

## Pros/Cons

Comparison with dependency management using buildSrc.

### Pros

- Don't need to use `buildSrc` for the dependency management.
- Don't need to re-compile `buildSrc` sources when the dependencies changed.
- Dependabot and Renovate works!!

### Cons

- Needs to declare the dependencies with String like `implementation("group.id:artifact-id”)` on each submodule’s `dependencies` block.
- Needs to add `implementation(platform(project(":platform")))` on each submodule’s `dependencies` block.