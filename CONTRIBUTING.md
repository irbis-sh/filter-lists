# Contributing to Zen's filter lists

> [!NOTE]
> Before proceeding, please read our [Code of Conduct](https://docs.irbis.sh/code-of-conduct), including the section on AI use.

This repository includes two sets of lists:

- `ads` and `privacy` fill gaps in the filter lists that are [enabled by default](https://github.com/irbis-sh/zen-desktop/blob/master/internal/config/default-config.json) in Zen. This guide covers these two lists.
- `no-doomscroll` hides algorithmic feeds and recommendations. See its own readme for how to [report a problem](no-doomscroll/readme.md#something-broke) and how to [contribute](no-doomscroll/readme.md#contributing).

## Reporting a problem

If you're certain a rule in this repository is causing a problem, please [open a new issue](https://github.com/irbis-sh/filter-lists/issues/new?labels=bug) in this repository.

If Zen breaks a site or isn't blocking an ad or tracker, and you're not sure which rule/filter list is responsible, please use Zen's [issue triage form](https://github.com/irbis-sh/zen-desktop/discussions/new?category=issue-triage) instead.

## List policies

For both `ads` and `privacy` lists, we accept two kinds of rules:

1. Rules the default lists miss, like an ad or tracker that gets through with every default list enabled.
2. Fixes for rules in the default lists – if the original rule doesn't work in Zen due to incompatibility, or if it breaks a site.

## Adding a rule

Rules should follow the [filter list syntax](https://docs.irbis.sh/docs/zen/reference/filter-list-syntax/) supported by Zen.

To submit:

1. Test the rule in Zen. Stop the proxy, add the rule in the **Rules** tab, start the proxy, and check that the rule works and that the site still behaves normally.
2. Add the rule to `ads/ads.txt` or `privacy/privacy.txt`. If the reason for it isn't obvious, add a `!` comment above it. For a fix to a rule in a default list, specify the list it comes from.
3. Open a pull request, starting the title with the list name, such as `ads: hide banner on example.com`. Describe what the rule fixes and how to check it.

By contributing, you agree that your work will be licensed under the [MIT Licence](LICENSE).
