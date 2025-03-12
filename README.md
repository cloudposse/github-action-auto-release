

<!-- markdownlint-disable -->
<a href="https://cpco.io/homepage"><img src="https://github.com/cloudposse/github-action-auto-release/blob/main/.github/banner.png?raw=true" alt="Project Banner"/></a><br/>
    <p align="right">
<a href="https://github.com/cloudposse/github-action-auto-release/releases/latest"><img src="https://img.shields.io/github/release/cloudposse/github-action-auto-release.svg" alt="Latest Release"/></a><a href="https://slack.cloudposse.com"><img src="https://slack.cloudposse.com/badge.svg" alt="Slack Community"/></a></p>
<!-- markdownlint-restore -->

<!--




  ** DO NOT EDIT THIS FILE
  **
  ** This file was automatically generated by the `cloudposse/build-harness`.
  ** 1) Make all changes to `README.yaml`
  ** 2) Run `make init` (you only need to do this once)
  ** 3) Run`make readme` to rebuild this file.
  **
  ** (We maintain HUNDREDS of open source projects. This is how we maintain our sanity.)
  **





-->

This is an opinionated composite Github Action that implements a workflow based on the popular `release-drafter` action to automatically draft releases with release notes that are derived from PR descriptions as they are merged into the default branch. ```

Under default settings, `auto-release` will also cut a new release from the default branch after every merge into it. However, releases are not cut for merges of pull requests with a `no-release` label attached. In that case, the release notes are left as a draft and a release with all unreleased changes will be made the next time a pull request without the `no-release` label is merged into the default branch.







## Usage

Copy the `.github/workflows/auto-release.yml` and `.github/configs/release-drafter.yml` files from this repository into the corresponding folders of the repository to which you'd like to add Auto-release functionality.
This will trigger the `auto-release` functionality every time merges are made into the default branch.


## Quick Start

Here's how to get started...
1. Copy the `.github/workflows/auto-release.yml` github action workflow from this repository into the corresponding folder of the target repo
2. Copy the `.github/configs/release-drafter.yml` auto-release config file from this repository into the corresponding folder of the target repo
3. Customize the config file as desired, per the [config documentation](https://github.com/release-drafter/release-drafter#configuration)
## Examples

Here's a real world example:
- [`github-action-auto-release`](https://github.com/cloudposse/github-action-auto-release/.github/workflows/auto-release.yml) - The self-testing Cloud Posse Auto-format GitHub Action




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


## Related Projects

Check out these related projects.

- [GitHub Action Auto-format](https://github.com/cloudposse/github-action-auto-format) - Add standard files to a repo and keep its README up to date
- [GitHub Action Terraform Auto-context](https://github.com/cloudposse/github-action-terraform-auto-context) - Automatically update `context.tf` whenever a new version becomes available
- [GitHub Action Terraform CI](https://github.com/cloudposse/github-action-terraform-ci) - Full suite of Terraform CI actions, along with chatops support
- [GitHub Action Validate CODEOWNERS](https://github.com/cloudposse/github-action-validate-codeowners) - Validate and lint contents of CODEOWNERS file


## References

For additional context, refer to some of these links.

- [Release Drafter](https://github.com/release-drafter/release-drafter) - Drafts your next release notes as pull requests are merged into master




## ✨ Contributing

This project is under active development, and we encourage contributions from our community.



Many thanks to our outstanding contributors:

<a href="https://github.com/cloudposse/github-action-auto-release/graphs/contributors">
  <img src="https://contrib.rocks/image?repo=cloudposse/github-action-auto-release&max=24" />
</a>

For 🐛 bug reports & feature requests, please use the [issue tracker](https://github.com/cloudposse/github-action-auto-release/issues).

In general, PRs are welcome. We follow the typical "fork-and-pull" Git workflow.
 1. Review our [Code of Conduct](https://github.com/cloudposse/github-action-auto-release/?tab=coc-ov-file#code-of-conduct) and [Contributor Guidelines](https://github.com/cloudposse/.github/blob/main/CONTRIBUTING.md).
 2. **Fork** the repo on GitHub
 3. **Clone** the project to your own machine
 4. **Commit** changes to your own branch
 5. **Push** your work back up to your fork
 6. Submit a **Pull Request** so that we can review your changes

**NOTE:** Be sure to merge the latest changes from "upstream" before making a pull request!

### 🌎 Slack Community

Join our [Open Source Community](https://cpco.io/slack?utm_source=github&utm_medium=readme&utm_campaign=cloudposse/github-action-auto-release&utm_content=slack) on Slack. It's **FREE** for everyone! Our "SweetOps" community is where you get to talk with others who share a similar vision for how to rollout and manage infrastructure. This is the best place to talk shop, ask questions, solicit feedback, and work together as a community to build totally *sweet* infrastructure.

### 📰 Newsletter

Sign up for [our newsletter](https://cpco.io/newsletter?utm_source=github&utm_medium=readme&utm_campaign=cloudposse/github-action-auto-release&utm_content=newsletter) and join 3,000+ DevOps engineers, CTOs, and founders who get insider access to the latest DevOps trends, so you can always stay in the know.
Dropped straight into your Inbox every week — and usually a 5-minute read.

### 📆 Office Hours <a href="https://cloudposse.com/office-hours?utm_source=github&utm_medium=readme&utm_campaign=cloudposse/github-action-auto-release&utm_content=office_hours"><img src="https://img.cloudposse.com/fit-in/200x200/https://cloudposse.com/wp-content/uploads/2019/08/Powered-by-Zoom.png" align="right" /></a>

[Join us every Wednesday via Zoom](https://cloudposse.com/office-hours?utm_source=github&utm_medium=readme&utm_campaign=cloudposse/github-action-auto-release&utm_content=office_hours) for your weekly dose of insider DevOps trends, AWS news and Terraform insights, all sourced from our SweetOps community, plus a _live Q&A_ that you can’t find anywhere else.
It's **FREE** for everyone!
## License

<a href="https://opensource.org/licenses/Apache-2.0"><img src="https://img.shields.io/badge/License-Apache%202.0-blue.svg?style=for-the-badge" alt="License"></a>

<details>
<summary>Preamble to the Apache License, Version 2.0</summary>
<br/>
<br/>



```text
Licensed to the Apache Software Foundation (ASF) under one
or more contributor license agreements.  See the NOTICE file
distributed with this work for additional information
regarding copyright ownership.  The ASF licenses this file
to you under the Apache License, Version 2.0 (the
"License"); you may not use this file except in compliance
with the License.  You may obtain a copy of the License at

  https://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing,
software distributed under the License is distributed on an
"AS IS" BASIS, WITHOUT WARRANTIES OR CONDITIONS OF ANY
KIND, either express or implied.  See the License for the
specific language governing permissions and limitations
under the License.
```
</details>

## Trademarks

All other trademarks referenced herein are the property of their respective owners.


## Copyrights

Copyright © 2022-2025 [Cloud Posse, LLC](https://cloudposse.com)



<a href="https://cloudposse.com/readme/footer/link?utm_source=github&utm_medium=readme&utm_campaign=cloudposse/github-action-auto-release&utm_content=readme_footer_link"><img alt="README footer" src="https://cloudposse.com/readme/footer/img"/></a>

<img alt="Beacon" width="0" src="https://ga-beacon.cloudposse.com/UA-76589703-4/cloudposse/github-action-auto-release?pixel&cs=github&cm=readme&an=github-action-auto-release"/>
