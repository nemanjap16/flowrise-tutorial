<script setup lang="ts">
const settings = useSettings();
</script>

<template>
  <Bounded as="header">
    <div class="flex gap-4 items-center justify-between flex-col sm:flex-row">
      <Logo />
      <nav>
        <ul class="flex gap-[30px]">
          <li
            v-for="item in settings?.data.navigation"
            :key="item.label ?? ''"
          >
            <PrismicLink
              :field="item.link"
              class="text-[#0891B2] font-normal"
            >
              {{ item.label }}
            </PrismicLink>
          </li>
        </ul>
      </nav>
    </div>
  </Bounded>
</template>
