<template>
  <header class="header">
    <div class="header__content">
      <div class="header__text">
        <h1 class="title">BLOSSOM & BREW FESTIVAL</h1>
        <p class="subtitle">
         A womans dream childhood now materialised  
        </p>

        <div class="header__actions">
          <button class="btn btn--primary">
            UPDATE ME 
          </button>
        </div>
      </div>

      <div class="header__visual" >
        <div class="visual__badge">Gold / Silver / Bronze</div>
      </div>
    </div>
  </header>
</template>

<style scoped>

.header {
  padding: 2.5rem 1.25rem;
  background: linear-gradient(180deg, #fff7f0 0%, #fffaf6 100%);
  border-bottom: 1px solid rgba(0,0,0,0.04);
}

.header__content {
  max-width: 1100px;
  margin: 0 auto;
  display: flex;
  gap: 2rem;
  align-items: center;
  justify-content: space-between;
  flex-wrap: wrap;
}

.header__text {
  flex: 1 1 420px;
  min-width: 260px;
}

.title {
  font-size: 2.1rem;
  margin: 0 0 0.4rem 0;
  line-height: 1.05;
}

.subtitle {
  margin: 0 0 1.2rem 0;
  color: #ffa5e0;
  font-size: 1rem;
}

/* Actions */
.header__actions {
  display: flex;
  gap: 0.75rem;
  flex-wrap: wrap;
}

.btn {
  padding: 0.6rem 1rem;
  border-radius: 8px;
  border: 1px solid transparent;
  cursor: pointer;
  font-weight: 600;
  font-size: 0.95rem;
}

.btn--primary {
  background: #ff97bf;
  color: white;
  border-color: rgba(0,0,0,0.06);
}

.btn--ghost {
  background: transparent;
  color: #ff97bf;
  border-color: rgba(255,107,53,0.12);
}

/* Visual / hero area */
.header__visual {
  flex: 0 0 220px;
  min-width: 160px;
  display: flex;
  align-items: center;
  justify-content: center;
}

.visual__badge {
  padding: 0.8rem 1rem;
  border-radius: 12px;
  background: linear-gradient(90deg,#fdc2ff,#fff1e8);
  box-shadow: 0 6px 18px rgba(255,107,53,0.08);
  font-weight: 700;
  color: #ff8dd9;
}

/* Responsive */
@media (max-width: 720px) {
  .title {
    font-size: 1.6rem;
  }
  .header__content {
    gap: 1rem;
  }
  .header__visual {
    margin-top: 0.8rem;
  }
}
</style>

