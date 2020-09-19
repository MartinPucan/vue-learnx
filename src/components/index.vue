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

.alert {
	max-width: 550px;
	position:  relative;
	padding: 10px 20px 10px 10px;
	margin:  10px auto;
	border-radius: 10px;
	background-color: #faf8df;
	border: 2px solid #f5c340;
	border-left-width: 40px;
}
.alert:before {
	content: '\f071';
	/*position: absolute;*/
	left: -27px;
	top: 50%;
	transform: translateY(-50%);
	color: #fff;
}
.alert .close {
	position:  absolute;
	right: 8px;
	cursor:  pointer;
	top: 10px;
	color: #999;
}

</style>
