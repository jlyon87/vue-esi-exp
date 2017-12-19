<template>
	<div class="">
		<v-app :dark="isDark">
			<v-content>
				<v-container>
					<v-select
						label="Theme"
						v-model="selectedTheme"
						:items="themes"
						single-line
						bottom ></v-select>
				</v-container>
			</v-content>
		</v-app>
	</div>
</template>

<script>
export default {
	data() {
		return {
			selectedTheme: "dark",
			themes: [
				{ text: 'Dark', value: 'dark' },
				{ text: 'Light', value: 'light' }
			]
		}
	},
	computed: {
		isDark() {
			return this.selectedTheme === "dark";
		}
	}
}
</script>
