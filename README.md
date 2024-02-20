# Cvfying

## Branch strategies
- use `main` branch to sync with [original repo](https://github.com/claudiabdm/cvfy),
- create feature branches to develop new features,
- create PR from feature branches to original repo,
- merge features from feature branches to `dev` branch, `dev` branch always hosts the full features.

## Build Setup

```bash
# install dependencies
$ yarn

# serve with hot reload at localhost:3000
$ yarn dev

# build for production and launch server
$ yarn build
$ yarn start

# generate static project
$ yarn generate
```

## Containerization
use `dockering.sh` to generate images:
> when create image, remove `node_modules` before build
```bash
# create image
./dockering.sh build 0.0.3

# tag image
./dockering.sh tag 0.0.3

# push image
./dockering.sh push 0.0.3

# run container
docker container run -d -p 4300:4300 --name cvering cvering:0.0.3
```
