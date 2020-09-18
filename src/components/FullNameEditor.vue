<template>
	<div>
		<h3>{{ firstName }} {{ lastName}}</h3>
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
		const [firstName = '', lastName = ''] = this.fullName.split(' ')
		return {
			firstName,
			lastName
		}
	},
	props: {
		fullName: {
			type: String,
			default: 'John Doe'
		}
	},
	watch: {
		fullName: function (newValue) {
			const [firstName = '', lastName = ''] = newValue.split(' ')
			this.firstName = firstName
			this.lastName = lastName
		}
	}
}
</script>

<style scoped>

</style>
