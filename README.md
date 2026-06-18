# GitNotes

These are my *Concise Personal Notes* on the use primarily of `Git`, but also of `Github`, `GitKraken`, ~~`BitBucket`~~[^1], and the `gh` GitHub command line interface tool.  [Download the PDF](./release/gitnotes.pdf).

---

This document is starting to shape up, but the structure is not working.  I need to refactor the organization to reflect the tasks that a Git user would do, not the logical grouping of what Git does or how it works.

**Note To Ian:** *Do not have a "workflow" chapter.  Instead, include a "workflow" section in each task chapter.*

Consider the following general structure:
- [ ] quick start
- [ ] what this document is about / who it's for
- [ ] Git file management: using rm and mv (and restore?)
- [ ] creating a local repo
- [ ] git config
	- [ ] global, system, local
	- [ ] user name, email, editor
	- [ ] remotes
- [ ] using branches
	- [ ] get a list of existing branches
		- [ ] git branch		# only local branches
		- [ ] git branch -r		# only remote branches
		- [ ] git branch -a		# all branches, local and remote
		- [ ] git remote show origin	# tracking status and remote branches
	- [ ] checking out an existing branch
	- [ ] creating a new branch
	- [ ] pulling an existing branch
	- [ ] branch naming conventions
		- [ ] release
			- [ ] used when you have a scheduled release cycle
				- [ ] avoid "release" if you practice "continuous delivery"
			- [ ] used to isolate, stabilize, and finalize a specific version
			  of software before it goes to production
			- [ ] it is a dedicated buffer zone where a team performs final
			  testing, fixes minor bugs, and prepares metadata (like
			  version numbers) without interrupting ongoing development
			- [ ] workflow:
				- [ ] development cycle finishes, all features merged into
				  "develop", "release" branch created
				- [ ] code freezes; new features are merged into "develop"
				  for the next release
				- [ ] release is a staging area for stabilization
					- [ ] bug fixes
					- [ ] documentation updates
					- [ ] release metadata
				- [ ] once it's stable, dual merge:
					- [ ] merge to "master" or a "stable" version branch
						- [ ] tag the merge with the version number
					- [ ] merge to "develop"
						- [ ] any bug fixes are merged back into the
						  development stream to be carried forward
					- [ ] release branch deleted
		- [ ] stable/<version?>
			- [ ] long-running
			- [ ] thoroughly-tested production-ready code
			- [ ] for long-term support, "stable" refers to frozen major
			  versions which only accept low-risk patches
		- [ ] daily development and feature integration happen on "main" or
		  "develop"
		- [ ] once the code on "main" / "develop" passes all QA tests and
		  is successfully deployed, it is merged into stable and tagged
		  with a release version
- [ ] git restore: how to fix bad file editing
	- if `restore` has already been covered earlier in this file, this
	  will be more extensive coverage of the `restore` command
- [ ] fetching, pulling, merging
	- [ ] merge individual file(s)
- [ ] merge request
	- [ ] deleting a branch
		- [ ] "keeping obsolete branches serves no technical purpose and 
		  creates massive clutter for collaboration"
		- [ ] successful merges integrates the entire history and all of
		  the branch's commits into the parent branch
- [ ] the stable branch
- [ ] the release branch
- [ ] Git for non-coders: tips on how creatives like writers and artists
      can use Git for versioning their own work.

***

## Current Branch Structure
Branches can be found using the `branch` command:
	git branch

- `master`: master development branch
- `release`: current release version of GitNotes (not working as intended)
- `chapter/bitbucket`: the "bitbucket" chapter
- `chapter/workflow`: the "workflow" chapter
- `chapter/branch`: the "branch" chapter

***
## Stuff To Do
- [x] play around with the gihub.txt file to make sure the information is fairly accurate
- [x] create repository for this document on GitHub (remotely)
- [x] create the master document for project
- [x] create chapter about the use of gh
- [x] create chapter about BitBucket
- [x] correct error in master document creation
- [x] "release" should probably go away and be part of the "master" branch
- [x] refactor the document structure
- [ ] what this document is about
- [ ] git - workflow
- [ ] git - config / init / commit
- [ ] git - remote repositories
- [ ] git - pushing and pulling
- [ ] git - branches
- [ ] move some of the information from the gh chapter to the github chapter
- [ ] I don't know what the hell I'm saying here, Friendo
- [ ] create a QuickStart based on the information I have completed so-far
- [ ] create a chapter on the basic use of "git"
- [ ] create a chapter on the intermediate use of "git"
- [ ] create a chapter on GitKraken

***

[^1]:  Sooo... we gotta talk about BitBucket.

	Don't use BitBucket.  BitBucket was bought up by Atlassian and added to their platform.  I spent way too much time trying to get a push to work from the command line, much less trying to integrate it with GitKraken.  It's an inconvenience up with which one need not put when one has access to GitHub.

	Just use either GitHub or set up your own remote repository server (easier than you might think).

