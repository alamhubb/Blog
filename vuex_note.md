### vuex原理

1. #### 挂载方式
    * 在install中使用mixin将store挂载到项目中的每一个vue实例中，从而使开发者通过this.$store调用
2. #### 响应式原理
    * 为store添加一个vue实例属性_vm,将store.state挂载到_vm的data.$$state上，因vue实例data中的属性可以响应式，所以state中的属性也就可以响应式了。



