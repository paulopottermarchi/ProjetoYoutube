# YouTube Clone - Educational Project

## Overview

This is a **Java project** that simulates a basic system similar to YouTube, where users (called *Gafanhotos*) can watch and interact with videos. The project demonstrates core **Object-Oriented Programming (OOP)** concepts including inheritance, interfaces, and encapsulation.

---

## Project Structure

### Classes

- **Video**: Implements video functionality including play, pause, and like.
- **Pessoa (Person)**: Abstract base class for user types.
- **Gafanhoto (Grasshopper)**: Extends `Pessoa`, represents a viewer/user.
- **Visualizacao (View)**: Manages the relationship between users and videos.
- **AcoesVideo (VideoActions)**: Interface that defines basic video actions.

---

## Main Features

- Video management (play, pause, like)
- User management
- View tracking system
- Video rating system
- Experience points system

---

## Class Details

### `Video`

**Attributes:**
- `titulo` (title)
- `avaliacao` (rating)
- `views` (view count)
- `curtidas` (likes)
- `reproduzindo` (isPlaying)

**Methods:**
- Control methods: `play()`, `pause()`, `like()`

---

### `Pessoa` (Abstract)

**Base Attributes:**
- `nome` (name)
- `idade` (age)
- `sexo` (gender)
- `experiencia` (experience)

**Abstract Method:**
- `ganharExperiencia()` (gainExperience)

---

### `Gafanhoto`

**Extends `Pessoa` with:**
- `login`
- `totAssistido` (total watched)

**Features:**
- Manages user's watch history

---

### `Visualizacao`

- Manages viewing interactions between users and videos
- Supports different evaluation methods:
  - Default rating (5-star scale)
  - Numeric rating
  - Percentage-based rating

---

## Example Usage

```java
// Create videos
Video v[] = new Video[3];
v[0] = new Video("OOP Class 1");

// Create users
Gafanhoto g[] = new Gafanhoto[2];
g[0] = new Gafanhoto("Jubileu", 22, "M", "juba");

// Create and record views
Visualizacao vis[] = new Visualizacao[5];
vis[0] = new Visualizacao(g[0], v[0]);
vis[0].avaliar(); // Rate the video


Rating System
The project supports three evaluation methods:

Default Rating: 5-star scale

Numeric Rating: 1 to 10

Percentage-Based Rating:

≤ 20% → 3 stars

≤ 50% → 5 stars

≤ 90% → 8 stars

90% → 10 stars

Requirements
Java Development Kit (JDK)

Java IDE (Eclipse, NetBeans, IntelliJ IDEA, etc.)

Project Status
This is a demonstration project for educational purposes, showcasing OOP concepts in Java.

Author
Paulo

## PS:
-  The project was developed in portuguese 
