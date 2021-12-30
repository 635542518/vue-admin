<template>
    <div>
        <div class="login">
            <div class="login-wrap">
                <ul class="login-top">
                    <li v-for="item in menuTab" :key="item.id" :class="{'current': item.current}" @click="toggleMneu(item)">{{item.txt}}</li>
                </ul>
            </div>
        </div>
    </div>
</template>
<script>
export default {
    name: 'login',
    data() {
        return {
          menuTab: [
            {txt: '登录', current: true},
            {txt: '注册', current: false}
          ],
          isActive: true
        };
    },
    created() {},
    mounted() {},
    methods: {
      //在vue里是用数据驱动视图渲染
      // 写函数的地方
      toggleMneu(data) {
        console.log(data);
      }
    },
    props: {},
    eatch: {},
};
</script>
<style lang="scss" scoped>
.login {
    background: #344a5f;
    height: 100vh;
}
.login-top {
    text-align: center;
    li {
        display: inline-block;
        width: 115px;
        line-height: 36px;
        color: #fff;
        border-radius: 2px;
        cursor: pointer;
        // cursor: progress;指针在转
    }
    .current {
      background: rgba(0,0,0,.1);
    }
}
</style>
