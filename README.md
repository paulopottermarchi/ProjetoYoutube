# Clone do YouTube - Projeto Educacional

## Visão Geral
Este é um projeto Java que simula um sistema básico similar ao YouTube, onde usuários (Gafanhotos) podem assistir vídeos e interagir com eles. O projeto demonstra conceitos de Programação Orientada a Objetos (POO) incluindo herança, interfaces e encapsulamento.

## Estrutura do Projeto

### Classes
- **Video**: Implementa a funcionalidade do vídeo com recursos como play, pause e like
- **Pessoa**: Classe abstrata base para tipos de usuários
- **Gafanhoto**: Estende Pessoa, representa um espectador/usuário
- **Visualizacao**: Gerencia a relação entre espectadores e vídeos
- **AcoesVideo**: Interface que define as ações básicas do vídeo

### Funcionalidades Principais
- Gerenciamento de vídeos (play, pause, like)
- Gerenciamento de usuários
- Controle de visualizações
- Sistema de avaliação
- Sistema de pontos de experiência

## Detalhes das Classes

### Video
- Atributos:
  - titulo
  - avaliacao
  - views
  - curtidas
  - reproduzindo
- Métodos para controle de vídeo (play, pause, like)

### Pessoa (Abstrata)
- Atributos base:
  - nome
  - idade
  - sexo
  - experiencia
- Método abstrato para ganhar experiência

### Gafanhoto
- Estende Pessoa com atributos adicionais:
  - login
  - totAssistido
- Controla histórico de visualizações do usuário

### Visualizacao
- Gerencia a relação de visualização entre usuários e vídeos
- Possui diferentes métodos de avaliação:
  - Avaliação padrão (escala de 5)
  - Avaliação numérica
  - Avaliação por porcentagem

## Exemplo de Uso
```java
// Criar vídeos
Video v[] = new Video[3];
v[0] = new Video("Aula 1 de POO");

// Criar usuários
Gafanhoto g[] = new Gafanhoto[2];
g[0] = new Gafanhoto("Jubileu", 22, "M", "juba");

// Criar e registrar visualizações
Visualizacao vis[] = new Visualizacao[5];
vis[0] = new Visualizacao(g[0], v[0]);
vis[0].avaliar(); // Avaliar o vídeo
```

## Sistema de Avaliação
O sistema suporta três métodos de avaliação:
1. Avaliação padrão (5 estrelas)
2. Avaliação numérica (1-10)
3. Avaliação por porcentagem:
   - ≤20% = 3 estrelas
   - ≤50% = 5 estrelas
   - ≤90% = 8 estrelas
   - >90% = 10 estrelas

## Requisitos
- Kit de Desenvolvimento Java (JDK)
- IDE Java (Eclipse, NetBeans, IntelliJ IDEA)

## Status do Projeto
Este é um projeto demonstrativo para fins educacionais, apresentando conceitos de POO em Java.

## Autor
- Paulo

## Observações
- O projeto foi desenvolvido em português para facilitar o aprendizado
- Projetado como uma ferramenta educacional para compreensão de conceitos de POO
- Ideal para estudantes iniciando em programação orientada a objetos
