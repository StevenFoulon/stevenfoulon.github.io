// Fichier LanguageSwitcher.js
import React from 'react';
import { NavLink, useLocation } from 'react-router-dom';
import './LanguageSwitcher.css'; // Le même CSS que ci-dessus

const LanguageSwitcher = () => {
  const location = useLocation();
  const isFrench = location.pathname === '/' || location.pathname.startsWith('/fr');

  return (
    <nav className="language-switcher">
      <NavLink
        to="/"
        className={({ isActive }) =>
          `lang-button ${isFrench ? 'active-lang' : ''}`
        }
        aria-label="Passer en français"
      >
        <span role="img" aria-label="Drapeau français">🇫🇷</span> Français
      </NavLink>
      <span className="separator">|</span>
      <NavLink
        to="/en"
        className={({ isActive }) =>
          `lang-button ${!isFrench ? 'active-lang' : ''}`
        }
        aria-label="Switch to English"
      >
        <span role="img" aria-label="UK flag">🇬🇧</span> English
      </NavLink>
    </nav>
  );
};

export default LanguageSwitcher;

// Dans votre fichier App.js ou équivalent (où vous définissez vos routes)
// ...
import { BrowserRouter as Router, Routes, Route } from 'react-router-dom';
import LanguageSwitcher from './LanguageSwitcher';
// ... Vos composants de CV pour chaque langue

function App() {
  return (
    <Router>
      <header>
        {/* Autres éléments de l'en-tête */}
        <LanguageSwitcher />
      </header>
      <main>
        <Routes>
          <Route path="/" element={/* Votre composant CV en FR */} />
          <Route path="/en" element={/* Votre composant CV en EN */} />
          {/* Si vous avez d'autres routes spécifiques à la langue */}
          <Route path="/fr/:id" element={/* ... */} />
          <Route path="/en/:id" element={/* ... */} />
        </Routes>
      </main>
    </Router>
  );
}
// ...

<img src="/assets/photos.png" alt="Steven Foulon" width="150" style="border-radius: 50%; margin-top: 1rem;">

# 👋 Salut, moi c'est Steven Foulon

Ex-manager chez Carrefour, aujourd’hui Data Engineer chez SNCF. Je me suis reconverti dans la data avec passion et détermination.

---

## 🚀 Projets

- 🎯 **Bot DCA Bitcoin** – Une app personnelle pour investir de manière intelligente en se basant sur des indicateurs économiques.
- 💼 **Tableau de bord Cloud (AWS)** – Pour suivre les coûts d’une plateforme data complexe.

---

## 🛠️ Stack technique

- **Data Engineering**: Databricks, Airflow
- **Data Visualisation**: Power BI, Streamlit
- **APIs**: FastAPI, Flask
- **Bases de données**: PostgreSQL
- **Cloud**: AWS
- **DevOps**: Docker, Git, GitLab CI/CD

---

## 🧠 Ce que je fais au quotidien

- 🔧 Data Engineering – 50% – Construction de pipelines ETL, automatisation ETL, industrialisation
- 📊 Data Analyse – 30% – Exploration, visualisation, recommandations
- 🎤 Vulgarisation et présentation – 20% – Présentations claires pour des publics non techniques

---

## 📄 Mon CV

👉 [Télécharger mon CV (PDF)](/CV_FR.pdf)

---

## 📬 Me contacter

- ✉️ Email : [flstevenpro@outlook.fr](mailto:flstevenpro@outlook.fr)
- 💼 LinkedIn : [linkedin.com/in/steven-foulon](https://www.linkedin.com/in/steven-foulon-69332514378921788486211/)
