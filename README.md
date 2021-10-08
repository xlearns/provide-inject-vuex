# provide-inject-vuex
- provide/inject代替vuex
- vuex4.x，store原理：当执行createApp.use(store)的时候，相当于注册了store插件，会执行store提供的install方法，内部通过provide把store挂载到根实例中，同时将store挂载到全局app.config.globalProperties.$store中,同时通过provide将修改store的方法挂载到实例中，这样当修改store的时候可以通过inject获取并触发方法
