# 🏋️ Swe Gym - Sistema Gestionale per Palestre

> Progetto universitario di Ingegneria del Software – Università degli Studi di Firenze

## 📌 Descrizione del progetto

**Swe Gym** è un sistema gestionale modulare per palestre, progettato per adattarsi a contesti sportivi eterogenei. Il software consente la gestione completa degli utenti, degli abbonamenti, delle attività, delle prenotazioni e del personale, con un’interfaccia dinamica basata sul ruolo dell’utente.

Il progetto è stato realizzato come parte di un laboratorio universitario di **Ingegneria del Software**, focalizzandosi **sulla fase di progettazione**, modellazione UML e interazione con il database, simulando il ciclo di vita completo di uno sviluppo professionale.

---

## 🧠 Obiettivi

- Progettare un **software gestionale scalabile e modulare**
- Gestire **autenticazione e autorizzazione** multi-utente
- Modellare e realizzare l’interazione tra sistema e database
- Supportare **diverse tipologie di utenti** (Clienti, Istruttori, Staff Amministrativo)
- Documentare l’intero processo attraverso **diagrammi UML**, template ingegneristici e casi d’uso

---

## 🏗️ Architettura e Design

### 🧩 Modularità per tipologia utente

ZUE Gym è progettato per adattare il comportamento dell’interfaccia e delle funzionalità in base al **ruolo dell’utente**:
- **Cliente**: prenotazione corsi, gestione abbonamenti, visualizzazione personal trainer
- **Istruttore**: monitoraggio utenti, caricamento piani di allenamento, gestione delle classi
- **Amministratore**: gestione abbonamenti , controllo personal trainer

Ogni interazione con il database è **filtrata e controllata** in base al tipo di utente.

---

## 🛠️ Tecnologie

- **Linguaggio:** Java (JDK 17)
- **Database:** MySQL 
- **Strumenti:** UML Designer, StarUML, Visual Paradigm, Lucidchart

---

## 📐 Progettazione e Modelli UML

Il progetto ha seguito un **approccio ingegneristico iterativo** con attenzione alle fasi di analisi e progettazione:

### 📎 Documentazione inclusa
- **Requisiti funzionali e non funzionali**
- **Template dei casi d’uso** (Use Case Template)
- **Diagrammi UML principali**:
  - Diagramma dei casi d’uso
  - Diagramma delle classi
  - Diagramma delle attività
  - Diagramma delle sequenze
  - Diagramma ER (Entity-Relationship)
  - Diagramma dei pacchetti

---

## 🧪 Esempio d’uso

```java
// Login e instradamento in base al tipo di utente
Utente utente = sistema.login("email@example.com", "password123");

if (utente instanceof Cliente) {
    interfacciaCliente.mostraDashboard((Cliente) utente);
} else if (utente instanceof Istruttore) {
    interfacciaIstruttore.mostraDashboard((Istruttore) utente);
} else if (utente instanceof Amministratore) {
    interfacciaAdmin.mostraPannelloGestione();
}
