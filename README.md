Use Impromptu
=============

1. `npm install -g use-impromptu`
2. Add `source impromptu` to your shell's configuration file (bashrc, zshrc, etc).

---

This installs Impromptu dependencies and clones the `my-impromptu` repository into `~/.impromptu`, adds a global `impromptu` bin script, and sets your prompt to use Impromptu.


## Using Sudo

We recommend that you do **not** use `sudo` to install Use Impromptu. If you absolutely must, you'll probably need to pass the `--unsafe` flag, like this: `npm install -g use-impromptu --unsafe`

The reason for this is that NPM tries to limit the risk of running install commands with `sudo` by running the package's install scripts as a non-root user called `nobody`. Use Impromptu clones a [starter prompt](https://github.com/Impromptu/my-impromptu) for you by deafult, so it needs to be able to create files in your home directory. The `nobody` user probably doesn't have permission to do that, so if you run the installer as a user other than your own, we need permission to act as `root`.

The exception to this is if you already have a prompt directory or just don't want Use Impromptu to create one for you. In that case we do not need permission to write files, and therefore do not need to act as `root`.
