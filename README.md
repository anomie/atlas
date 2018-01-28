# atlas
Setting up servers with Ansible 2.x

## To setup

Install ansible, on macOS this can be achieved with:

```
brew install ansible
```

Add your servers to your `~/.ssh/config` file. Example blocks of
this are included in the various setup directories. Just appened
them and update your IPs, key paths, etc. accordingly.

## What information to update

All information that _definitely_ should be updated is marked with
a comment. If you want to see all the comments at once, `cd` into
the desired directory and run:

```
ack \# .
```

If you are running Ubuntu, you'll need to replace `ack` with
`ack-grep`.

## Minimal configuration

In the `minimal` directory, after making your edits, run:

```
ansible-playbook create-users.yml
ansible-playbook install-pkgs.yml
```
