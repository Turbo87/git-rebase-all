git-rebase-all
==============================================================================

**This project is work-in-progress! The content below is not yet implemented!**

… automatically rebases your git feature branches

`git-rebase-all` will first run `git fetch` to download any updates from the
remote server(s). Afterwards it will show a list of planned branch updates
according to the following logic:

- local branches without a tracking branch will be rebased
- local branches that are pointing to the same commit as their tracking branch
  will be rebase and pushed to the server again
- local branches that are pointing to a different commit than their tracking
  branch will be skipped

Once you confirm these actions, the branches will be rebased and finally the
updates will be pushed to the server.


Install
------------------------------------------------------------------------------

```bash
cargo install git-rebase-all
```


Usage
------------------------------------------------------------------------------

```
git-rebase-all 

USAGE:
    git-rebase-all [FLAGS] [OPTIONS]

FLAGS:
    -h, --help               Prints help information
        --rebase             Rebases branches automatically without user confirmation
        --rebase-and-push    Rebases and pushes branches automatically without user confirmation
        --skip-fetch         Skips the `git fetch` step
    -V, --version            Prints version information

OPTIONS:
        --cwd <cwd>    Changes the working directory to `cwd`
```


License
------------------------------------------------------------------------------

git-rebase-all is released under the [MIT License](LICENSE.md).
