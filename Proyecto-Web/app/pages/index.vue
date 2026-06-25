<script setup lang="ts">
const email = ref('')
const password = ref('')

const handleLogin = async () => {
  console.log(email.value, password.value)
}
</script>

<template>
  <div class="flex flex-col items-center justify-center min-h-screen bg-slate-900">
    <h1 class="text-7xl font-bold text-center py-8 text-white">
      Smart Events
    </h1>

    <div class="w-full max-w-sm bg-white shadow-md rounded-lg p-6">
      <h2 class="text-xl font-semibold mb-4 text-center text-gray-900">
        Iniciar sesión
      </h2>

      <form @submit.prevent="handleLogin" class="flex flex-col gap-4">
        <div class="flex flex-col gap-1">
          <label for="email" class="text-sm font-medium text-gray-700">Email</label>
          <input
            id="email"
            v-model="email"
            type="email"
            placeholder="usuario@gmail.com"
            class="border border-gray-300 rounded-md px-3 py-2 text-gray-900 placeholder-gray-400 focus:outline-none focus:ring-2 focus:ring-blue-500"
            required
          />
        </div>

        <div class="flex flex-col gap-1">
          <label for="password" class="text-sm font-medium text-gray-700">Contraseña</label>
          <input
            id="password"
            v-model="password"
            type="password"
            placeholder="••••••••"
            class="border border-gray-300 rounded-md px-3 py-2 text-gray-900 placeholder-gray-400 focus:outline-none focus:ring-2 focus:ring-blue-500"
            required
          />
        </div>

        <button
          type="submit"
          class="bg-blue-600 text-white rounded-md py-2 mt-2 hover:bg-blue-700 transition"
        >
          Ingresar
        </button>
      </form>
    </div>
  </div>
</template>