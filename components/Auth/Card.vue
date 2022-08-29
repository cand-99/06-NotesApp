<script lang="ts" setup>
const authState = ref<"Login" |"Signup">("Login");

const toggleAuthState = () => {
 if(authState.value === "Login") authState.value = "Signup";
  else authState.value = "Login";
}
</script>

<template>
  <div>
    <NCard class="card">
      <h2>{{authState}}</h2>
      <div class="input-container">
        <input placeholder="Email">
        <input placeholder="Password">
      </div>
      <NButton>Submit </NButton>
      <p @click="toggleAuthState">{{authState === "Login" ? "Don't have account? Create one now" : "Already have an accoutn? Please login" }}</p>
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

p {
  color: white;
  font-size: small;
  cursor: pointer;
  margin-top: 0.5rem;
}

</style>
