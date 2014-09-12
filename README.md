# PublicDB

## (WIP) still organizing thoughts

The idea behind this is to create a self replicating shapeless database. all configuration and organization will be done using ethereum and etcd.

# Getting Started

## 1. Install `repo`
`repo` is a tool developed by [Google](https://chromium.googlesource.com/external/repo) to make development on multiple repositories much easier. duralog will eventually integerate this with heavyk's work on Laboratory.

1. OSX: `brew install repo` (if you don't have brew installed [find out how to do it here](http://brew.sh))
2. Linux: [Get depot_tools](http://www.chromium.org/developers/how-tos/install-depot-tools).
3. *Windows currently not supported*

## 2. Download Release Version

```
mkdir PublicDB
cd PublicDB
repo init -u https://github.com/duralog/PublicDB.git \
  --repo-url https://github.com/duralog/repo.git \
  --no-repo-verify --depth=1
repo sync
npm install
```

that last option, `--depth=1` is optional, but it'll clone the repositories in a lot less time.

## 3. Upgrade to the the development version and begin contributing

### Convert to deep commit history

```
repo forall -c git fetch --unshallow
repo sync
```

## 4. Stay up to date
these commands are sufficient to upgrade to the latest version
```
git -C .repo/repo pull
repo sync
npm install
```

# Contribute
contribute your ideas, at least, and if they're any good, we'll figure out how to get them coded.
