<!-- markdownlint-disable -->

## Inputs

| Name | Description | Default | Required |
|------|-------------|---------|----------|
| config-name | If your workflow requires multiple release-drafter configs it is helpful to override the config-name.<br>The config should still be located inside `.github` as that's where we are looking for config files.<br> | configs/draft-release.yml | false |
| latest | A string indicating whether the release being created or updated should be marked as latest.<br> |  | false |
| prerelease | Boolean indicating whether this release should be a prerelease |  | false |
| publish | Whether to publish a new release immediately | false | false |
| summary-enabled | Enable github action summary. | true | false |
| token | Standard GitHub token (e.g., secrets.GITHUB\_TOKEN) | ${{ github.token }} | false |


## Outputs

| Name | Description |
|------|-------------|
| body | The body of the drafted release. |
| exists | Tag exists so skip new release issue |
| html\_url | The URL users can navigate to in order to view the release |
| id | The ID of therelease that was created or updated. |
| major\_version | The next major version number. For example, if the last tag or release was v1.2.3, the value would be v2.0.0. |
| minor\_version | The next minor version number. For example, if the last tag or release was v1.2.3, the value would be v1.3.0. |
| name | The name of the release |
| patch\_version | The next patch version number. For example, if the last tag or release was v1.2.3, the value would be v1.2.4. |
| resolved\_version | The next resolved version number, based on GitHub labels. |
| tag\_name | The name of the tag associated with the release. |
| upload\_url | The URL for uploading assets to the release, which could be used by GitHub Actions for additional uses, for example the @actions/upload-release-asset GitHub Action. |
<!-- markdownlint-restore -->
