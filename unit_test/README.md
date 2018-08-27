开发日期：20180824
开发人员：hezhixiong
功能介绍：使用 goconvey 包进行单元测试
参考文档：{
    1. go walker for goconvey：https://gowalker.org/github.com/smartystreets/goconvey
    2. https://www.jianshu.com/p/e3b2b1194830
}

使用方法：
1. 命令行方式的单元测试：go test -v
2. Web界面方式的单元测试：goconvey

goconvey 使用小结：
1. import goconvey包时，前面加点号"."，以减少冗余的代码；
2. 测试函数的名字必须以Test开头，而且参数类型必须为*testing.T；
3. 每个测试用例必须使用Convey函数包裹起来，推荐使用Convey语句的嵌套，即一个函数有一个测试函数，
   测试函数中嵌套两级Convey语句，第一级Convey语句对应测试函数，第二级Convey语句对应测试用例；
4. Convey语句的第三个参数习惯以闭包的形式实现，在闭包中通过So语句完成断言；
5. 使用GoConvey框架的 Web 界面特性，作为命令行的补充；
6. 在适当的场景下使用SkipConvey函数或SkipSo函数；
7. 当测试中有需要时，可以定制断言函数。
