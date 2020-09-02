你好！
很冒昧用这样的方式来和你沟通，如有打扰请忽略我的提交哈。我是光年实验室（gnlab.com）的HR，在招Golang开发工程师，我们是一个技术型团队，技术氛围非常好。全职和兼职都可以，不过最好是全职，工作地点杭州。
我们公司是做流量增长的，Golang负责开发SAAS平台的应用，我们做的很多应用是全新的，工作非常有挑战也很有意思，是国内很多大厂的顾问。
如果有兴趣的话加我微信：13515810775  ，也可以访问 https://gnlab.com/，联系客服转发给HR。
# bosun

Bosun is a time series alerting framework developed by Stack Exchange. Scollector is a metric collection agent. Learn more at [bosun.org](http://bosun.org).

[![Build Status](https://travis-ci.org/bosun-monitor/bosun.svg?branch=master)](https://travis-ci.org/bosun-monitor/bosun/branches)

## building

To build bosun and scollector, clone to `$GOPATH/src/bosun.org`:

```
$ go get bosun.org/cmd/bosun
```

bosun and scollector are found under the `cmd` directory. Run `go build` in the corresponding directories to build each project.

## developing

Install:

* `npm install typescript@<version> -g` to be able to compile the ts files to js files. The current version of typescript to install will be in the `.tavis.yml` file in the root of this repo.
* `go get github.com/mjibson/esc` to embed the static files. Run `go generate` in `cmd/bosun` when new static assets (like JS and CSS files) are added or changed.

The `w.sh` script will automatically build and run bosun in a loop.
It will update itself when go/js/ts files change, and it runs in read-only mode, not sending any alerts.

```
$ cd cmd/bosun
$ ./w.sh
```

Go Version:
  * See the version number in `.travis.yml` in the root of this repo for the version of Go to use. Generally speaking, you should be able to use newer versions of Go if you are able to build Bosun without error.
  
Miniprofiler:
 * Bosun includes [miniprofiler](https://github.com/MiniProfiler/go) in the web UI which can help with debugging. The key combination `ALT-P` will show miniprofiler. This allows you to see timings, as well as the raw queries sent to TSDBs.
