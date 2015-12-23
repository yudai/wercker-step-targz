Wercker step targz [![MIT License](http://img.shields.io/badge/license-MIT-blue.svg?style=flat)](https://github.com/yudai/wercker-step-targz/blob/master/LICENCE)
====

[![wercker status](https://app.wercker.com/status/2731ce0d44665102c1255e2029185029/m "wercker status")](https://app.wercker.com/project/bykey/2731ce0d44665102c1255e2029185029)

This is [wercker](http://wercker.com/) build step script to package your directories as `.tar.gz`. 

## Usage

In the `wercker.yml` of your application use the following step definition:

```yaml
steps:
   - yudai/targz:
     input: $WERCKER_OUTPUT_DIR/pkg
     output: $WERCKER_OUTPUT_DIR/dist
```

You must set `input` directory where directories you want to package are in and `output` directory where zip archives will be generated. Both must be set as absolte path (`$WERCKER_OUTPUT_PATH` is built-in environmental valiable which is used for pass the artifacts between build step and deploy step). 

## Author

* [yudai](https://github.com/yudai)
* [tcnksm](https://github.com/tcnksm) (Original .zip version)
