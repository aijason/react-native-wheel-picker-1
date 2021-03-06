# [0.2.3]() (2020-09-15)
* 修复并完善`DateRangePicker`组件及文档,修复[#9](https://github.com/yz1311/react-native-wheel-picker/issues/9)

# [0.2.2]() (2020-09-07)
* 移除不必要的`create-react-class`库，修复[#7](https://github.com/yz1311/react-native-wheel-picker/issues/7)

# [0.2.1]() (2020-08-28)(<font color="red">不要使用该版本，有严重bug</font>)
* 修复`DatePicker`对年份和月份处理有误
* `DatePicker`添加对错误参数的兼容处理 
* 修复`DatePicker`的ts定义

# [0.2.0]() (2020-08-27)
* 重写`DatePicker`组件，底层实现从`cascade`模式改为`parallel`模式，性能有了很大提升,有些默认行为发生了变化
  
> 1.minDate的默认值为改为当前日期的前30年(前面是10年)和后10年

> 2.在切换日期的时候，重置日期有一直默认为第一个变为动态改变
    譬如从2020-08-31滑动到2月份，会引起日期的重置，变为0-28,此时改为默认选中28号;如果是因为最小值和最大值引起的重置，则默认选中第一个

# [0.2.0-beta18]() (2020-07-30)
* 将所有的`componentWillReceiveProps`换成`componentDidUpdate`中实现
* 移除`DatePicker中`的propTypes校验

# [0.2.0-beta17]() (2020-07-30)

* 修复`DatePicker`必须要设置默认值并且dateime模式下数据有问题的bug
* 修复`DatePicker`中onDateChange改为非必选
* 移除`CommonPicker`中的componentWillReceiveProps方法(~~项目react版本在16.3以下的使用该版本会报错~~)