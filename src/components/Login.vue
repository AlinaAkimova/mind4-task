<template lang="pug">
form(class="login")
  section(class="login__section")
    h2(class="login__head") Please login
    section(class="login__inputSection")
      label(class="login__label") E-mail
      input(class="login__input" type="text" id="email" name="email" placeholder="Enter E-mail")
      label(class="login__label") Password
      input(class="login__input" type="text" id="password" name="password" placeholder="Enter Password")
    button(class="login__button login__button-login" type="submit") Login
    section(class="login__divide")
      div(class="login__line")
      div(class="login__or") OR
      div(class="login__line")
    button(class="login__button login__button-signUp" type="submit") Sign up
    p(class="login__text") Forget password? Restore
</template>

<script>
export default {
  name: "Login",
};
</script>

<style scoped lang="scss">
@import "../assets/scss/main.scss";

.login {
  width: 630px;
  background-color: rgba(255, 255, 255, 0.1);
  border-radius: 30px;

  display: flex;
  justify-content: center;

  @media (max-width: 750px) {
    width: 500px;
  }

  @media (max-width: 550px) {
    width: 350px;
  }

  &__section {
    display: flex;
    flex-direction: column;
    width: 80%;
  }

  &__head {
    @include font-title;
    color: $white;
  }

  &__label {
    @include font-main-text;
    color: $white;
    margin-bottom: 10px;
  }

  &__inputSection {
    display: flex;
    flex-direction: column;
  }

  &__inputSection:not(:last-child) {
    margin-bottom: 30px;
  }

  &__input {
    @include font-input;
    margin-bottom: 15px;
    padding: 16px;
    border: none;
    border-radius: 12px;

    color: $lightBlack;
    background-color: $white;

    &:focus {
      border: none;
      outline: none;
    }

    @media (max-width: 900px) {
      max-width: 100%;
    }
  }

  &__button {
    @include font-button;
    width: 100%;
    padding: 16px;
    border: none;
    border-radius: 12px;

    text-transform: uppercase;
    cursor: pointer;

    @media (max-width: 900px) {
      max-width: 100%;
    }

    &-login {
      border: 1px solid $white;
      background-color: $white;
      color: $blue;
    }

    &-signUp {
      border: 1px solid rgba(255, 255, 255, 0.2);
      background-color: inherit;
      color: $blue;
    }
  }

  &__button-login:hover {
    border: 1px solid rgba(255, 255, 255, 0.2);
    background-color: inherit;
  }

  &__button-signUp:hover {
    background-color: $white;
  }

  &__divide {
    display: flex;
    align-items: center;
    margin: 15px 0;
  }

  &__or {
    @include font-button;
    padding: 0 33px;
    color: $white;
  }

  &__line {
    max-width: 211px;
    width: 100%;
    height: 1px;
    opacity: 0.1;
    background: $white;
  }

  &__text {
    @include font-main-text;
    color: $white;
    margin-bottom: 70px;
  }
}
</style>
