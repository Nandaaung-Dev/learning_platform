<template>
	<div>
		<div class="flex justify-between p-2 bg-slate-200 text-white">
      <div>
        <NuxtLink to='/' class="p-2 bg-blue-500 text-white rounded items-end">Home</NuxtLink>
      </div>
			<div>
        <NuxtLink to='/login' class="p-2 bg-blue-500 text-white rounded" v-if="!$auth.loggedIn">Login</NuxtLink>
        <NuxtLink to='/register' class="p-2 bg-blue-500 text-white rounded" v-if="!$auth.loggedIn">Register</NuxtLink>
        <NuxtLink to='/dashboard' class="p-2 bg-blue-500 text-white rounded"
          v-if="$auth.loggedIn">Dashboard</NuxtLink>
      </div>
		</div>
		<Nuxt />
	</div>
</template>
<script>
	export default{
		auth:false
	}
</script>

