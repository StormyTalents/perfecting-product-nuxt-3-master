<template>
    <div class="w-44 h-44 border-[10px] border-black shadow-lg">
        <div class="flex min-h-full justify-center items-center">
        <button :class="{ color }" @click="toggleColor" class="w-20 h-20 border-[10px] border-black bg-yellow-200 rounded-lg drop-shadow-[0_4px_4px_rgba(0,0,0,0.5)] hover:drop-shadow-none transition duration-200">
        </button>
        </div>
    </div>
</template>