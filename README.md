/* ==========================================================================
   1. CSS VARIABLES & BASE STYLES
   ========================================================================== */
:root {
  --primary-color: #2b3a4a;
  --accent-color: #007acc;
  --accent-hover: #0056b3;
  --bg-color: #f8f9fa;
  --card-bg: #ffffff;
  --text-color: #333333;
  --spacing-unit: 1rem;
}

body {
  margin: 0;
  padding: 0;
  font-family: system-ui, -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, sans-serif;
  background-color: var(--bg-color);
  color: var(--text-color);
}

/* ==========================================================================
   2. EXTRA 1: RESPONSIVE NAVIGATION MENU
   ========================================================================== */
.main-header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 1rem 2rem;
  background-color: var(--primary-color);
  color: #ffffff;
}

.nav-links {
  display: flex;
  gap: 1.5rem;
  list-style: none;
  margin: 0;
  padding: 0;
}

.nav-links a {
  color: #ffffff;
  text-decoration: none;
}

.nav-toggle {
  display: none; /* Hidden on larger screens */
  background: none;
  border: none;
  color: #ffffff;
  font-size: 1.5rem;
  cursor: pointer;
}

/* Mobile viewpoint breakpoint */
@media (max-width: 768px) {
  .nav-links {
    display: none; /* Hide default inline links */
  }
  
  .nav-toggle {
    display: block; /* Show hamburger button on mobile */
  }
}

/* ==========================================================================
   3. EXTRA 2: DYNAMIC CSS GRID LAYOUT
   ========================================================================== */
.feature-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
  gap: 1.5rem;
  padding: 2rem;
}

.card {
  background: var(--card-bg);
  padding: 1.5rem;
  border-radius: 8px;
  box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
}

/* ==========================================================================
   4. EXTRA 3: INTERACTIVE MICRO-INTERACTIONS (HOVER TRANSITIONS)
   ========================================================================== */
.btn-primary,
.cta-button {
  display: inline-block;
  padding: 0.75rem 1.5rem;
  background-color: var(--accent-color);
  color: #ffffff;
  border: none;
  border-radius: 4px;
  text-decoration: none;
  font-weight: bold;
  cursor: pointer;
  transition: transform 0.2s ease, background-color 0.2s ease;
}

.btn-primary:hover,
.cta-button:hover {
  transform: translateY(-2px);
  background-color: var(--accent-hover);
}

/* ==========================================================================
   5. EXTRA 4: UNIQUE LANDING PAGE ARCHITECTURE
   ========================================================================== */
.landing-hero {
  display: flex;
  flex-direction: column;
  align-items: center;
  padding: 4rem 2rem;
  background-color: #f4f6f8;
  text-align: center;
}

.landing-hero h1 {
  font-size: 2.5rem;
  margin-bottom: 1rem;
  color: var(--primary-color);
}

.landing-hero p {
  max-width: 600px;
  margin-bottom: 2rem;
  font-size: 1.125rem;
}
