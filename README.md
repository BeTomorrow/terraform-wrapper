Minimalist Terraform wrapper to help with Terraform version and variables per workspace.

# Requirements

OSX, bash compatible shell, [tfenv](https://github.com/tfutils/tfenv).

# Homebrew Install

```
brew install betomorrow/draft/terraform-wrapper
```

# Manual Install

Checkout this repo, give the `tfw` script `+x` permission and add the directory to your `PATH` variable
or add a symbolic link for example in your `/usr/local/bin`:

```sh
chmod +x tfw
ln -s `pwd`/tfw /usr/local/bin/tfw
```

# Use

Make sure you have expected Terraform version installed with `tfenv install min-required` in your terraform folder.

Create a `workspaces/<workspace>.tfvars` file for your workspaces in your root module.

Use `tfw` instead of `terraform`. It runs `tfenv use min-required` first then will forward command to `terraform`
while adding a `-var-file=workspaces/<workspace>.tfvars` option when needed.
