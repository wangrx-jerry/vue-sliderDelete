 <template>
     <div>
		<h1>LOGIN</h1>
		<h3>-By&nbsp;wrx</h3>
        <div class="input-box">
			<span class="input-placeholder">placeholder</span>
			<input type="text"  @focus="focusInput" @blur="blurInput">
		</div>
        <div class="input-box">
			<span class="input-placeholder">placeholder</span>
			<input type="text"  @focus="focusInput" @blur="blurInput">
		</div>
     </div>
</template>
<script>
  export default {
     data() {
     return { 
		}
	 },
     methods:{ 
		 focusInput (ev){
			 ev = ev || event;
			 ev.target.parentNode.classList.add("highlight");
			 if (ev.target.value === '') {
				 ev.target.parentNode.classList.add("move");
			 }
			 
			 
		 },
		 blurInput (ev) {
			 ev = ev || event;
			 ev.target.parentNode.classList.remove("highlight");
			 if (ev.target.value === '') {
				 ev.target.parentNode.classList.remove("move");
			 }
		 }   
     },
     components: { 
     }
}
</script>
<style scoped>
.input-box{position: relative; display: inline-block;width: 70%;height: 35px;transition: all .3s;border: 1px solid #918888;border-radius: 20px; margin-bottom: 15px;}
.input-placeholder{font-size: 12px; position: absolute;z-index: 1;top: 8px;left: 15px;transition: top .3s;background-color: #fff; }
.input-box > input{line-height: 35px;position: absolute;z-index: 2;top: 0;right: 0;bottom: 0;left: 0;width: 100%;padding: 0 10px; border: none;outline: none;background-color: transparent; }
.input-box.highlight{color: turquoise; border-color: turquoise; }
.input-box.move .input-placeholder{ top: -9px; }
</style>