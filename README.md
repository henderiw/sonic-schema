# sonic schema

this repo holds a sonic schema for use with SDCIO. this is an example repo and is not keeping track of the latest changes that SONiC is making

## how to build/update a sonic schema in this repo

generate the yang schema from the sonic build image

```
rm -rf yang-models
rm -rf tmp;mkdir tmp;cd tmp
git clone https://github.com/sonic-net/sonic-buildimage
cd sonic-buildimage/src/sonic-yang-models;python setup.py install 
cd ../../../..
cp -r tmp/sonic-buildimage/src/sonic-yang-models/yang-models .
rm -rf tmp
```
The ietf module dependencies are manually put here

## genrating a naked yaml from a yang model

gnmic generate --file yang-models --dir ietf --path / > sonic.yaml