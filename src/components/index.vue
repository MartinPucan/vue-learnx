<template>
	<div class="wrapper">
		<p>{{ fullName }}</p>
		<p>
			<label>Full name<br>
				<input
						type="text"
						v-model="fullName"
				>
			</label>
		</p>
		<FullNameEditor
				v-model="fullName"
		/>
		<div class="alert">
			<b>Warning:</b> this is the text you want to show as a warning message.
			<span class="close">&times;</span>
		</div>
	</div>
</template>

<script>

import FullNameEditor from "@/components/FullNameEditor";
export default {
	components: { FullNameEditor },
	data () {
		return {
			fullName: "John Doe"
		}
	}
}
</script>

<style scoped>

</style>
