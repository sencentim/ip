﻿17MonIP Golang Lib
======

IP search based on 17monipdb, the IP database parser for china with golang.


install
--------

	 go get github.com/axgle/ip

example
-------

	package main
	
	import "github.com/axgle/ip"
	
	func main() {
		ip.Load("../17monipdb.dat")
	
		address := ip.Find("8.8.8.8") //address: GOOGLE\tGOOGLE\t
		println(address)
	
		address = ip.Find("202.106.46.151") //address: 中国\t北京\t
		println(address)
	
		address = ip.Find("202.115.128.64") //address: 中国\t四川\t成都理工大学
		println(address)
	
	}


## License

BSD

## Version

0.0.3 update 17monipdb.dat for more detail info and add  Paul Gao's php parse

0.0.2 remove binary package

0.0.1 init release.

## Thanks

* Paul Gao: for his 17monipdb.dat data.