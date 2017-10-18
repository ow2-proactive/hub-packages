Hub Packages
============

## Introduction

This repository includes the public packages hosted on [hub.activeeon.com](http://hub.activeeon.com/). Do not hesitate to share your own. If your pack might be useful to more people than just yourself, we would be happy to include it. Don't worry if your code isn't perfect or is incomplete. We will organize ourselves to come and help.

All the other packages fully supported by the ActiveEon's team are available on [this repo](https://github.com/ow2-proactive/proactive-examples).

## Create and Contribute

Ready to contribute to our community and share your own workflows.

A package as a defined structure that needs to be followed to be included into the hub. Below, the main rules are described, we tried to keep it simple for easier contribution.

### Package Structure

```bash
METADATA.json           # information required to be included in the hub
README.md               # optional information about the package (e.g. description of the workflows, of the Dockerfiles, etc.)
resources/catalog       # all workflows
resources/dataspace     # all files to be included in the dataspace
resources/dockerfile    # all Dockerfiles user in a fork environment
resources/jar           # all jar dependencies used within the workflows 
```

### Metadata Structure

```json
{
	"metadata": {
		"slug": "a-slug-name",
		"name": "Your Package name",
		"short_description": "A line describing your package and purpose",
		"author": "Your company/name",
		"tags": ["tag1", "tag2", "tag3"],
		"version": "0.0.1"
	},
	"catalog": {
		"bucket": "name of the bucket in ProActive containing the package (Finance, Cloud Automation, ...)",
		"objects": [
			{
				"name":"name to display",
				"metadata": {
					"kind": "kind of file (workflow, pcw-rule, ...)",
					"commitMessage": "message of the last commit",
					"contentType":"media type (application/wml, image/png, ...)"
				},
				"file":"relative/path/to/this/file"
			}
		]
	}
}
```
You can find examples of metadata files in the GitHub repository of existing packages.
Do not hesitate to go on the hub to use similar tags than existing packages. This will help searches.

## Submit your Package

Now that you have a fully functioning package, let's share it with the community. [ActiveEon's Hub](http://hub.activeeon.com/) is the place where packages are easily shared between users and where you can find your next workflows to help you build faster.

The last step is a standard pull request on this specific repository. If you are not familiar with github, we suggest this [tutorial](https://try.github.io/levels/1/challenges/1) and these two guides to help you with a pull request: [guide 1](https://guides.github.com/activities/forking/) and [guide 2](https://guides.github.com/activities/forking/).

### Get Started

Do not hesitate to go through the folders on [ProActive Examples](https://github.com/ow2-proactive/proactive-examples) to explore some examples. Then, when you feel ready, clone this repository and copy paste the folder [package-sample](https://github.com/ow2-proactive/hub-packages/tree/master/package-sample) to get started.

## Licence Agreement for Contributors

By contributing you agree that these contributions are your own (or approved by your employer) and you grant a full, complete, irrevocable copyright license to all users and developers of the project, present and future, pursuant to the license of the project.
