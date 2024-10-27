<template>
	<div class="flex flex-col justify-center items-center font-poppins mt-2">
		<h1 class="flex flex-col items-center text-xl">
			<img class="w-32"  src="~/assets/img/logo.png" alt="Logo">
			<span class="text-2xl">Ondokuz Mayıs Üniversitesi</span>
			<span class="text-2xl">Kimya Mühendisliği</span>
			<span class="text-xl">Proses Topluluğu</span>
		</h1>
		
		<div class="mt-6 flex flex-col justify-center items-center">
			<div class="text-xl">Sponsorlarımız</div>
			<div class="text-gray-500 text-xs">İndirimli kampanyalardan yararlanabilirsiniz!</div>
		</div>
		
		<div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-[5px] mt-4">
			<div
			v-for="(cafe, index) in cafes"
			:key="index"
			class="relative w-96 rounded overflow-hidden group"
			>
			<img class="w-full h-64 object-cover" :src="cafe.image" :alt="cafe.name">
			
			<!-- Düz Hali -->
			<div class="absolute inset-0 bg-black bg-opacity-60 flex items-center justify-center transition-opacity duration-300 group-hover:opacity-0">
				<span class="text-white text-lg">{{ cafe.name }}</span>
			</div>
			
			<!-- Hover efekti -->
			<div class="absolute inset-0 bg-black bg-opacity-80 flex items-center justify-center opacity-0 group-hover:opacity-100 transition-opacity duration-300">
				<span class="text-white text-lg"> {{ cafe.yazi }} </span>
			</div>
		</div>
	</div>
	
	<!-- Sosyal Medya -->
	<div class="mt-10">
		Bizi sosyal medyada takip edin!
	</div>
	<div class="flex justify-center items-center space-x-4">
		<a href="https://instagram.com/omuproses" target="_blank" class="text-pink-500">
			<Icon name="uil-instagram" class="h-10 w-10" />
		</a>
		<a href="https://www.youtube.com/@prosestoplulugu2555" target="_blank" class="text-red-500">
			<Icon name="uil-youtube" class="h-10 w-10" />
		</a>
		<a href="https://www.linkedin.com/company/proses-toplulu%C4%9Fu/" target="_blank" class="text-blue-500">
			<Icon name="uil-linkedin" class="h-10 w-10" />
		</a>
	</div>
	
	
</div>
</template>

<script setup>
import { ref } from 'vue';

const cafes = ref([
{
	name: "Cafe 1",
	yazi: "Cafe 1 kafesinde %10 indirim",
	image: "https://www.yapikatalogu.com/Files/Project/571/file-3216.jpg",
},
{
	name: "Cafe 2",
	yazi: "Cafe 2 kafesinde %15 indirim",
	image: "https://i.pinimg.com/564x/98/ff/1f/98ff1f34046a7e1a0f112a5a1856050e.jpg",
},
{
	name: "Cafe 3",
	yazi: "Cafe 3 kafesinde %20 indirim",
	image: "https://www.yapikatalogu.com/Files/Project/571/file-3216.jpg",
},
{
	name: "Cafe 4",
	yazi: "Cafe 4 kafesinde %25 indirim",
	image: "https://www.yapikatalogu.com/Files/Project/571/file-3216.jpg",
},
]);
</script>
