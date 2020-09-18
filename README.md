This is a repository for workflow templates to run Pulumi in CI/CD systems.

These templates are used by the Pulumi Console to provide customized templates based on your stack.

## Template Tokens

The following tokens are supported by the Console so that they are dynamically replaced:

> The templating engine is Go's text/template engine.

* `PulumiStackName`
* `PathFilter`
* `WorkingDirectory`

### Delimiters

The delimiters for the above tokens are `[[` and `]]`. For example, to use the `PulumiStackName` token, you'd do `[[ .PulumiStackName ]]`.
This is to avoid any collisions with CI systems that use parentheses or double-curly braces for build variable expansion in their configuration files.
It also makes it easy to recognize which ones are placeholder tokens supported by the Pulumi Service and which ones are provided by the CI service itself.
