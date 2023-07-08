<template>
  <VBtn @click="dialog = !dialog"> Trigger Dialog </VBtn>
  <VDialog v-model="dialog">
    <VCard class="mx-auto" width="500">
      <VToolbar color="primary">
        <VToolbarTitle>Settings</VToolbarTitle>
        <VSpacer />
        <VToolbarItems>
          <VBtn class="mx-3" icon="$close" size="small" @click="dialog = false" />
        </VToolbarItems>
      </VToolbar>
      <VCardText>
        <VRow>
          <VCol cols="6">
            <VTextField v-model="dialogFormFields.name" label="Name" />
          </VCol>
          <VCol cols="6">
            <VTextField v-model="dialogFormFields.lastName" label="Last name" />
          </VCol>
          <VCol cols="6">
            <VTextField v-model="dialogFormFields.gender" label="Gender" />
          </VCol>
          <VCol cols="6">
            <VTextField v-model="dialogFormFields.house" label="House" />
          </VCol>
        </VRow>
      </VCardText>
    </VCard>
  </VDialog>
</template>

<script setup>
const { dialogFormFields, dialog } = toRefs(useAppStore())
</script>
