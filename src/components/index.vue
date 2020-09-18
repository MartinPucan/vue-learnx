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
				v-bind:fullName="fullName"
				v-on:nameChange="handleNameChange"
		/>
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
	},
	methods: {
		handleNameChange (newName) {
			this.fullName = newName
		}
	}
}
</script>

<style scoped>

</style>
