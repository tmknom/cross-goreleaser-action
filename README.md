# cross-goreleaser-action

Run [goreleaser/goreleaser-action][goreleaser] with configuration shared across repositories.

<!-- actdocs start -->

## Description

This action serves as a convenient wrapper for [goreleaser/goreleaser-action][goreleaser].

## Usage

To set up the action, you need to create a YAML file that defines your configurations.
Refer to the detailed configuration syntax for the GoReleaser in [goreleaser/goreleaser-action][goreleaser].

### Configuration URL

```yaml
  steps:
    - name: Cross GoReleaser
      uses: tmknom/cross-goreleaser-action@v0
      with:
        configuration-url: https://raw.githubusercontent.com/tmknom/configurations/main/goreleaser/cli.yml
```

### Configuration Path

```yaml
  steps:
    - name: Cross GoReleaser
      uses: tmknom/cross-goreleaser-action@v0
      with:
        configuration-path: .goreleaser.yml
```

## Inputs

| Name | Description | Default | Required |
| :--- | :---------- | :------ | :------: |
| configuration-path | The path for the GoReleaser configurations. | n/a | no |
| configuration-url | The url for the GoReleaser configurations. | n/a | no |
| dry-run | Whether to use snapshot mode when invoking GoReleaser. | `false` | no |

## Outputs

| Name | Description |
| :--- | :---------- |
| configuration-path | The path for the configuration file to passing goreleaser/goreleaser-action. |
| configuration-sha256 | SHA256 of the configuration file to passing goreleaser/goreleaser-action. |

<!-- actdocs end -->

## Permissions

N/A

## FAQ

N/A

## Related projects

- [release-workflows](https://github.com/tmknom/release-workflows): Collection of release workflows.
- [configurations](https://github.com/tmknom/configurations): Collection of configurations.

## Release notes

See [GitHub Releases][releases].

## License

Apache 2 Licensed. See [LICENSE](LICENSE) for full details.

[goreleaser]: https://github.com/goreleaser/goreleaser-action
[releases]: https://github.com/tmknom/cross-goreleaser-action/releases
