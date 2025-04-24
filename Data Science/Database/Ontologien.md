---
uni-module: "KonzMod"

alias: ["Ontology", "Ontologies"]
---

# Ontology

## Classical Definition

An ontology is a representation of the

- types
- properties
- interrelationships
  of the entities that fundamentally exist for a particular domain of discourse (e.g. [[Environment]] when talking about a [[Rational Agent]]).

We want to take actions when something in the [[Environment]] is [[Entailment|entailed]] by the [[Percept|percepts]].

## Logic Definition

An ontology consists of a [[Logical System]] $\mathcal{S}:=\langle\mathcal{L}, \mathcal{K}, \models\rangle$ and [[Concept Axiom|concept axioms]] expressed in the formal language $\mathcal{L}$ about:

- individuals (concrete instance of object in the domain)
- [[Concept|concepts]] (classes of individuals)
- relations between [[Concept|concepts]] and individuals

Examples of ontologies:

- [[Semantic Network]]
- [[Propositional Logic as Set Description Language]]
- [[First-Order Predicate Logic]]

## Others

**In Phylosophy**
Die Ontologie ist die Lehre des Seins, des Existierenden. Sie beschreibt eine Einteilung aller Dinge in Kategorien. Ein Teilgebiet ist deswegen auch die Mereologie, also die Lehre vom Teil und Ganzem.

- [[Epistemologie]]
- [[Semiotik]]

**In Computer Science**

Durch die Kommunikation auf Basis einer Umgangssprache können Mehrdeutigkeiten entstehen. Beispiel dafür sind Homonyme und Synonyme

Als Terminologische Kontrolle bezeichnet man alle Maßnahmen, die dazu beitragen Begriffe zu definieren und voneinander abzugrenzen.

In der Informatik wird Ontologie anders als in der Philosophie als eine Spezifikation von gemeinsam zu verwendenden Begriffen (und deren Zusammenhängen) definiert. -> gemeinsames Verständnis.

- Top-level-Ontologie
  - Top-level-Ontologien sind allgemeingültige Kategorien, die eine Art Kategorie der Top-Domänen-Ontologie darstellen.
- Top-Domänen-Ontologie
  - Top-Domänen-Ontologie sind Kategorien, die für einen größeren Anwendungsbereich spezifiziert sind.
- Domänen-Ontologie
  - Domänen-Ontologien sind Kategorien, die einen spezifischen Anwendungsbereich beschreiben können.

**Grad der Formalisierung**

1. informal
   - Ein [[Vocabulary|Vokabular]].
2. Begriffshierarchie
   - Nomenklaturen.
3. semiformal
   - Ein semantisches Netz oder auch [[Unified Modelling Language]] , [[ER-Modell]].
4. formal
   - Formalisierte logische Theorie

## Ziele

Ziel ist es eine Domänenontologie für Systementwickler bereitzustellen, kompatible Systeme zu bauen und dabei effizient vorzugehen.

Eine spezielle Methode zur Spezifikation von [[Ontologien]] ist es allen Dingen einen Namen zu geben und diese dann zueinander in Beziehung zu setzen. Dabei entsteht ein riesiger [[Graph]], der die Grundidee von _"Linked Data"_ darstellt. Zusätzlich kann jedem Namen noch eine weltweit eindeutige URI zugewiesen werden um einen globalen Graphen zu erstellen, der Aussagen über alle Dinge treffen kann.
Wenn dem Namen zuletzt noch eine Bedeutung zugeteilt wird entsteht aus dem globalen Graphen ein Wissensgraph. Aus diesem vorhanden Wissen kann dann neues Wissen abgeleitet werden.
Genau auf diesem Prinzip basiert auch das Zettelkasten System, mit dem diese Notiz geschrieben wurde.

RDF und OWL fehlen noch...

[[Formal Ontology]]
