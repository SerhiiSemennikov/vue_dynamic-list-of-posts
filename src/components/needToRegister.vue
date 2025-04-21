<script>
export default {
  name: "NeedToRegister",
  data() {
    return {
      name: "",
    };
  },
};
</script>

<template>
  <div class="field">
    <label class="label" htmlFor="user-name"> Your Name </label>

    <div class="control has-icons-left">
      <input
        v-model="name"
        type="text"
        id="user-name"
        name="name"
        class="input"
        placeholder="Enter your name"
        required
        minlength="{4}"
      />
      <div class="body">
        <slot :x="name">{{ name }}</slot>
      </div>
      <span class="icon is-small is-left">
        <i class="fas fa-user" />
      </span>
    </div>

    <p v-if="!name" class="help is-danger">Start type Your Name please!</p>
  </div>
</template>

<style></style>
