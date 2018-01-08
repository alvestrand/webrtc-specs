This repository contains all the Git-tracked documents (that I've found)
in the WebRTC standards work.

To check out:

  git clone --recursive git@github.com:alvestrand/webrtc-specs.git

To update all specs to the most recent version (this takes some time):

  git submodule init
  git submodule update --remote

The "init" step is only needed when new repos are added, but does no harm.

NOTE: This will likely leave your submodules in "detached head" state.
It will NOT overwrite your not-checked-in-changes, but it will confuse.
If you want to push a branch, check it out explicitly.

Build status
------------
* ![](https://travis-ci.org/w3c/mediacapture-main.svg?branch=master) mediacapture-main
* ![](https://travis-ci.org/w3c/webrtc-pc.svg?branch=master) webrtc-pc
* ![](https://travis-ci.org/w3c/webrtc-stats.svg?branch=master) webrtc-stats
* ![](https://travis-ci.org/w3c/mediacapture-output.svg?branch=master) mediacapture-output
* ![](https://travis-ci.org/w3c/mediacapture-image.svg?branch=master) mediacapture-image
* ![](https://travis-ci.org/w3c/mediacapture-fromelement.svg?branch=gh-pages) mediacapture-fromelement
* ![](https://travis-ci.org/w3c/mediacapture-worker.svg?branch=gh-pages) mediacapture-worker
* ![](https://travis-ci.org/w3c/mediacapture-depth.svg?branch=master) mediacapture-depth
* ![](https://travis-ci.org/w3c/mediacapture-screen-share.svg?branch=gh-pages) mediacapture-screen-share
* ![](https://travis-ci.org/w3c/mediacapture-record.svg?branch=master) mediacapture-record

WebRTC demo and tools pages:

* ![](https://travis-ci.org/webrtc/samples.svg?branch=gh-pages) samples
* ![](https://travis-ci.org/webrtc/testrtc.svg?branch=master) testrtc
* ![](https://travis-ci.org/webrtc/adapter.svg?branch=master) adapter
* ![](https://travis-ci.org/webrtc/apprtc.svg?branch=master) apprtc


Maintenance
-----------
I expect to do this myself; the important info is only what specs exist
and which branch for each is worth tracking. Keeping up to date can be
done by everyone who clones this.

If you have new specs to add, send me a pull request.

To add a spec:

  git submodule add git@github.com:&lt;user>/&lt;repo> &lt;local dir for repo>

To specify which branch is tracked by "submodule update":

  git config -f .gitmodules submodule.&lt;spec-directory>.branch &lt;branch name>

To change the repository tracked by a branch:

* edit .gitmodules to change the URL
* rm -rf the old repo (just resyncing does NOT overwrite the .git config)
* git submodule sync
* git submodule update --remote

To push updates on which version is the latest:

  git push

Enjoy!
