# 📘 README — Trabalho 3: Raciocínio Neuro-Simbólico com LTN

## 📌 Descrição Geral

Este repositório contém o código e a documentação do **Trabalho 3 da disciplina Fundamentos de Inteligência Artificial (FIA)**.  
O objetivo é implementar e analisar um sistema de **Raciocínio Neuro-Simbólico (NeSy)** baseado em **Logic Tensor Networks (LTN)**, integrando percepção neural, conhecimento lógico e inferência simbólica.

Além dos cenários gerados aleatoriamente, conforme solicitado no enunciado, foi incluído **um cenário manual**, construído explicitamente com objetos definidos à mão, permitindo uma análise mais controlada e interpretável do comportamento do sistema.

---

## 1. NeSy e Logic Tensor Networks (LTN)

### 🔹 Neuro-Symbolic Learning (NeSy)
NeSy combina:
- **Modelos neurais**, responsáveis por lidar com dados contínuos e perceptuais;
- **Lógica simbólica**, responsável por impor regras, restrições e estrutura semântica.

Essa integração permite sistemas mais **interpretáveis**, **estruturados** e capazes de realizar **raciocínio lógico explicável**.

### 🔹 Logic Tensor Networks (LTN)
As LTNs representam:
- Predicados como funções neurais diferenciáveis;
- Fórmulas lógicas como restrições;
- O grau de verdade das fórmulas por meio de **satisfatibilidade fuzzy**.

O treinamento ocorre maximizando a satisfatibilidade global das fórmulas lógicas.

---

## 2️. Dataset CLEVR e Descrição Simplificada

O trabalho utiliza dados inspirados no **dataset CLEVR**, compostos por cenários sintéticos com múltiplos objetos.

Cada objeto é descrito por:
- **Cor**: vermelho, verde ou azul;
- **Forma**: círculo, quadrado, cilindro, cone ou triângulo;
- **Tamanho**: pequeno ou grande;
- **Posição espacial**: coordenadas contínuas no plano.

### 🔹 Cenários Aleatórios
- Gerados automaticamente;
- Utilizados para avaliar a generalização do sistema em diferentes instâncias do problema.

### 🔹 Cenário Manual (Realizado Previamente)
- Criado explicitamente com objetos definidos à mão;
- Permite validar se o raciocínio lógico está de acordo com a semântica esperada;
- Facilita a interpretação das respostas e a análise qualitativa do sistema.

---

## 3️. Predicados, Axiomas e Fórmulas Lógicas

### 🔹 Predicados
- **Perceptuais**: `isRed`, `isGreen`, `isBlue`, `isCircle`, `isSquare`, `isCylinder`, `isCone`, `isTriangle`, `isSmall`, `isBig`
- **Espaciais (treináveis)**: `leftOf`, `rightOf`, `above`, `below`
- **Derivado**: `canStack(x, y)`

---

## 4️. Valor de Satisfatibilidade das Fórmulas

São reportados:
- **Satisfatibilidade global (SatAgg)** do conjunto de axiomas;
- **Satisfatibilidade individual** de cada fórmula lógica;
- **Satisfatibilidade das perguntas (queries)** de raciocínio.

Esses valores são analisados tanto para os cenários aleatórios quanto para o cenário manual.

---

## 5️. Protocolo Experimental — 5 Execuções

### 5.1. Treinamento:
- O modelo é **treinado uma única vez**, partindo de um cenário introduzido manualmente (realizado previamente em sala de aula);
- O objetivo é capturar as regularidades lógicas do domínio.

### 5.2. Avaliação:
- O passo de **geração de dados** é repetido **5 vezes**, produzindo **5 datasets aleatórios distintos**;
- Para cada dataset:
  - O cenário é plotado;
  - As consultas de raciocínio são executadas;
  - As métricas são calculadas;
- Não há re-treinamento entre execuções, garantindo independência entre os cenários.

---

## 6️. Resultados Reportados

Para **cada uma das 5 execuções**, são apresentados:

### 🔹 Métricas Lógicas
- **Satisfatibilidade (SatAgg)**:
  - de cada axioma;
  - de cada fórmula;
  - de cada pergunta de raciocínio.

### 🔹 Métricas Clássicas
Calculadas para os predicados perceptuais:
- **Acurácia**
- **Precisão**
- **Recall**
- **F1-score**

---

## 7️. Explicação dos Resultados (Célula Final)

Ao final do notebook, é incluída uma **célula dedicada à explicação dos resultados**, na qual:

- Cada pergunta de raciocínio é analisada individualmente;
- Justifica-se, em linguagem natural, o valor de satisfatibilidade obtido;

Essa etapa atende ao requisito de **explicabilidade** solicitado no enunciado.

---

## 📁 Estrutura do Repositório

- `notebook.ipynb` — implementação completa do sistema LTN;
- `README.md` — descrição do projeto, protocolo experimental e resultados;

---

## 8. Conclusão

Os resultados demonstram que **Logic Tensor Networks** permitem integrar aprendizado neural e raciocínio lógico de forma consistente.  
A inclusão de um **cenário manual** fortalece a análise qualitativa, evidenciando maior assertividade e maior interpretabilidade das respostas obtidas.

---

## 9. Integrantes

<div align="center">

<table>
  <tr>
    <td align="center" style="padding: 10px;">
      <a href="https://github.com/giovani-artil" target="_blank">
        <img src="https://github.com/giovani-artil.png" width="150px" style="border-radius: 50%;" alt="Giovani Carvalho"/><br />
        <span style="font-weight: bold; font-size: 16px; color: #333;">Giovani Carvalho</span>
      </a><br />
      <span style="font-size: 14px; color: #777;">Developer</span>
    </td>
    <td align="center" style="padding: 10px;">
      <a href="https://github.com/samuelcoelhoam" target="_blank">
        <img src="https://github.com/samuelcoelhoam.png" width="150px" style="border-radius: 50%;" alt="Jorge Coelho"/><br />
        <span style="font-weight: bold; font-size: 16px; color: #333;">Jorge Coelho</span>
      </a><br />
      <span style="font-size: 14px; color: #777;">Developer</span>
    </td>
    <td align="center" style="padding: 10px;">
      <a href="https://github.com/rehOtsedom12" target="_blank">
        <img src="https://github.com/rehOtsedom12.png" width="150px" style="border-radius: 50%;" alt="Renata Fernandes"/><br />
        <span style="font-weight: bold; font-size: 16px; color: #333;">Renata Fernandes</span>
      </a><br />
      <span style="font-size: 14px; color: #777;">Developer</span>
    </td>
    <td align="center" style="padding: 10px;">
      <a href="https://github.com/sofiaIcavino" target="_blank">
        <img src="https://github.com/sofiaIcavino.png" width="150px" style="border-radius: 50%;" alt="Sofia Moura"/><br />
        <span style="font-weight: bold; font-size: 16px; color: #333;">Sofia Moura</span>
      </a><br />
      <span style="font-size: 14px; color: #777;">Developer</span>
    </td>
    <td align="center" style="padding: 10px;">
      <a href="https://github.com/Tory18" target="_blank">
        <img src="https://github.com/Tory18.png" width="150px" style="border-radius: 50%;" alt="Vitória Edward"/><br />
        <span style="font-weight: bold; font-size: 16px; color: #333;">Vitória Edwards</span>
      </a><br />
      <span style="font-size: 14px; color: #777;">Developer</span>
    </td>
  </tr>
</table>
</div>


- Giovani Artil Oliveira de Carvalho (giovaniartil@icomp.ufam.edu.br)
- Jorge Samuel Silva Coelho (samcoelho@icomp.ufam.edu.br)
- Renata Modesto Fernandes (renata.modesto@icomp.ufam.edu.br)
- Sofia Pinho Icavino Moura (sofiaicavino@icomp.ufam.edu.br)
- Vitória Luz Edwards (vitoria.edwards@icomp.ufam.edu.br)
