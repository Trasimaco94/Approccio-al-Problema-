# Approccio alla Programmazione: Gestione della Business Logic

## Definizione della Business Logic

La Business Logic rappresenta la parte centrale di un'applicazione, che gestisce il comportamento e le regole di business. È composta principalmente da due elementi:

1. **State**: Lo stato rappresenta i dati dell'applicazione in un dato momento. Può includere informazioni come utenti loggati, dati di input, risultati di calcoli, ecc.

2. **Actions**: Le azioni sono gli eventi che modificano lo stato dell'applicazione. Possono essere scatenati dall'utente (come clic su un pulsante) o da altri eventi interni (come ricevere dati da un server).

## Passi per l'Approccio al Problema

1. **Comprendere il Problema**: Analizzare e comprendere appieno il problema che l'applicazione deve risolvere. Identificare i requisiti e le regole di business.

2. **Definire lo Stato Iniziale**: Identificare quali dati sono necessari per rappresentare lo stato iniziale dell'applicazione.

3. **Identificare le Azioni**: Determinare le azioni che possono essere eseguite all'interno dell'applicazione e che influenzano lo stato.

4. **Implementare la Business Logic**: Scrivere il codice che gestisce lo stato e le azioni. Questo può includere funzioni per aggiornare lo stato in risposta alle azioni.

5. **Testare la Business Logic**: Verificare che la logica funzioni correttamente, testando vari scenari e casi d'uso.

## Applicazione della Business Logic

### Utilizzo delle Classi in JavaScript

In JavaScript, è possibile utilizzare classi per organizzare e gestire la business logic dell'applicazione.

```javascript
class App {
  constructor() {
    this.state = {
      // Definizione dello stato iniziale
    };
  }

  // Definizione di metodi per gestire le azioni
  handleAction1() {
    // Logica per gestire Action 1 e aggiornare lo stato
  }

  handleAction2() {
    // Logica per gestire Action 2 e aggiornare lo stato
  }

  // Altri metodi per gestire altre azioni...
}

const myApp = new App();

## Utilizzo del Context in React

In React, il Context può essere utilizzato per condividere lo stato tra i componenti senza dover passare manualmente le props attraverso ogni livello dell'albero dei componenti.

import React, { createContext, useContext, useReducer } from 'react';

// Definizione del contesto
const AppContext = createContext();

// Definizione del provider
const AppProvider = ({ children }) => {
  const [state, dispatch] = useReducer(reducer, initialState);

  return (
    <AppContext.Provider value={{ state, dispatch }}>
      {children}
    </AppContext.Provider>
  );
};

// Utilizzo del contesto
const MyComponent = () => {
  const { state, dispatch } = useContext(AppContext);

  // Utilizzo dello stato e delle azioni
};

 export { AppProvider, MyComponent };‹


In questo modo, la business logic può essere gestita centralmente e condivisa tra i vari componenti dell'applicazione React.

Con questo approccio, è possibile mantenere un codice più organizzato, modulare e facilmente testabile, consentendo una migliore gestione e scalabilità dell'applicazione nel tempo.

# RIASSUNTO DI GESTIONE DI DATI IN ARRAY

- Eliminare = Filter

- Aggiungere = Spread Operator

- Modificare = Map
