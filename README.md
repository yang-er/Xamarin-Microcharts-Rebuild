# Microcharts 自定义编译

由于直接fork他们代码，改版本号，会非常尴尬，于是……

```bash
$ mkdir OriginalSource
$ cd OriginalSource
$ git init
$ git remote add -f origin https://github.com/aloisdeniel/Microcharts.git
$ git config core.sparsecheckout true
$ echo >> .git/info/sparse-checkout <<EOF
> Sources/Microcharts.Forms
> Sources/Microcharts.Uwp
> Sources/Microcharts.Shared
> EOF
$ git pull origin master
$ cd ..
```

然后就可以用VS编译了？emmmmm

反正目的是为了让它用较新的库。