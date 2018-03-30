<template>

<div>
<table>
<!--<tr>
<td>内容1</td>
<td>内容2</td>
<td>内容3</td>
</tr>-->
<tr v-for="i in arr">
<td>{{i.id|zongshu}}</td>
<td>{{i.tit|zongshu}}</td>
<td>{{i.con|zongshu}}</td>
</tr>

</table>

</div>
</template>

<script>
	
	
	export default {
		data(){
			return{
				
				arr:[]
			}
			
		},
		created(){
			this.$http.get("http://localhost:8000").then(e=>this.arr=e.body)
		}
		}
		
	
	
</script>

<style>
</style>