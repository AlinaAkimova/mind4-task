<template lang="pug">
form(class="login")
  section(class="login__section")
    h1(class="login__head") Please login
    section(class="login__inputSection")
      label(class="login__label") E-mail
      input(class="login__input" type="email" id="email" name="email" placeholder="Enter E-mail")
      label(class="login__label") Password
      input(class="login__input" type="password" id="password" name="password" placeholder="Enter Password")
    button(class="login__button login__button-login" type="submit") Login
    div(class="login__or") OR
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
  height: 646px;
  border-radius: 30px;

  background-color: rgba(255, 255, 255, 0.1);
  backdrop-filter: blur(27.5px);

  display: flex;
  justify-content: center;

  @media (max-width: 750px) {
    width: 500px;
  }

  @media (max-width: 550px) {
    width: 350px;
  }

  @media (max-width: 500px) {
    width: 350px;
    height: 550px;
  }

  &__section {
    display: flex;
    flex-direction: column;
    width: 80%;
  }

  &__head {
    @include font-title;
    color: $white;
    margin: 45px 0 30px 0;
  }

  &__label {
    @include font-main-text;
    color: $white;
    margin-bottom: 10px;
  }

  &__inputSection {
    display: flex;
    flex-direction: column;
    margin-bottom: 15px;
  }

  &__input {
    @include font-input;
    margin-bottom: 15px;
    padding: 16px;
    border: none;
    border-radius: 12px;
    line-height: 32px;

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
    padding: 8px 10px;
    border: none;
    border-radius: 12px;
    line-height: 44px;

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
      color: $white;
    }
  }

  &__button-login:hover {
    border: 1px solid rgba(255, 255, 255, 0.2);
    background-color: inherit;
    color: $white;
  }

  &__button-signUp:hover {
    background-color: $white;
    color: $blue;
  }

  &__or {
    @include font-button;
    padding: 15px 0;
    color: $white;
    display: flex;
    align-items: center;
    justify-content: space-between;
  }

  &__or::before,
  &__or::after {
    content: "";
    max-width: 211px;
    width: 100%;
    height: 1px;
    opacity: 0.1;
    background: $white;
  }
  &__text {
    @include font-main-text;
    color: $white;
  }
}
</style>
