<script>
import ticket from '../tickets';

export default {
  name: "ticketdispense",

  data() {
    return {
      ticket
    };
  },}
</script>
<template>
    <div class="cards-row"> <!-- instead of me using containers i used rows so the cards can be next to eachother-->

    <div 
      class="ticketDispensr"
      v-for="(tickets, index) in ticket"
      :key="tickets.id"
    >
      <div class="stack">
        <div class="card">
          <img class="image" :src="tickets.image" alt="..." />
          <h2>{{ tickets.name }}</h2>
          <p>{{ tickets.description }}</p>
          <small>{{ tickets.benefit }}</small>
        </div>
      </div>
    </div>
  </div>
</template>




<style>
.cards-row {
  display: flex;
  justify-content: center;
  gap: 2rem;
  padding: 2rem;
}

.ticketDispensr {
  display: flex;
  justify-content: center;
}


img {
  display: block;
  max-width: 60%;
  position: absolute;
}

.stack {
  width: 90%;
  max-width: 400px;
  transition: 0.25s ease;
  &:hover {
    transform: rotate(5deg);
    .card:before {
      transform: translatey(-2%) rotate(-4deg);
    }
    .card:after {
      transform: translatey(2%) rotate(4deg);
    }
  }
}

.card {
  aspect-ratio: 3 / 2;
  border: 4px solid;
  background-color: #fff;
  position: relative;
  transition: 0.15s ease;
  cursor: pointer;
  padding: 5% 5% 15% 5%;
  &:before,
  &:after {
    content: "";
    display: block;
    position: absolute;
    height: 100%;
    width: 100%;
    border: 4px solid;
    background-color: #fff;
    transform-origin: center center;
    z-index: -1;
    transition: 0.15s ease;
    top: 0;
    left: 0;
  }

  &:before {
    transform: translatey(-2%) rotate(-6deg);
  }

  &:after {
    transform: translatey(2%) rotate(6deg);
  }
}
.image {
  width: 100%;
  border: 4px solid;
  background-color: #eee;
  aspect-ratio: 1 / 1;
  position: relative;
}

.browser-warning {
  margin-bottom: 4rem;
}

@supports (aspect-ratio: 1 / 1) {
  .browser-warning {
    display: none;
  }
}
</style>