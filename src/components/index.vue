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
		<FullNameEditor v-bind:fullName="fullName" />
	</div>
</template>

<script>

import FullNameEditor from "@/components/FullNameEditor";
export default {
	components: { FullNameEditor },
	data () {
		return {
			fullName: "Karel Gott"
		}
	}
}
</script>

<style scoped>

</style>
