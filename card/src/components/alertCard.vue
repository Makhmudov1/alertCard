<template>
<!--  alert card-->
    <article class="border rounded-lg mt-1 relative
    pt-4 pb-4  pl-9 pr-3
    sm:pl-6 sm:pr-4
    md:pr-7"
    :class="[{
      'block before:absolute before:w-2.5 before:h-2.5 md:before:w-3 md:before:h-3 before:rounded-full before:bg-accent before:top-1/4 sm:before:top-1/2 before:-translate-y-1.5 before:right-full before:translate-x-7 sm:before:-translate-x-3':!item.isReady,
      }]">
        <!--Теги (контейнер)-->
        <div class="flex">
          <!--Тег 'дата'-->
          <p class = "bg-accent-8 rounded text-10 font-semibold py-1 px-2.5
          sm:py-1 sm:px-2.5 sm:text-12">{{item.date}}</p>
          <!--Тег 'время'-->
          <p class="bg-accent-8 rounded text-10 font-semibold py-1 px-2.5 ml-1
          sm:px-2.5 sm:py-1 sm:text-12">
            <!--Иконка 'время'-->
            <svg class="hidden sm:inline-block" width="13.5" height="13.5" viewBox="0 0 16 16" fill="none" xmlns="http://www.w3.org/2000/svg">
              <path d="M8 5V8L10.25 10.25M14.75 8C14.75 8.88642 14.5754 9.76417
              14.2362 10.5831C13.897 11.4021 13.3998 12.1462 12.773 12.773C12.1462 13.3998 11.4021
              13.897 10.5831 14.2362C9.76417 14.5754 8.88642 14.75 8 14.75C7.11358 14.75 6.23583
              14.5754 5.41689 14.2362C4.59794 13.897 3.85382 13.3998 3.22703 12.773C2.60023 12.1462
              2.10303 11.4021 1.76381 10.5831C1.42459 9.76417 1.25 8.88642 1.25 8C1.25 6.20979 1.96116
              4.4929 3.22703 3.22703C4.4929 1.96116 6.20979 1.25 8 1.25C9.79021 1.25 11.5071 1.96116 12.773
              3.22703C14.0388 4.4929 14.75 6.20979 14.75 8Z" stroke="#121212" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"/>
            </svg>
            {{item.time}}
          </p>
        </div>
      <!--Текст уведомления (контейнер)-->
      <div class="mt-4 md:flex md:flex-row md:justify-between
      md:py-1 md:text-16">
        <!--Текст уведомления-->
        <p class="text-14 font-normal">{{item.text}}</p>
        <!--Ссылка 'перейти к заказу'-->
          <a class="mt-2.5
          flex justify-end text-12
          sm:py-2 sm:pl-1 sm:text-12
          md:pl-1 md:py-1 md:text-14
          xl:text-14 font-semibold" href="#">Перейти к заказу
            <!--Иконка 'стрелка'-->
            <svg class="inline-block ml-2" width="16" height="10" viewBox="0 0 17 10" fill="none" xmlns="http://www.w3.org/2000/svg">
              <path fill-rule="evenodd" clip-rule="evenodd"
                    d="M10.793 0.293031C10.9805 0.10556 11.2348 0.000244141 11.5 0.000244141C11.7652 0.000244141 12.0195 0.10556 12.207 0.293031L16.207
                  4.29303C16.3945 4.48056 16.4998 4.73487 16.4998 5.00003C16.4998 5.26519 16.3945 5.5195 16.207 5.70703L12.207
                  9.70703C12.0184 9.88919 11.7658 9.98998 11.5036 9.9877C11.2414 9.98543 10.9906 9.88026 10.8052 9.69485C10.6198
                  9.50944 10.5146 9.25863 10.5123 8.99643C10.51 8.73423 10.6108 8.48163 10.793 8.29303L13.086 6.00003H1.5C1.23478
                  6.00003 0.98043 5.89467 0.792893 5.70714C0.605357 5.5196 0.5 5.26525 0.5 5.00003C0.5 4.73481 0.605357 4.48046
                  0.792893 4.29292C0.98043 4.10539 1.23478 4.00003 1.5 4.00003H13.086L10.793 1.70703C10.6055 1.5195 10.5002 1.26519
                  10.5002 1.00003C10.5002 0.734866 10.6055 0.480558 10.793 0.293031Z" fill="#5B5B5B"/>
            </svg>
          </a>
      </div>
    </article>
</template>

<script setup>
import { ref } from 'vue'
defineProps({
    item: {
        type: Object,
        default: null
    }
})
</script>

<style scoped>

</style>
