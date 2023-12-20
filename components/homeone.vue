<template>
  <div class="flex flex-col mx-5">
    <div>
      <h1>I say hello</h1>
      <p>
        Lorem ipsum dolor sit amet, consectetur adipisicing elit. Magni
        accusantium totam autem harum quas dicta, numquam ad. Doloremque!
      </p>
      <p>
        Lorem ipsum dolor sit amet consectetur adipisicing elit. Sapiente,
        nesciunt?
      </p>
    </div>
    <div class="w-46 md:w-80 my-2">
      <UFormGroup
        size="md"
        label="Email"
        hint="Optional"
        description="We'll only use this for spam."
        help="We will never share your email with anyone else."
      >
        <UInput placeholder="you@example.com" icon="i-heroicons-envelope" />
      </UFormGroup>
    </div>
    <div class="my-2">
      <modal />
    </div>
    <div class="flex gap-2 my-2">
      <UBadge color="primary" variant="solid">Badge</UBadge>
      <UBadge color="rose" variant="solid">Badge</UBadge>
      <UBadge color="indigo" variant="solid">Badge</UBadge>
      <UBadge color="violet" variant="solid">Badge</UBadge>
    </div>
  </div>
</template>

<script setup></script>
