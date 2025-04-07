# @seal.run/plate-indent-list

Seal's fork of @udecode/plate-indent-list, which adds hierarchical numbered list and 
arbitrary restarts functionality.

Our npm module is here: https://www.npmjs.com/package/@seal.run/plate-indent-list


## What's this repo about?

It's nicer to fork the plate code rather than copying it into our own repo - makes it
easier to maintain. We can then publish our modified version of the indent-list package to 
npm (public!), so we can easily install it.

Plate's code is a monorepo, so to publish our own version of the indent list package, we
need to fork the whole plate repo.

## How to release a new version of @seal.run/plate-indent-list

1. bump the version number in `packages/indent-list/package.json` (see [this commit](https://github.com/opvia/plate/pull/5/commits/4f324ed1402b66ebbb44b7d3ce9b849c6cbc318d))
2. `HOME=/Users/yourname NODE_AUTH_TOKEN=get_from_npm NPM_TOKEN=get_from_npm yarn release`
   - this first builds every plate package
   - and then compares each package's version number against the one already in npm. So if 
    you've only bumped the version in `/indent-list`, only that package will be released 
    (it's the only package configured to be released in the @seal.run npm org)
   - N.B. there's only one token, obtained from npm - for some reason you pass it to `NODE_AUTH_TOKEN`
     and `NPM_TOKEN`


## TODO

- [ ] get tests running in a github action
- [ ] fix tests
- [ ] add tests for our changes (hierarchical numbered lists)



