# Summary

[Restriction Rules](https://developer.salesforce.com/docs/atlas.en-us.restriction_rules.meta/restriction_rules/restriction_rules_about.htm) are beta as of v52.0.  This repository is a sample showing an issue with converting restriction rules to metadata API format.

## Steps

1. Clone this repository
1. Run `sfdx force:source:convert -d ./mdapi`

### Expected

Source is converted to metadata API format with a `restrictionRules` folder and the `package.xml` should reference the `RestrictionRule` metadata type.

### Actual

Source is converted to metadata API formate with a `moderation` folder instead of `restrictionRules`.  The `package.xml` file also defines the metadata type as `ModerationRule` instead of `RestrictionRule`.
