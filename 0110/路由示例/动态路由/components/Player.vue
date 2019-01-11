<template>
	<div>
		<h1>页面</h1>
		<p>{{detail}}</p>
	</div>
</template>

<script>
 export default {
        name: "Player",
        data () {
            return {
                detail: {}
            };
        },
        mounted () {
            // 接受url参数id
            this.detail = this.getPlayer(this.router.params.uid);
        },
        methods: {
            getPlayer(uid) {
                switch (uid) {
                    case '1':
                        return {uid: 1,name: '墨鱼',point: 26};
                    case '2':
                        return {uid: 2,name: '哈佛',point: 30};
                    default:
                        return {uid: -1};
                }
            }
        }
    };
</script>