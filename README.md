# 🧵 Generative Adversarial Network (GAN) para Geração de Imagens Fashion MNIST

Este projeto implementa uma Rede Generativa Adversarial (GAN) utilizando TensorFlow e Keras, com o objetivo de gerar imagens realistas inspiradas no conjunto de dados **Fashion MNIST**. O projeto é uma aplicação direta do conceito original de GANs proposto por Ian Goodfellow, simulando uma competição entre duas redes neurais: o gerador (Generator) e o discriminador (Discriminator).

---

## 🎯 Objetivo

Treinar uma GAN para que o gerador aprenda a criar imagens falsas de peças de roupas (como camisetas, bolsas, sapatos, etc.), imitando as imagens reais do dataset Fashion MNIST, e explorar visualmente a evolução do modelo ao longo das épocas.

---

## ⚙️ Tecnologias Utilizadas

- Python 3.10+
- TensorFlow 2.x
- NumPy
- Matplotlib

---

## 🗃️ Dataset

Utilizamos o **Fashion MNIST**, que contém:

- 70.000 imagens em escala de cinza
- Dimensões: 28x28 pixels
- 10 classes diferentes de roupas (como camisetas, casacos, botas, etc.)

Esse dataset é uma alternativa mais desafiadora ao MNIST tradicional (dígitos), com imagens de roupas estilizadas.

---

## 📐 Estrutura e Fluxo do Projeto

1. **Pré-processamento dos dados**
   - As imagens são normalizadas para a faixa `[-1, 1]` para compatibilidade com a função de ativação `tanh` do gerador.

2. **Criação dos modelos**
   - **Gerador (Generator):** Recebe ruído (vetor aleatório) e tenta gerar imagens de roupas que imitem as reais.
   - **Discriminador (Discriminator):** Recebe uma imagem (real ou gerada) e decide se ela é "real" ou "falsa".

3. **Treinamento manual**
   - Foi utilizada uma abordagem manual (sem `model.fit`) para alternar entre o treinamento do discriminador e do gerador.
   - A cada batch:
     - O discriminador é treinado com imagens reais e falsas.
     - O gerador é treinado para tentar enganar o discriminador.
   - A cada 2 épocas, o modelo exibe 81 imagens geradas para análise visual da evolução.

4. **Registro de desempenho**
   - Em cada época, são impressas as métricas:
     - Perda do Gerador e do Discriminador
     - Acurácia de ambos
     - Tempo gasto por época (em segundos)

5. **Visualização Final**
   - Ao fim do treinamento, é gerado um mosaico de 81 imagens produzidas pelo gerador treinado.
   - Observa-se o fenômeno de *mode collapse*, em que o gerador tende a focar em apenas um ou poucos padrões de roupa.

---

## 🧠 Conceitos Abordados

- **Redes Neurais Profundas**
- **Adversarial Learning**
- **Treinamento manual de GANs**
- **Normalização de dados**
- **Visualização de progresso**

---

## 🎮 Aplicações Reais

- Geração de roupas para avatares em jogos
- Simulações de moda para e-commerce
- Produção de datasets sintéticos para treinamento de modelos de classificação
- Criação de texturas e elementos gráficos dinâmicos para jogos ou filmes
- Pesquisa sobre aprendizado não supervisionado e geração de dados

---

## 🧵 Exemplo de Saída

As imagens geradas são visualizadas em uma grade 9x9, com o objetivo de mostrar o quão realistas estão ficando ao longo do tempo. Isso ajuda a entender a qualidade da distribuição aprendida pelo gerador.

---
## ✅ Conclusão

Este projeto demonstrou de forma prática como funciona uma GAN, desde a definição dos modelos até a visualização dos resultados gerados. Utilizar o Fashion MNIST acrescenta um grau de complexidade adicional em relação ao MNIST original, além de trazer um contexto mais aplicável à indústria da moda, jogos e design gráfico.

---

- 📌 **Autor**: Hian Stafford
- 📩 **Email**: hian.correa@gmail.com
```text
  /\_/\  
 ( -.- ) 
  > ^ < 
```
