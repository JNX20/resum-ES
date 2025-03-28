# Resum: Tema 5 – Qualitat del Software (Primera part)

Aquest document aborda la importància de la qualitat en el desenvolupament de software, centrant-se en les estratègies de prova, els models de desenvolupament i el disseny de proves, amb especial atenció a les tècniques de proves de caixa blanca.

---

## 1. Introducció

- **Definició de Test:**  
  Un test és l'avaluació (manual o automàtica) d'un sistema per verificar que compleix els requisits especificats i per detectar discrepàncies entre els resultats esperats i els obtinguts.

- **Importància de provar el software:**  
  - Sempre hi ha errors en qualsevol implementació.  
  - Els tests serveixen com a xarxa de seguretat per assegurar que el sistema funciona correctament i per poder afrontar canvis sense trencar funcionalitats existents.  
  - Es presenten exemples reals (com els problemes amb el coet Ariane 5 o errors en sistemes bancaris) per destacar el cost elevat que poden comportar els errors.

- **Cost de correcció:**  
  El cost de corregir un error és molt inferior quan es detecta de forma precoç, abans que el disseny estigui completament definit.

---

## 2. Estratègies de Prova

- **Manual vs. Automàtic:**  
  - Les proves manuals són laborioses, consumeixen molt temps i poden provocar errors degut a la seva natura repetitiva.  
  - Els tests automàtics són ràpids i permeten comprovar la funcionalitat en segons, facilitant la detecció d'errors amb cada canvi.

- **La Piràmide de Tests:**  
  Un enfocament que defineix diferents nivells de proves (unitàries, d'integració, d'acceptació, etc.) per assegurar una cobertura eficaç del software.

- **Tipus de proves:**  
  - **Proves de Caixa Blanca:** Avaluen la lògica interna i l'execució de totes les línies de codi.  
  - **Proves de Caixa Negra:** Se centren en el comportament extern del sistema, sense tenir en compte la seva estructura interna.

---

## 3. Models de Desenvolupament de Software

- **Model en Cascada:**  
  - Els plans de prova es defineixen durant l'anàlisi, però les proves es realitzen després de finalitzar el desenvolupament.  
  - Avantatge: rigor inicial; Inconvenient: els errors es detecten massa tard.

- **Model en V:**  
  - Cada fase de desenvolupament té la seva fase de test corresponent, des de proves unitaris fins a la integració del sistema complet.
  - Permet detectar defectes des de les fases inicials, però el client encara veu el producte només al final.

- **Model Agile:**  
  - Integració contínua de desenvolupament i tests (TDD – Test Driven Development).  
  - Avantatges: feedback constant, detecció precoç dels errors i adaptabilitat als canvis en els requisits.  
  - Inconvenients: en projectes molt complexos pot ser difícil predir l'esforç requerit en cada iteració.

---

## 4. Disseny de Proves

- **Activitats Principals:**  
  - **Definició de casos de prova:** Determinar quines propietats del sistema es verificaran i com es provaran.  
  - **Execució de proves:** Executar el sistema segons els casos de prova i comparar els resultats obtinguts amb els esperats.
  - **Selecció de casos de prova:** Degut a la impossibilitat de provar totes les condicions possibles, s'ha de seleccionar un conjunt de casos que cobreixi els escenaris més rellevants.

---

## 5. Proves de Caixa Blanca

- **Objectius:**  
  - Verificar que s'executin totes les línies de codi.  
  - Assegurar l'ús correcte de totes les estructures de dades i l'execució completa dels bucles.

- **Tipus de proves de Caixa Blanca:**  
  - **Tests Unitaris:** Comproven el correcte funcionament d'una unitat (funció, classe) de forma aïllada.  
  - **Tests d'Integració:** Verifiquen la interacció correcta entre diferents mòduls del sistema.

- **Mètode de Camins Bàsics:**  
  - **Pas 1:** Representar el flux de control mitjançant un graf.  
  - **Pas 2:** Comptar el nombre de camins independents utilitzant la complexitat ciclomàtica (V(G)).  
  - **Pas 3:** Seleccionar un conjunt de camins bàsics, on cada camí representa una execució independent.  
  - **Pas 4:** Dissenyar casos de prova que forcin l'execució de cada camí seleccionat.  
  - **Pas 5:** Executar el codi i comparar els resultats obtinguts amb els esperats.

- **Detalls addicionals:**  
  Es poden utilitzar representacions com la matriu d'adjacència per analitzar les connexions i el flux d'execució, cosa que pot ajudar a mecanitzar la detecció de camins i la mesura de la complexitat del codi.

---

## Conclusió

Aquest document posa en relleu com la qualitat del software depèn en gran mesura d'un enfocament estructurat en les proves. Tant les estratègies de prova (automàtiques i manuals) com els models de desenvolupament (en cascada, en V i agile) són essencials per garantir que el sistema compleixi els requisits especificats i funcioni de manera fiable. Les proves de caixa blanca, especialment a través de la tècnica dels camins bàsics i la mesura de la complexitat ciclomàtica, ofereixen eines clau per detectar errors internament i assegurar una alta cobertura del codi.

:contentReference[oaicite:0]{index=0}&#8203;:contentReference[oaicite:1]{index=1}
