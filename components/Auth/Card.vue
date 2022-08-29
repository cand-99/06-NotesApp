<script lang="ts" setup></script>

<template>
  <div>
    <NCard class="card">
      <h2>Login</h2>
      <div class="input-container">
        <input placeholder="Email">
        <input placeholder="Password">
      </div>
      <NButton>Login </NButton>
    </NCard>
  </div>
</template>

<style scoped>
.card {
  padding: 1rem;
  width: 20rem;
}

.card h2 {
  font-size: 1.5rem;
  margin-bottom: 0.5rem;
text-align: center;}
.input-container {
  display: flex;
  flex-direction: column;
}

.input-container input {
  margin-bottom: 0.3rem;
  padding: 0.3rem;
  outline: none;
}

</style>
