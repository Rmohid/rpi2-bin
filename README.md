# rpi2-bin
Various scripts or statically linked binaries for the raspberry pi 2.

Binaries weere compiled on rpi2 with [go 1.5](http://dave.cheney.net/2015/09/04/building-go-1-5-on-the-raspberry-pi)

Static linking is required for probrams using cgo, for swarm, [command used](http://blog.hypriot.com/post/let-docker-swarm-all-over-your-raspberry-pi-cluster/) was:

CGO_ENABLED=0 $(GOPATH)/bin/godep go install -v -a -tags netgo -installsuffix netgo -ldflags '-extldflags "-static" -s' .
