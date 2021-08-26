<template>
	<header>
		<h1>{{ title }}</h1>
		<Button
			:text="showAddTask ? 'Close' : 'Add Task'"
			:color="showAddTask ? 'red' : 'green'"
			@btn-click="$emit('toggle-btn')"
		/>
	</header>
</template>

<script>
import Button from './Button.vue'

export default {
	name: 'Header',
	props: {
		title: String,
		showAddTask: Boolean,
	},
	components: {
		Button,
	},
	emits: ['toggle-btn'],
}
</script>

<style scoped>
header {
	display: flex;
	justify-content: space-between;
	align-items: center;
	margin: 0 0 20px;
}
</style>
