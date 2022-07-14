<template>
  <div>
    <pre>
      {{ JSON.stringify(account, null, 2) }}
    </pre>
  </div>
  <form action="" method="post">
    <div>
      <label for="name">Name</label>
      <input type="text" name="Name" id="name" v-model="account.name" />
    </div>
    <div>
      <label for="email">Email</label>
      <input type="email" name="Email" id="email" v-model="account.email" />
    </div>
    <div>
      <label for="country">Country</label>
      <select v-model="account.country">
        <option value="---">---</option>
        <option>Canada</option>
        <option>United States of America</option>
      </select>
    </div>
    <div>
      <label for="password">Password</label>
      <input
        type="password"
        name="Password"
        id="password"
        v-model="account.password"
      />
    </div>
    <div>
      <label for="passwordRetry">Re-enter password</label>
      <input
        type="password"
        name="Re-enter password"
        id="passwordRetry"
        v-model="account.passwordRetry"
      />
    </div>
  </form>
</template>

<script>
export default {
  name: "CreateAccount",
  data() {
    return {
      account: {
        name: "",
        email: "",
        country: "",
        password: "",
        passwordRetry: "",
      },
    };
  },
};
</script>

<style scoped></style>
