# BlockChains
learn and practise Blockchains

use

https://github.com/chainHero/heroes-service-network

learn how to build a network, then use

https://github.com/chainHero/heroes-service

to test a sdk-go

change dep to go mod 

目前看来，用mod管理依赖很简单，先输入 export GO111MODULE=on
1. 	在main.go所在的目录，输入go mod init XX, 就可以生成初始的go.mod文件，一定输入XX表示模块的名字，任意起名。
2. 	在main.go所在的目录，输入go build或者go mod tidy，就会按照main.go中的imports在go.mod中生成依赖关系以及go.sum文件。
	2.1	如果没有对应的包，就会进行下载。这里有个坑，就是由于开发的原因，某个包不见了，那么就要查找含有这个包的版本进行下载，加入repalce语句，或者用新版的release重新写，如replace google.golang.org/grpc => google.golang.org/grpc v1.26.0
	go build成功后会生成XX的可执行文件，./XX就可以运行，但是一定要启动对应的平台，比如网络等。
	2.2	golang的准标准库golang.org/x在国内无法直接访问，需要代理才行，我们可以replace到github的目录。
3.	可以用go mod vendor语句将所依赖的包放入vendor文件夹，这样就不用重新下载包了，vendor一定要放在链码的.go文件所在文件夹里面


中文版的可以参考

https://github.com/kevin-hf/kongyixueyuan

