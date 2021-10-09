# provide-inject-vuex
- provide/inject代替vuex
- vuex4.x，store原理：当执行createApp.use(store)的时候，相当于注册了store插件，会执行store提供的install方法，内部通过provide把store挂载到根实例中，同时将store挂载到全局app.config.globalProperties.$store中,同时通过provide将修改store的方法挂载到实例中，这样当修改store的时候可以通过inject获取并触发方法。本质来说，provide/inject是可以实现vuex的数据共享能力的，但是vuex除了共享状态能力还具备模块、插件、严格模式等功能。一般来说provide/inject的应用场景组件库，对于一个特定的组件，上下联系比较密切就可以通过provide/inject来实现状态共享。Vuex 和 provide/inject 最大的区别在于，Vuex 中的全局状态的每次修改是可以追踪回溯的，而 provide/inject 中变量的修改是无法控制的，换句话说，你不知道是哪个组件修改了这个全局状态
