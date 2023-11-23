<script setup>
</script>

<template>
  <header class="header">
    <div class="header-container">
      <div class="header-logo">
        <img src="../assets/img/header-logo.svg" alt="logo" width="96" height="28" />
      </div>

      <form class="header-search">
        <input type="search" placeholder="Search">
        <button type="submit">
          <svg width="24" height="24">
            <use href="#search-icon" />
          </svg>
        </button>
      </form>

      <ul class="header-nav">
        <li class="nav-item">
          <a href="#" class="nav-link active">Home</a>
        </li>
        <li class="nav-item">
          <a href="#" class="nav-link">About</a>
        </li>
        <li class="nav-item">
          <a href="#" class="nav-link">Contact Us</a>
        </li>
        <li class="nav-item">
          <a href="#" class="nav-link">Blog</a>
        </li>
      </ul>

      <ul class="header-user-panel">
        <li class="user-panel-item">
          <a href="#" class="user-panel-link">
            <svg width="32" height="32">
              <use href="#favorites" />
            </svg>
          </a>
        </li>
        <li class="user-panel-item">
          <a href="#" class="user-panel-link">
            <svg width="32" height="32">
              <use href="#cart" />
            </svg>
          </a>
        </li>
        <li class="user-panel=item">
          <a href="#" class="user-panel-link">
            <svg width="32" height="32">
              <use href="#user" />
            </svg>
          </a>
        </li>
      </ul>
    </div>
  </header>
</template>

<style scoped lang="scss">
@import '../assets/styles/mixins.scss';

.header-container {
  @include container;

  padding-top: 16px;
  padding-bottom: 16px;
  display: flex;
  gap: 32px;
  align-items: center;
}

.header-search {
  flex: 1;
  position: relative;

  input {
    @include txt-14;
    padding: 19px 16px 19px 48px;
    background-color: var(--light-grey);
    border-radius: 8px;
    width: 100%;

    &::placeholder {
      @include txt-14;
      color: var(--dark-grey);
    }

    &::-webkit-search-cancel-button {
      display: none;
    }
  }

  button {
    position: absolute;
    top: 50%;
    left: 16px;
    transform: translateY(-50%);
    cursor: pointer;
  }
}

.header-nav {
  display: flex;
  gap: 52px;
}

.nav-link {
  @include header-link;

  color: var(--typo-dark);
  opacity: .3;

  transition: opacity .2s ease-in-out;

  &.active {
    opacity: 1;
  }

  &:hover {
    opacity: 1;
  }
}

.header-user-panel {
  display: flex;
  gap: 24px;
}
</style>