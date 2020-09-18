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
3.	可以用go mod vendor语句将所依赖的包放入vendor文件夹，这样就不用重新下载包了，vendor一定要放在链码的.go文件所在文件夹里面 


中文版的可以参考

https://github.com/kevin-hf/kongyixueyuan

