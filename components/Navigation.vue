<template>
  <header class="flex flex-col md:flex-row justify-between items-center py-4 px-8 bg-gray-800">
    <div class="flex items-center">
      <img src="logo.png" alt="Logo" class="w-12 h-12">
      <h3 class="text-white text-2xl ml-4">Movie App</h3>
    </div>
    <div class="flex items-center md:hidden">
      <button class="text-white focus:outline-none">
        <svg class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg">
          <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 6h16M4 12h16M4 18h16"></path>
        </svg>
      </button>
    </div>
    <div class="hidden md:block">
      <input type="text" class="bg-gray-800 p-2 rounded-full text-white w-64 focus:outline-none" placeholder="Search">
    </div>
    <nav class="flex items-center">
      <ul class="flex text-white">
        <li class="px-4">
          <a href="#">Categories</a>
        </li>
        <li class="px-4">
          <a href="#">Movies</a>
        </li>
        <li class="px-4">
          <a href="#">TV Shows</a>
        </li>
        <li class="px-4">
          <a href="#">Login</a>
        </li>
      </ul>
    </nav>
  </header>
</template>