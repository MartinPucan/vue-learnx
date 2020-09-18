<template>
	<div>
		<p>{{ firstName }} {{ lastName}}</p>
		<p>
			<label>First name<br>
				<input
						type="text"
						v-model="firstName"
				>
			</label>
		</p>
		<p>
			<label>Last name<br>
				<input
						type="text"
						v-model="lastName"
				>
			</label>
		</p>
	</div>
</template>

<script>
export default {
	name: "FullNameEditor",
	data () {
		return {
			firstName: "Martin",
			lastName: "Pucan"
		}
	}
}
</script>

<style scoped>

</style>
