# Bundle Kitty Channel

## Adding Your Project

1. Clone this repo.
2. Add your project details inline in the appropriate `.json` file (see below).
3. Validate your new `.json` file to ensure there are no typos.
4. Create a Pull Request.

## Project Types

#### `toolkit.json`

Toolkit engines, apps, and frameworks.

#### `shotgun.json`
  
Any non-Toolkit tools or scripts that utilize the Shotgun API. For example, any ORM, ActionMenuItem handlers, caching tools, etc. 

#### `shotgun_events.json`
  
Event daemon triggers and related tools. Triggers should be compatible with the [shotgunEvents](https://github.com/shotgunsoftware/shotgunEvents) project.


## Example schema

```
{
    "name": "tk-multi-foobar",
    "details": "https://github.com/kporangehat/tk-multi-foobar",
    "labels": ["foobar", "bar", "cupcakes"],
    "releases": "releases"
}
```

- `name`: The name of your project. 
- `details`: The full URL to your project's home on Github
- `labels`: Optional tags to help in classifying your project.
- `releases`: Defines how Bundle Kitty will detect releases of your project. Valid options are:
  
  - `releases`: (Default) Any Github Releases will be detected as a release to be listed (this does not include drafts or pre-releases)
  - `tags`: Tags will be treated as releases provided they are sematically versioned (https://semver.org/)
  - `branch:branchname`: The latest commit on the _`branchname`_ branch will be treated as the current version. Eg. `branch:master`.
