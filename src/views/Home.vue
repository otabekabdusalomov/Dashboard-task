<script setup>
import ChevronDownIcon from "../icons/chevron-down.svg";
import QuestionMarkIcon from "../icons/question-mark.svg";
import MasterCardIcon from "../icons/master-card.svg";
import CubeIcon from "../icons/cube.svg";
import TransactionsVue from "../components/Transactions.vue";
import StatisticsList from "../components/StatisticsList.vue";
import Transaction from "../components/Transaction.vue";
</script>

<template>
  <div class="px-8">
    <ul class="grid grid-cols-3 gap-x-5 trasform -translate-y-[100px]">
      <li class="rounded-[16px] bg-sky-400 px-5 py-6">
        <div class="mb-[80px] flex justify-between">
          <p class="text-xs font-semibold capitalize">Software product</p>
          <p
            class="text-xs font-semibold capitalize text-darkgray underline decoration-2 underline-offset-4"
          >
            Saving account
          </p>
        </div>
        <div class="flex justify-between">
          <p class="text-[28px] font-semibold uppercase">Service</p>
          <button
            class="inline-flex items-center gap-x-1 rounded-10 text-xs font-semibold uppercase text-gray-700 hover:text-white"
          >
            <span class="pl-2">Big product</span>
            <ChevronDownIcon class="h-6 w-6 stroke-current" />
          </button>
        </div>
      </li>

      <li class="rounded-[16px] bg-sky-400 px-5 py-6">
        <div class="mb-[60px] flex items-center justify-between">
          <p class="text-xs font-semibold capitalize">Your saving status</p>
          <button class="cursor-pointer">
            <QuestionMarkIcon class="h-6 w-6 stroke-darkgray fill-darkgray" />
          </button>
        </div>
        <div class="flex">
          <CubeIcon class="h-14 w-14 stroke-red-500 fill-red-500 p-3 bg-red-200 rounded-full" />
          <div class="ml-3">
            <span class="text-red-500 text-[24px] font-semibold">4.28%</span>
            <p class="text-xs font-semibold">Your spending increased</p>
          </div>
        </div>
      </li>

      <li class="rounded-[16px] bg-sky-400 px-5 pt-2 pb-6">
        <div class="flex flex-col">
          <MasterCardIcon class="h-12 w-12" />
          <span class="text-[10px] mb-2 uppercase">Card number</span>
          <span class="font-medium text-[17px] tracking-wider">Any number</span>
        </div>
        <div class="flex mt-6">
          <div class="flex flex-col mr-[60px]">
            <span class="uppercase text-[10px]">Card holder name</span>
            <span class="capitalize font-semibold text-sm">Responsible person</span>
          </div>
          <div class="flex flex-col">
            <span class="uppercase text-[10px]"></span>
            <strong class="text-sm">01/04</strong>
          </div>
        </div>
      </li>
    </ul>
    <StatisticsList />
    <div class="flex">
      <TransactionsVue/>
      <Transaction/>
    </div>
  </div>
</template>
