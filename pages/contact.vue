<template>
  <div class="relative">
    <div class="w-full bg-cover bg-center rounded-lg md:h-[576px] h-[450px] bg-[url('/contact.jpg')]">
      <div class="flex items-center justify-center h-full w-full bg-gray-900 bg-opacity-50 rounded-lg">
        <div class="text-center">
          <h1 class="text-white text-2xl font-semibold md:text-3xl">
            Ha felkeltettük érdeklődését vagy kérdése van, keressen minket!
          </h1>
        </div>
      </div>
    </div>

    <div class="container mx-auto relative z-10">

      <form @submit.prevent="onSubmit" @reset="onReset" class="w-full lg:w-1/2 mt-[-100px] bg-white rounded-lg p-6 shadow-lg mx-auto">


        <div class="mb-6 text-center text-2xl">
          <p class="mb-10"><strong>Elérhetőségeink</strong></p>
          <div class="mb-6 flex items-center justify-center">
            <div class="flex flex-col items-center mr-4">
              <svg
                class="w-6 h-6 text-sky-400 dark:text-gray-400"
                aria-hidden="true"
                xmlns="http://www.w3.org/2000/svg"
                fill="currentColor"
                viewBox="0 0 20 20"
              >
                <path
                  d="M12 0H2a2 2 0 0 0-2 2v16a2 2 0 0 0 2 2h10a2 2 0 0 0 2-2V2a2 2 0 0 0-2-2ZM7.5 17.5h-1a1 1 0 0 1 0-2h1a1 1 0 0 1 0 2ZM12 13H2V4h10v9Z"
                ></path>
              </svg>
              <p class="text-gray-900 dark:text-white text-sm">
                Telefon: 30/248-6910
              </p>
            </div>
            <div class="flex flex-col items-center">
              <svg
                class="w-6 h-6 text-sky-400 dark:text-gray-400"
                aria-hidden="true"
                xmlns="http://www.w3.org/2000/svg"
                fill="currentColor"
                viewBox="0 0 20 16"
              >
                <path
                  d="m10.036 8.278 9.258-7.79A1.979 1.979 0 0 0 18 0H2A1.987 1.987 0 0 0 .641.541l9.395 7.737Z"
                ></path>
                <path
                  d="M11.241 9.817c-.36.275-.801.425-1.255.427-.428 0-.845-.138-1.187-.395L0 2.6V14a2 2 0 0 0 2 2h16a2 2 0 0 0 2-2V2.5l-8.759 7.317Z"
                ></path>
              </svg>
              <p class="text-gray-900 dark:text-white text-sm">
                Email: k13mester@gmail.com
              </p>
            </div>
          </div>
          <p class="text-xl">Vagy töltse ki az alábbi mezőket!</p>
        </div>


        <label for="name" class="block mb-2 text-sm font-medium text-gray-900 dark:text-white">Név</label>
        <div class="relative mb-6">
          <span class="absolute inset-y-0 left-0 flex items-center pl-3.5 pointer-events-none">
            <svg
              class="w-4 h-4 text-gray-500 dark:text-gray-400"
              aria-hidden="true"
              xmlns="http://www.w3.org/2000/svg"
              fill="currentColor"
              viewBox="0 0 20 20"
            >
              <path
                d="M10 0a10 10 0 1 0 10 10A10.011 10.011 0 0 0 10 0Zm0 5a3 3 0 1 1 0 6 3 3 0 0 1 0-6Zm0 13a8.949 8.949 0 0 1-4.951-1.488A3.987 3.987 0 0 1 9 13h2a3.987 3.987 0 0 1 3.951 3.512A8.949 8.949 0 0 1 10 18Z"
              ></path>
            </svg>
          </span>
          <input
            type="text"
            id="name"
            v-model="name"
            class="bg-gray-50 border border-gray-300 text-gray-900 text-sm rounded-lg focus:ring-blue-500 focus:border-blue-500 block w-full pl-10 p-2.5  dark:bg-gray-700 dark:border-gray-600 dark:placeholder-gray-400 dark:text-white dark:focus:ring-blue-500 dark:focus:border-blue-500"
            placeholder="Név"
            required
          />
        </div>

        <label for="email" class="block mb-2 text-sm font-medium text-gray-900 dark:text-white">Email cím</label>
        <div class="relative mb-6">
          <div class="absolute inset-y-0 left-0 flex items-center pl-3.5 pointer-events-none">
            <svg
              class="w-4 h-4 text-gray-500 dark:text-gray-400"
              aria-hidden="true"
              xmlns="http://www.w3.org/2000/svg"
              fill="currentColor"
              viewBox="0 0 20 16"
            >
              <path
                d="m10.036 8.278 9.258-7.79A1.979 1.979 0 0 0 18 0H2A1.987 1.987 0 0 0 .641.541l9.395 7.737Z"
              ></path>
              <path
                d="M11.241 9.817c-.36.275-.801.425-1.255.427-.428 0-.845-.138-1.187-.395L0 2.6V14a2 2 0 0 0 2 2h16a2 2 0 0 0 2-2V2.5l-8.759 7.317Z"
              ></path>
            </svg>
          </div>
          <input
            type="email"
            id="email"
            v-model="email"
            class="bg-gray-50 border border-gray-300 text-gray-900 text-sm rounded-lg focus:ring-blue-500 focus:border-blue-500 block w-full pl-10 p-2.5  dark:bg-gray-700 dark:border-gray-600 dark:placeholder-gray-400 dark:text-white dark:focus:ring-blue-500 dark:focus:border-blue-500"
            placeholder="név@email.hu"
            required
          />
        </div>

        <label for="phone" class="block mb-2 text-sm font-medium text-gray-900 dark:text-white">Telefonszám</label>
        <div class="relative mb-6">
          <div class="absolute inset-y-0 left-0 flex items-center pl-3.5 pointer-events-none">
            <svg
              class="w-4 h-4 text-gray-500 dark:text-gray-400"
              aria-hidden="true"
              xmlns="http://www.w3.org/2000/svg"
              fill="currentColor"
              viewBox="0 0 20 22"
            >
              <path
                d="M12 0H2a2 2 0 0 0-2 2v16a2 2 0 0 0 2 2h10a2 2 0 0 0 2-2V2a2 2 0 0 0-2-2ZM7.5 17.5h-1a1 1 0 0 1 0-2h1a1 1 0 0 1 0 2ZM12 13H2V4h10v9Z"
              ></path>
            </svg>
          </div>
          <input
            type="text"
            id="phone"
            v-model="phone"
            class="bg-gray-50 border border-gray-300 text-gray-900 text-sm rounded-lg focus:ring-blue-500 focus:border-blue-500 block w-full pl-10 p-2.5  dark:bg-gray-700 dark:border-gray-600 dark:placeholder-gray-400 dark:text-white dark:focus:ring-blue-500 dark:focus:border-blue-500"
            placeholder="+36..."
            required
          />
        </div>

        <div class="relative mb-6">
          <label for="message" class="block mb-2 text-sm font-medium text-gray-900 dark:text-white">Üzenet</label>
          <textarea
            id="message"
            rows="4"
            v-model="message"
            class="block p-2.5 w-full text-sm text-gray-900 bg-gray-50 rounded-lg border border-gray-300 focus:ring-blue-500 focus:border-blue-500 dark:bg-gray-700 dark:border-gray-600 dark:placeholder-gray-400 dark:text-white dark:focus:ring-blue-500 dark:focus:border-blue-500"
            placeholder="Írjon nekünk..."
            required
          ></textarea>
        </div>

        <div class="container flex flex-row justify-center mx-auto items-center">
          <button
            type="submit"
            variant="success"
            class="px-5 py-2.5 text-sm font-medium text-white inline-flex items-center bg-sky-400 hover:bg-sky-600 focus:ring-4 focus:outline-none focus:ring-blue-300 rounded-lg text-center dark:bg-blue-600 dark:hover:bg-blue-700 dark:focus:ring-blue-800 mx-2"
          >
            <svg
              class="w-3.5 h-3.5 text-white mr-2"
              aria-hidden="true"
              xmlns="http://www.w3.org/2000/svg"
              fill="currentColor"
              viewBox="0 0 20 16"
            >
              <path
                d="m10.036 8.278 9.258-7.79A1.979 1.979 0 0 0 18 0H2A1.987 1.987 0 0 0 .641.541l9.395 7.737Z"
              ></path>
              <path
                d="M11.241 9.817c-.36.275-.801.425-1.255.427-.428 0-.845-.138-1.187-.395L0 2.6V14a2 2 0 0 0 2 2h16a2 2 0 0 0 2-2V2.5l-8.759 7.317Z"
              ></path>
            </svg>
            Küldés
          </button>

          <button
            type="reset"
            variant="success"
            class="px-5 py-2.5 text-sm font-medium text-white inline-flex items-center bg-red-400 hover:bg-red-600 focus:ring-4 focus:outline-none focus:ring-blue-300 rounded-lg text-center dark:bg-blue-600 dark:hover:bg-blue-700 dark:focus:ring-blue-800"
          >
            <svg
              class="w-3.5 h-3.5 text-white mr-2"
              aria-hidden="true"
              xmlns="http://www.w3.org/2000/svg"
              fill="currentColor"
              viewBox="0 0 20 16"
            >
              <path
                d="M17 4h-4V2a2 2 0 0 0-2-2H7a2 2 0 0 0-2 2v2H1a1 1 0 0 0 0 2h1v12a2 2 0 0 0 2 2h10a2 2 0 0 0 2-2V6h1a1 1 0 1 0 0-2ZM7 2h4v2H7V2Zm1 14a1 1 0 1 1-2 0V8a1 1 0 0 1 2 0v8Zm4 0a1 1 0 0 1-2 0V8a1 1 0 0 1 2 0v8Z"
              ></path>
            </svg>
            Törlés
          </button>
        </div>
      </form>
    </div>
  </div>
</template>

<script setup>
import { ref } from 'vue';

const name = ref('');
const email = ref('');
const phone = ref('');
const message = ref('');

async function onSubmit() {
  const response = await fetch("https://api.web3forms.com/submit", {
    method: "POST",
    headers: {
      "Content-Type": "application/json",
      Accept: "application/json",
    },
    body: JSON.stringify({
      access_key: "a9255bbd-ba5d-4b46-ae3e-786222cd8f05",
      name: name.value,
      email: email.value,
      phone: phone.value,
      message: message.value,
    }),
  });
  const result = await response.json();
  if (result.success) {
    window.alert("Üzenet sikeresen elküldve!");
    console.log(result);
  }
}

function onReset(event) {
  event.preventDefault();
  email.value = '';
  name.value = '';
  phone.value = '';
  message.value = '';
}
</script>
