<template>
	<div>
		<h3>{{ joinedName }}</h3>
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
		const [firstName = '', lastName = ''] = this.value.split(' ')
		return {
			firstName,
			lastName
		}
	},
	props: {
		value: {
			type: String,
			default: 'John Doe'
		}
	},
	computed: {
		joinedName () {
			return [this.firstName, this.lastName]
					.filter(value => value !== '')
					.join(' ')
		}
	},
	watch: {
		value: function (newValue) {
			const [firstName = '', lastName = ''] = newValue.split(' ')
			this.firstName = firstName
			this.lastName = lastName
		},
		joinedName: function () {
			this.$emit('input', this.joinedName)
		}
	}
}
</script>

<style scoped>

</style>
