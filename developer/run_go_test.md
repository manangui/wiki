# True链开发准备篇-调通测试代码，执行单元测试#
关于True链的开发环境，目前支持Windows，MacOS,Linux,本篇主要是针对在Windows环境上搭建作一个详细说明。

### 运行go test -v来运行go测试代码 ###
go test执行会自动检查当前目录下的测试模块和代码，并自动加载执行。
truechain fpow当前项目有如下测试模块：TestBlockchain、TestDifficulty、TestRLP、TestState、TestTransaction、TestVM。
执行完毕会给出测试结果。初学者可以通过学习运行和学习测试代码尽快进入到项目。
以Windows平台为例：
运行命令：cd tests，切换到\tests目录下，再运行命令： go test -v 。
如果发现部分pacakge不全的话，可以运行go get [pacakage]命令获取指定pacakge。
如果发现报错gcc编译报错问题，可以按照帮助文档“Window环境搭建”章节检查是否正确安装MinGW。
如果发现找不到文件错误，类似如“can't find test files in testdata\TransactionTests, did you clone the tests submodule?”
按照英文提示可以直接在testdata目录下创建“TransactionTests”目录，即可解决问题。
再次运行go test -v。检查运行结果，直到全部通过测试。
全部通过测试的执行结果见如下：
--- PASS: TestState (0.00s)
--- PASS: TestBlockchain (0.00s)
--- PASS: TestTransaction (0.00s)
--- PASS: TestVM (0.00s)
--- PASS: TestRLP (0.00s)
--- PASS: TestDifficulty (0.00s)
PASS
ok  表明5个测试模块全部通过测试。
### 补充 ###
	鉴于各人的开放环境及配置不同，可能会碰到其他不能正常通过go test测试情况，建议大家要多利用搜索，先尝试自己解决。
如果还有问题，可以提issue，或者在线联系本人（通过13621629235手机号码添加微信好友即可）。