# Resum Combinat: Tema 5 – Qualitat del Software (Parts I i II)

Aquest document aborda la qualitat del software des d'una perspectiva integral. Es presenten les estratègies de prova, els models de desenvolupament, el disseny de proves i les tècniques tant de caixa blanca com de caixa negra, així com la implementació detallada i la derivació de casos de prova.

---

## 1. Introducció

- **Definició de Test:**  
  Un test és l’avaluació (manual o automàtica) d’un sistema per verificar que compleix els requisits especificats i per identificar discrepàncies entre els resultats esperats i els obtinguts.

- **Importància de les proves:**  
  - Tots els sistemes presenten errors; per tant, les proves actuen com a xarxa de seguretat.
  - Detectar errors precoçment redueix el cost de correcció, tal com s’ha vist en casos reals (ex. coet Ariane 5, errors bancaris).

---

## 2. Estratègies de Prova

- **Manual vs. Automàtic:**  
  - **Manual:** Laboriós, consumeix molt temps i és més propens a errors per la seva naturalesa repetitiva.
  - **Automàtic:** Permet executar proves ràpidament, integrant-se en el procés de desenvolupament (TDD) i facilitant la detecció de regressions.

- **Tipus de Proves:**  
  - **Caixa Blanca:** S'examina la lògica interna, els camins d'execució, les estructures de dades i els bucles.
  - **Caixa Negra:** Es comprova el comportament extern del sistema, enfocant-se en la verificació dels requisits sense conèixer la implementació interna.

- **Piràmide de Tests:**  
  Es recomana una estructura de proves que inclogui un alt nombre de tests unitaris (baixa escala) i menys tests d’integració i d’acceptació (escala global).

---

## 3. Models de Desenvolupament de Software

- **Model en Cascada:**  
  Els plans de test es defineixen en fases inicials, però els errors es detecten al final del desenvolupament, cosa que pot portar a costos elevats de correcció.

- **Model en V:**  
  Cada fase del desenvolupament té una fase de test corresponent, des de tests unitaris fins a la integració completa. Permet detectar defectes en fases inicials, però el client rep el producte només al final.

- **Model Agile:**  
  Integra desenvolupament i tests de manera contínua (TDD). Ofereix feedback constant, adaptabilitat als canvis i una estabilitat progressiva del sistema, encara que en projectes molt complexos pot resultar difícil predir l’esforç necessari.

---

## 4. Disseny i Implementació de Proves

### 4.1 Proves de Caixa Blanca

- **Objectius:**  
  - Verificar que totes les línies de codi s'executen almenys una vegada.
  - Comprovar que es cobreixen totes les condicions, bucles i estructures de dades.

- **Tècniques:**
  - **Tests Unitaris:** Proven la funcionalitat d’una unitat de codi (funció o classe).
  - **Prova de Camins Bàsics:**  
    1. Representar el flux de control mitjançant un graf.
    2. Comptar el nombre de camins independents amb la complexitat ciclomàtica (V(G)).
    3. Seleccionar un conjunt de camins bàsics que cobreixin totes les sentències.
    4. Dissenyar casos de prova per a cada camí i executar-los.
    
- **Implementació específica (Part II):**
  - **Prova dels bucles:** Es defineixen diferents classes de bucles (simples, niats, concatenats, no estructurats) i es proposen casos de prova per verificar condicions com "passar per alt", "executar una vegada", "executar n-1, n i n+1 vegades", etc.
  - **Prova basada en el flux de dades:** Es seleccionen variables d’interès i es defineixen les cadenes definició-ús (DU), assegurant que cada cadena es cobreix almenys una vegada.

### 4.2 Proves de Caixa Negra

- **Objectius:**  
  Verificar el comportament del sistema sense conèixer la seva estructura interna.
  
- **Tècniques:**
  - **Prova de Partició Equivalent:**  
    Dividir l’espai d’entrades en classes d’equivalència (entrades vàlides vs. no vàlides) i seleccionar un representant per cada classe.
  - **Anàlisi de Valors Límits:**  
    Es prioritzen els casos de prova amb valors en les fronteres de cada classe, ja que són més propensos a generar errors.
  - **Prova de Comparació:**  
    Especialment per entorns crítics, on diverses implementacions s’executen paral·lelament per comparar resultats en temps real.
  
---

## 5. Nivells de Proves i Casos de Prova

- **Nivells de Prova:**
  - **Proves de Components (Unitats):** Verifiquen el correcte funcionament de mòduls individuals.
  - **Proves d’Integració:** Comproven la col·laboració entre diferents mòduls, detectant errors en les interfícies i dependències.
  - **Proves de Sistema:** Validació del sistema com un tot, assegurant que compleix els requisits globals.
  - **Proves d’Acceptació:** Verifiquen que el sistema compleix amb el contracte establert amb el client, incloent proves en entorns reals (alfa, beta i de camp).

- **Definició de casos de prova:**
  - **Basada en el codi:** (Caixa Blanca) Derivació directa a partir de l’estructura interna.
  - **Basada en requisits:** (Caixa Negra) Els casos es deriven dels requisits funcionals i no funcionals, i poden ser especificats mitjançant models (diagrames d’estats, d’activitats, etc.).
  - **Derivació basada en models:** Cada camí d’un model de prova representa un escenari a cobrir; es defineixen criteris de cobertura (estats, transicions, esdeveniments, branques, camins).

- **Implementació en entorns orientats a objectes (POO):**
  - **Test Drivers:** Es pot implementar com a funcions dins del mateix arxiu o com a classes separades (CTester) per executar proves de classes, integració i interacció entre objectes.
  - **Proves d’integració en POO:** Es detecten errors en la col·laboració entre objectes, especialment en situacions amb herència, encapsulament i polimorfisme.

---

## Conclusió

La qualitat del software depèn d’un enfocament sistemàtic en les proves a tots els nivells del desenvolupament. Un bon pla de proves combina tècniques de caixa blanca i caixa negra per aconseguir una cobertura àmplia, mentre que la derivació i implementació de casos de prova, basada tant en el codi com en els requisits, permeten detectar errors de manera precoç. Els models de desenvolupament (en cascada, en V i agile) determinen com i quan s’executen aquestes proves, amb una forta orientació a l’automatització per garantir la fiabilitat del sistema.

---

*(Veure Tema5-1 per la primera part de la qualitat del software: :contentReference[oaicite:0]{index=0}&#8203;:contentReference[oaicite:1]{index=1})*  
*(Veure Tema5-2 per la implementació i derivació avançada de casos de prova: :contentReference[oaicite:2]{index=2}&#8203;:contentReference[oaicite:3]{index=3})*
