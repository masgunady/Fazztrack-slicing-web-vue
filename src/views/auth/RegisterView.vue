<script setup lang="ts">
  import imgLogo from '../../assets/images/fazztrack.svg'
  import { RouterLink } from 'vue-router';
</script>

<template>
  <div class="w-full flex justify-center items-center p-5 my-11">
      <div class="lg:w-[700px] border rounded-sm shadow-sm p-5 py-11 lg:px-11 flex flex-col gap-3">
        <div class="w-full flex justify-center items-center">
          <img :src="imgLogo" alt="logo" class="w-32 pb-3" />
        </div>
        <div class="w-full text-black text-2xl font-semibold text-center tracking-wide">
          Daftar & Mulai Belajar
        </div>
        <div class="text-black text-base text-center tracking-tight">
          Sudah punya akun Fazztrack? 
          <RouterLink to="/auth/login" class="text-primary font-bold">
            Masuk Disini
          </RouterLink>
        </div>

        <form class="w-full flex flex-col gap-6 text-black">
          <div class="w-full flex flex-col gap-2">
            <label htmlFor="input-name" class="text-black">
              <span class="text-red-600">*</span> Nama Lengkap
            </label>
            <input
              type="text"
              id="input-name"
              class="input input-bordered input-accent border-slate-300"
              placeholder="Masukan nama lengkap..."
            />
          </div>
          <div class="w-full flex flex-col gap-2">
            <label htmlFor="input-email" class="text-black">
              <span class="text-red-600">*</span> Email
            </label>
            <input
              type="text"
              id="input-email"
              class="input input-bordered input-accent border-slate-300"
              placeholder="Masukan nama e-mail..."
            />
          </div>
          <div class="w-full flex flex-col gap-2">
            <label htmlFor="input-phone" class="text-black">
              <span class="text-red-600">*</span> No. Handphone
            </label>
            <input
              type="text"
              id="input-phone"
              class="input input-bordered input-accent border-slate-300"
              placeholder="Masukan no. handphone..."
            />
          </div>
          <div class="w-full flex flex-col gap-2">
            <label htmlFor="input-password" class="text-black">
              <span class="text-red-600">*</span> Kata Sandi
            </label>
            <input
              id="input-password"
              type="password"
              class="input input-bordered input-accent border-slate-300"
              placeholder="Masukan kata sandi..."
            />
          </div>
          <div class="w-full flex flex-col gap-2">
            <label htmlFor="input-confirm-password" class="text-black">
              <span class="text-red-600">*</span> Konfirmasi Kata Sandi
            </label>
            <input
              id="input-confirm-password"
              type="password"
              class="input input-bordered input-accent border-slate-300"
              placeholder="Masukan ulang kata sandi..."
            />
          </div>

          <div class="w-full flex items-center justify-between">
            <div class="flex justify-start items-center gap-2">
              <input id="ingat-saya" type="checkbox" class="w-4 h-4" />
              <label htmlFor="ingat-saya" class="text-black">
                Saya menyetujui{" "}
                <RouterLink to='/' class="text-secondary font-bold">
                  Syarat dan Ketentuan
                </RouterLink>
              </label>
            </div>
          </div>

          <div class="w-full">
            <button class="btn btn-primary text-white text-lg font-semibold capitalize w-full">
              Masuk
            </button>
          </div>
        </form>
      </div>
    </div>
</template>