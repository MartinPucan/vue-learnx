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
		<FullNameEditor />
	</div>
</template>

<script>

import FullNameEditor from "@/components/FullNameEditor";
export default {
	components: { FullNameEditor },
	data () {
		return {
			fullName: "CoSiZac"
		}
	}
}
</script>

<style scoped>

</style>
