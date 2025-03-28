# Resum Combinat: Tema 4 – Disseny del Software i Patrons

Aquest document combina els conceptes exposats en dos PDFs sobre el disseny del software. D'una banda, s’analitza l’enfocament global del disseny i l’arquitectura del sistema, i de l’altra, s’exploren els patrons de disseny que faciliten la resolució de problemes comuns en el desenvolupament orientat a objectes.

---

## 1. Introducció i Conceptes Generals

- **Objectiu:**  
  Dissenyar un sistema que s'adapti al model de negoci del client, que sigui flexible davant canvis en els requisits i que faciliti la comunicació entre els diferents components del software.

- **Relació amb l’anàlisi de requisits:**  
  Mentre que l’anàlisi de requisits defineix el “què” del sistema, el disseny es centra en el “com” es construeix per complir aquests requisits, traduint-los en estructures i mòduls que puguin evolucionar.

---

## 2. Arquitectura i Disseny del Software

### 2.1. Importància de l’Arquitectura

- **Comunicació i Organització:**  
  Una bona arquitectura permet comunicar el disseny d’alt nivell, assignar tasques als enginyers i gestionar la complexitat del sistema.
  
- **Adaptabilitat i Fiabilitat:**  
  L’arquitectura ha de permetre canvis en funció de l’entorn i garantir la robustesa i la integritat del sistema, tant estructuralment com conceptualment.

### 2.2. Procés de Disseny

- **Disseny Preliminar vs. Disseny Detallat:**  
  - **Preliminar:** Transformació del model de dades i definició de l’arquitectura general (disseny de dades, arquitectònic i interfície).  
  - **Detallat:** Refinament dels mòduls, definició de les funcions i la lògica pròpia del sistema.
  
- **Tipus de Disseny:**  
  - **Disseny de Dades:** Conversió del model de dades en estructures utilitzables.  
  - **Disseny Arquitectònic:** Estableix la relació entre els components principals.  
  - **Disseny Procedimental:** Defineix la lògica de programació i les operacions concretes.  
  - **Disseny d’Interfície:** Especifica com es comunica el sistema amb els usuaris i altres sistemes.

### 2.3. Modularitat, Cohesió i Acoblament

- **Modularitat:**  
  Divideix el sistema en mòduls amb responsabilitats ben definides, minimitzant la dependència entre ells.
  
- **Cohesió i Acoblament:**  
  L’objectiu és aconseguir una alta cohesió (components internament relacionats) i un baix acoblament (mínima dependència entre mòduls), facilitant així el manteniment i l’evolució del sistema.

### 2.4. Principis de Disseny Orientat a Objectes

- **Principis SOLID:**  
  - **SRP (Single Responsibility):** Una classe ha de tenir una única responsabilitat.  
  - **OCP (Open/Closed):** Les classes han d’estar obertes per a l’extensió però tancades per a modificacions.  
  - **LSP (Liskov Substitution):** Les subclasses han de poder substituir la seva classe base sense afectar el comportament del sistema.  
  - **ISP (Interface Segregation):** Es recomana dividir interfícies grans en interfícies més específiques.  
  - **DIP (Dependency Inversion):** Els mòduls d’alt nivell han de dependre d’abstraccions, no de mòduls de baix nivell.

- **Altres pràctiques:**  
  Disseny per contracte, dependency injection i el principi DRY (Don't Repeat Yourself) per mantenir el codi net i fàcil de modificar.

### 2.5. Disseny d’Interfícies d’Usuari

- **Objectius:**  
  Crear interfícies que millorin l’eficiència, minimitzin els errors i s’adaptin a les necessitats dels usuaris.
  
- **Principis Fonamentals (Regles daurades):**  
  - **Control a l’usuari:** Permetre desfer accions i oferir feedback constant.  
  - **Reducció de la càrrega cognitiva:** Utilitzar dreceres i mostrar informació de manera progressiva.  
  - **Consistència i Simplicitat:** Mantenir un disseny uniforme, reutilitzant patrons coneguts i assegurant l’accessibilitat i usabilitat.

> *(Veure resum Tema 4 – Disseny del Software per a més detalls)*  
> :contentReference[oaicite:0]{index=0}&#8203;:contentReference[oaicite:1]{index=1}

---

## 3. Patrons de Disseny

Els patrons de disseny són solucions generalitzades per problemes recurrents en el desenvolupament de software. Es classifiquen en tres grans categories:

### 3.1. Patrons de Creació

- **Objectiu:** Facilitar la creació d’objectes de manera flexible i desacoblar la instanciació de la implementació.
  
- **Exemples:**  
  - **Factory Method:** Crea objectes sense necessitar conèixer la classe exacta a instanciar.  
  - **Abstract Factory:** Proporciona una interfície per crear famílies d’objectes relacionats.  
  - **Builder:** Separa la construcció d’un objecte complex de la seva representació.  
  - **Prototype:** Clona objectes existents per crear noves instàncies.  
  - **Singleton:** Assegura que només hi hagi una única instància d’una classe en tot el sistema.

### 3.2. Patrons Estructurals

- **Objectiu:** Definir com s'organitzen i connecten els objectes per formar estructures més grans.
  
- **Exemples:**  
  - **Adapter:** Converteix la interfície d'una classe en una altra que el client espera.  
  - **Bridge:** Desacobla l’abstracció de la seva implementació, permetent modificar-los independentment.  
  - **Composite:** Permet tractar col·leccions d’objectes com si fossin un sol objecte.  
  - **Decorator:** Afegeix funcionalitats a un objecte dinàmicament sense modificar la seva estructura.  
  - **Facade:** Proporciona una interfície simplificada per a un conjunt de funcionalitats complexes.  
  - **Flyweight:** Optimitza l’ús de recursos compartint objectes comuns entre moltes instàncies.  
  - **Proxy:** Controla l’accés a un altre objecte, afegint funcionalitats com el control d'accés o la càrrega diferida.

### 3.3. Patrons de Comportament

- **Objectiu:** Gestionar la comunicació i la interacció entre objectes.
  
- **Exemples:**  
  - **Strategy:** Permet definir una família d’algorismes, encapsulant cada un i fent-los intercanviables.  
  - **Observer:** Defineix una dependència un a molts per actualitzar automàticament els objectes quan canvia un d’ells.  
  - **Iterator:** Proporciona una manera d’accedir als elements d’una col·lecció sense exposar la seva representació interna.  
  - **Template Method:** Defineix l’estructura d’un algorisme en una superclasse, permetent que les subclasses implementin certes parts.

> *(Veure resum Tema 4 – Disseny del Software. Patrons per a més detalls)*  
> :contentReference[oaicite:2]{index=2}&#8203;:contentReference[oaicite:3]{index=3}

---

## 4. Conclusió

La combinació d'una arquitectura ben dissenyada amb l'ús de patrons de disseny proporciona una base sòlida per construir software flexible, escalable i fàcil de mantenir. Mentre que el disseny general i la gestió dels components asseguren que el sistema s’adapti als requisits i canvis de l’entorn, els patrons de disseny permeten resoldre problemes comuns de manera estàndard i reusables, millorant la qualitat i la robustesa del codi.

---

Aquest resum integrat ofereix una visió global tant del procés de disseny del software com de les eines (patrons) disponibles per optimitzar aquest procés.
