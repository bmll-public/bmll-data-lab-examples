# BMLL Data Lab Examples

The repo provides a source of examples, recipes and best practices when using the BMLL Data Lab and BMLL Data Feed. If you have any questions, please get in touch with *support@bmlltech.com*.

## Set up

This repo can be pulled directly into the Data Lab, using the `default_bootstrap` (see https://lab.bmlltech.com/docs/contents/tutorials/git_repository.html#). An example bootstrap (with appropriate SSH keys) is:

```
SSH_DIR=$HOME/.ssh/
mkdir -p $SSH_DIR
python -c "import bmll2; bmll2.get_file('.ssh/id_rsa', local_dir='$SSH_DIR')"
python -c "import bmll2; bmll2.get_file('.ssh/id_rsa.pub', local_dir='$SSH_DIR')"
python -c "import bmll2; bmll2.get_file('.ssh/known_hosts', local_dir='$SSH_DIR')"
chmod 600 $SSH_DIR/id_rsa
chmod 600 $SSH_DIR/id_rsa.pub

git clone git@github.com:bmlltech/bmll2.git
```

## Folder structure

The repo contains a series of notebooks, that can be run directly on the Data Lab. In general, any notebooks only using the `bmll` API (rather than `bmll2`) can also be run in your own environment, although you will need to login to the API.

The folders are structured as follows:

* prototypes. This includes technical demos and samples within the Lab
* demos. These are any notebooks and snippets for specific use cases
* publications. This includes any notebooks from regular or ad-hoc BMLL publications (e.g View From The Feed and Liquidity Maps)
