 <template>
     <div>
		<h1> 这是一个移动端侧滑删除组件demo </h1>
		<h3>-By&nbsp;wrx</h3>
        <delete-slider v-for="(list, index) in dataList" :key="index" @deleteLine="deleteLine">
          <h1 slot="line">{{'line' + (index + 1)}}</h1>
          <h2>{{list.name}}</h2>
        </delete-slider> 
     </div>
</template>
<script>
import deleteSlider from '@/components/deleteTemplate.vue' 
  export default {
     data() {
     return {
		dataList: [
			{name: 'name'},
			{name: 'name2'},
			{name: 'name3'},
			]
		}
	 },
     methods:{
        deleteLine (index){
			this.dataList.splice(index, 1)
		}      
     },
     components: {
        deleteSlider
     }
}
</script>
<style scoped>
</style>