# sonic schema

this repo holds a sonic schema for use with SDCIO

## how to build a sonic schema

generate

```
rm -rf yang-models
rm -rf tmp;mkdir tmp;cd tmp
git clone https://github.com/sonic-net/sonic-buildimage
cd sonic-buildimage/src/sonic-yang-models;python setup.py install 
cd ../../../..
cp -r tmp/sonic-buildimage/src/sonic-yang-models/yang-models .
rm -rf tmp
```
