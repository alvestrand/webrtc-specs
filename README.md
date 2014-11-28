This repository contains all the Git-tracked documents (that I've found)
in the WebRTC standards work.

To check out:

  git clone --recursive git@github.com:alvestrand/webrtc-specs.git

To update all specs to the most recent version (this takes some time):

  git submodule update --remote

NOTE: This will likely leave your submodules in "detached head" state.
It will NOT overwrite your not-checked-in-changes, but it will confuse.
If you want to push a branch, check it out explicitly.

Maintenance
-----------
I expect to do this myself; the important info is only what specs exist
and which branch for each is worth tracking. Keeping up to date can be
done by everyone who clones this.

If you have new specs to add, send me a pull request.

To add a spec:

  git submodule add git@github.com:<user>/<repo> <local dir for repo>

To specify which branch is tracked by "submodule update":

  git config -f .gitmodules submodule.<spec-directory>.branch <branch name>

To push updates on which version is the latest:

  git push

Enjoy!


