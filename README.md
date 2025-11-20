<img src="https://capsule-render.vercel.app/api?type=waving&color=FF6666&height=120&section=header" width="100%">

<p align="center">
  <img src="http://meusite.mackenzie.br/rogerio/mackenzie_logo/UPM.2_horizontal_vermelho.jpg" width="55%">
</p>

# **Projeto Aplicado III**  
## **Sistema de Recomendação de Cursos Online (Udemy) — ODS 4 🎓📚**  
**Universidade Presbiteriana Mackenzie — Faculdade de Computação e Informática**  
**São Paulo — 2025**

---

## 👨‍🏫 **Docente**
**Profa. Carolina Toledo Ferraz**

## 👥 **Autores**
- **Bruno Galvão de Oliveira Lima — TIA: 10441285**  
- **Vitória Ferreira Corrêa — TIA: 10441482**  
- **Lucas Santos Borba de Araújo — TIA: 10176256**  
- **Anna Teresa Soares Sacchi — TIA: 10441273**

---

# 📘 **Resumo**

Este projeto implementa um sistema de recomendação de cursos baseado em conteúdo utilizando o dataset *Udemy Course Recommendation* (Kaggle).  
A solução combina **TF-IDF** e **Similaridade do Cosseno** para identificar cursos semelhantes e apoiar a personalização de trilhas de aprendizagem, contribuindo diretamente para o **ODS 4 — Educação de Qualidade**.  
Foram realizadas análise exploratória, preparação dos dados, modelagem e avaliação das pipelines desenvolvidas.

---

# 📑 **Sumário**
1. [Introdução](#1-introdução)  
2. [Referencial Teórico](#2-referencial-teórico)  
3. [Metodologia](#3-metodologia)  
4. [Resultados](#4-resultados)  
5. [Referências](#5-referências)  
6. [Repositório e Arquivos](#6-repositório-e-arquivos)

---

# 1. **Introdução**

## 1.1 **Contexto**
Sistemas de recomendação são essenciais para lidar com excesso de informação e personalizar experiências em plataformas digitais. No contexto educacional, essas técnicas ajudam alunos a encontrarem conteúdos relevantes, reduzindo evasão e promovendo aprendizagem contínua.

## 1.2 **Motivação**
Plataformas como Udemy, Coursera e edX reúnem milhares de cursos. A ausência de direcionamento pode gerar dispersão e escolhas pouco eficientes. Recomendadores atuam como guias personalizados nessa jornada.

## 1.3 **Justificativa**
O dataset da Udemy contém atributos ricos (preço, nível, inscritos, assunto, duração), permitindo experimentação de abordagens modernas de recomendação aplicáveis ao e-learning.

## 1.4 **Objetivos**
**Geral:**  
Construir e avaliar um sistema de recomendação para cursos online, alinhado ao ODS 4.

**Específicos:**  
- realizar EDA;  
- preparar e padronizar dados;  
- criar corpora textuais;  
- desenvolver múltiplas pipelines TF-IDF;  
- comparar desempenho e selecionar o melhor modelo.

---

# 2. **Referencial Teórico**

Baseado em literatura clássica e atual:  
- **Filtragem colaborativa** — *Sarwar et al., 2001*  
- **Baseado em conteúdo** — *Lops, De Gemmis, Semeraro, 2011*  
- **Sistemas híbridos** — *Burke, 2002*  
- Estudos brasileiros em personalização de aprendizagem — *Machado & Silva, 2020; Lima & Andrade, 2022*

Esses trabalhos sustentam o uso de atributos dos itens e similaridade entre representações vetoriais como base para recomendação.

---

# 3. **Metodologia**

### 🔧 **Ferramentas**
`Python`, `pandas`, `numpy`, `matplotlib`, `scikit-learn`

### 🔍 **Etapas**
- **EDA**: distribuição de preço, duração, níveis, inscrições, assuntos.  
- **Preparação**: normalização textual e geração do dataset limpo.  
- **Modelagem**: construção de três pipelines TF-IDF:  
  - **v1:** título  
  - **v2:** título + assunto  
  - **v3:** título + assunto + nível  
- **Avaliação**: uso da métrica **pop_score@5** — média de inscritos entre os 5 cursos recomendados.  
- **Entrega**: modelo salvo, rankings, recomendações-exemplo e gráficos.

---

# 4. **Resultados**

Todos os resultados estão disponíveis na pasta `/reports/`.

### **Saídas principais**
- **Dataset tratado:** `udemy_courses_clean.csv`  
- **Ranking final das pipelines:** `reports/ranking_pipelines.csv`  
- **Melhor pipeline salva em:** `models/best_pipeline.pkl`  
- **Exemplo de recomendação:** `reports/exemplo_recomendacao_python.csv`  
- **Gráficos de EDA:** `/reports/eda/*.png`  
- **Gráfico do desempenho das pipelines:** `/reports/poc/desempenho_pipelines_poc.png`

### **Conclusão parcial da PoC**
A pipeline **v3 (título + assunto + nível)** obteve o melhor desempenho geral segundo a métrica pop_score@5.

---

# 5. **Referências**

- BURKE, R. *Hybrid Recommender Systems: Survey and Experiments*. UMUAI, 2002.  
- LIMA, R. F.; ANDRADE, P. H. *Algoritmos de Recomendação em Plataformas de Ensino Online*. RBIE, 2022.  
- LOPS, P.; DE GEMMIS, M.; SEMERARO, G. *Content-Based Recommender Systems*. Springer, 2011.  
- MACHADO, T.; SILVA, L. *Impacto da Personalização em AVAs*. SBIE, 2020.  
- RESNICK, P.; VARIAN, H. *Recommender Systems*. CACM, 1997.  
- RICCI, F.; ROKACH, L.; SHAPIRA, B. *Recommender Systems Handbook*. Springer, 2011.  
- SARWAR, B. et al. *Item-Based Collaborative Filtering*. WWW, 2001.

---

# 6. **Repositório e Arquivos**

📁 **Repositório:**  
https://github.com/galvaodeoliveirab/projeto_aplicado_3

📌 **Notebooks:**  
- `EDA_Udemy.ipynb`  
- `Preparacao_Udemy.ipynb`  
- `PoC_Recomendacao_Udemy.ipynb`

📌 **Dados:**  
- `dataset/udemy_course_data.csv`  
- `dataset/udemy_courses_clean.csv`

📌 **Modelos e Relatórios:**  
- `models/best_pipeline.pkl`  
- `reports/eda/*.png`  
- `reports/poc/*.png`

---

<img src="https://capsule-render.vercel.app/api?type=waving&color=FF6666&height=120&section=footer" width="100%">
