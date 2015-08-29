# How to serve the current dir

There is probably a simpler way to do this, but this will serve the current directory.

```
require 'webrick'
server = WEBrick::HTTPServer.new( {:BindAddress => '0.0.0.0', :Port => 3000, :DocumentRoot => '.'})
server.start
```
