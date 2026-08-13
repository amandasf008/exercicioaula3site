/* Header / Navbar — Amanda (padaria/confeitaria artesanal premium) */

:root {
  --amanda-brown-dark: #2b1d1a;
  --amanda-brown-mid: #3a2722;
  --amanda-gold: #d8c27a;
  --amanda-offwhite: #f8f5f0;
  --amanda-carmine: #d9082f;
  --amanda-carmine-hover: #c00729;
}

.header {
  position: sticky;
  top: 0;
  z-index: 50;
  background-color: var(--amanda-brown-dark);
  border-bottom: 1px solid var(--amanda-brown-mid);
}

.header__inner {
  margin: 0 auto;
  max-width: 1200px;
  height: 64px;
  display: flex;
  align-items: center;
  justify-content: space-between;
  padding: 0 20px;
}

@media (min-width: 768px) {
  .header__inner {
    height: 72px;
    padding: 0 32px;
  }
}

/* Logo */
.header__logo {
  font-family: "Cormorant Garamond", serif;
  font-size: 26px;
  font-weight: 600;
  letter-spacing: 0.03em;
  color: var(--amanda-gold);
  text-decoration: none;
  transition: color 0.2s ease;
}

.header__logo:hover {
  color: var(--amanda-offwhite);
}

@media (min-width: 768px) {
  .header__logo {
    font-size: 30px;
  }
}

/* Navegação desktop */
.header__nav {
  display: none;
  align-items: center;
  gap: 36px;
}

@media (min-width: 768px) {
  .header__nav {
    display: flex;
  }
}

.header__link {
  font-family: "Jost", sans-serif;
  font-size: 13px;
  font-weight: 500;
  letter-spacing: 0.12em;
  color: rgba(248, 245, 240, 0.9);
  text-decoration: none;
  transition: color 0.2s ease;
}

.header__link:hover {
  color: var(--amanda-gold);
}

/* Botão Orçamento */
.header__budget-btn {
  font-family: "Jost", sans-serif;
  font-size: 13px;
  font-weight: 500;
  letter-spacing: 0.08em;
  color: var(--amanda-offwhite);
  background-color: var(--amanda-carmine);
  border: none;
  border-radius: 9999px;
  padding: 10px 24px;
  margin-left: 8px;
  cursor: pointer;
  transition: background-color 0.2s ease;
}

.header__budget-btn:hover {
  background-color: var(--amanda-carmine-hover);
}

.header__budget-btn--mobile {
  margin-left: 0;
  margin-top: 8px;
  width: 100%;
  max-width: 220px;
  padding: 12px 24px;
  font-size: 14px;
}

/* Botão hamburger — mobile */
.header__burger {
  position: relative;
  z-index: 50;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  gap: 5px;
  width: 36px;
  height: 36px;
  background: transparent;
  border: none;
  cursor: pointer;
}

@media (min-width: 768px) {
  .header__burger {
    display: none;
  }
}

.header__burger-line {
  width: 24px;
  height: 1.5px;
  background-color: var(--amanda-gold);
  transition: transform 0.3s ease, opacity 0.2s ease;
}

.header__burger-line--top-open {
  transform: translateY(6.5px) rotate(45deg);
}

.header__burger-line--mid-open {
  opacity: 0;
}

.header__burger-line--bottom-open {
  transform: translateY(-6.5px) rotate(-45deg);
}

/* Menu mobile */
.header__mobile-menu {
  overflow: hidden;
  background-color: var(--amanda-brown-dark);
  max-height: 0;
  opacity: 0;
  transition: max-height 0.3s ease-in-out, opacity 0.3s ease-in-out;
}

.header__mobile-menu--open {
  max-height: 420px;
  opacity: 1;
}

@media (min-width: 768px) {
  .header__mobile-menu {
    display: none;
  }
}

.header__mobile-nav {
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 24px;
  padding: 32px 20px;
  border-top: 1px solid var(--amanda-brown-mid);
}

.header__mobile-nav .header__link {
  font-size: 15px;
}
