<img src="https://capsule-render.vercel.app/api?type=waving&color=FF6666&height=120&section=header" width="100%">

<p align="center">
  <img src="http://meusite.mackenzie.br/rogerio/mackenzie_logo/UPM.2_horizontal_vermelho.jpg" width="55%">
</p>

# Projeto Aplicado III  
## Sistema de Recomendação de Cursos Online (Udemy) — ODS 4 🎓📚  
**Universidade Presbiteriana Mackenzie — Faculdade de Computação e Informática**  
**São Paulo — 2025**

---

## 👨‍🏫 Docente
**Profa. Carolina Toledo Ferraz**

## 👥 Autores
- **Bruno Galvão de Oliveira Lima — TIA: 10441285**  
- **Vitória Ferreira Corrêa — TIA: 10441482**  
- **Lucas Santos Borba de Araújo — TIA: 10176256**  
- **Anna Teresa Soares Sacchi — TIA: 10441273**

---

# 📘 Resumo

Este projeto desenvolve um sistema de recomendação de cursos online baseado no *Udemy Course Recommendation Dataset* (Kaggle).  
A solução envolve análise exploratória, preparação de dados, construção de representações textuais e implementação de um recomendador baseado em conteúdo, utilizando **TF-IDF** e **Similaridade do Cosseno**.  
O projeto contribui com o **ODS 4 — Educação de Qualidade**, oferecendo suporte à personalização de trilhas de aprendizagem.

---

# 📑 Sumário

1. [Introdução](#introdução)  
2. [Referencial Teórico](#referencial-teórico)  
3. [Metodologia](#metodologia)  
4. [Resultados (PoC)](#resultados)  
5. [Referências](#referências)  
6. [Repositório e Arquivos](#repositório-e-arquivos)

---

# 1. Introdução

## 1.1 Contexto  
Plataformas digitais geram excesso de opções, tornando recomendadores essenciais para personalizar experiências — Netflix, YouTube e Amazon já utilizam amplamente esse tipo de sistema.  
No ensino online, recomendadores ajudam a reduzir dispersão, orientar trilhas e apoiar permanência estudantil, alinhando-se ao **ODS 4**.

## 1.2 Motivação  
Ambientes como Udemy, Coursera e edX oferecem milhares de cursos. Escolher o conteúdo mais relevante é difícil sem apoio automatizado.  
O projeto busca facilitar essa jornada e aplicar técnicas práticas de ciência de dados com impacto social.

## 1.3 Justificativa  
O dataset da Udemy oferece atributos úteis (preço, nível, inscritos, duração, título, assunto), permitindo modelar e avaliar técnicas de recomendação aplicáveis ao e-learning.

## 1.4 Objetivos  
**Geral:** criar e avaliar um sistema de recomendação para cursos online.  
**Específicos:**  
- realizar EDA detalhada;  
- limpar e padronizar dados;  
- implementar técnicas baseadas em conteúdo;  
- avaliar pipelines;  
- fornecer base para extensões futuras (colaborativa/híbrida).

---

# 2. Referencial Teórico

Os principais modelos estudados incluem:  
- **Filtragem colaborativa** (usuário-usuário, item-item) — Sarwar et al.  
- **Recomendação baseada em conteúdo** — Lops, De Gemmis, Semeraro.  
- **Sistemas híbridos** — Burke.  
- Trabalhos brasileiros sobre personalização em ambientes virtuais de aprendizagem — Machado & Silva; Lima & Andrade.

Essas abordagens reforçam o uso de atributos textuais, interações e metadados para identificar itens semelhantes.

---

# 3. Metodologia

### 🔧 Bibliotecas utilizadas  
`pandas`, `numpy`, `matplotlib`, `scikit-learn`

### 🔍 Etapas
- **EDA**  
  Visualizações de distribuição de preço, duração, nível, assuntos e inscritos.  
- **Preparação**  
  • limpeza textual  
  • normalização  
  • criação de corpus  
  • exportação do dataset tratado  
- **Modelagem (PoC)**  
  TF-IDF + Similaridade do Cosseno para encontrar cursos semelhantes.  
  Três pipelines foram comparadas:
  - v1 — título  
  - v2 — título + assunto  
  - v3 — título + assunto + nível  
- **Avaliação**  
  Métrica utilizada: **pop_score@5** (popularidade média entre os top-5).

---

# 4. Resultados

A etapa de EDA e a PoC geraram gráficos e arquivos presentes em `/reports/`.  
Principais entregas:

- Dataset tratado: `udemy_courses_clean.csv`  
- Ranking das pipelines: `ranking_pipelines.csv`  
- Pipeline vencedora salva em: `models/best_pipeline.pkl`  
- Exemplo de recomendação para *python*: `exemplo_recomendacao_python.csv`  
- Figuras da análise exploratória em `/reports/eda/`  
- Figura de desempenho das pipelines em `/reports/poc/`  

A pipeline **v3 (título + assunto + nível)** apresentou o melhor desempenho.

---

# 5. Referências

- BURKE, R. *Hybrid Recommender Systems: Survey and Experiments*. UMUAI, 2002.  
- LIMA, R. F.; ANDRADE, P. H. *Algoritmos de Recomendação em Plataformas de Ensino Online*. RBIE, 2022.  
- LOPS, P.; DE GEMMIS, M.; SEMERARO, G. *Content-Based Recommender Systems*. In: Ricci et al. Springer, 2011.  
- MACHADO, T.; SILVA, L. *Impacto da Personalização em AVAs*. SBIE, 2020.  
- RESNICK, P.; VARIAN, H. *Recommender Systems*. CACM, 1997.  
- RICCI, F.; ROKACH, L.; SHAPIRA, B. *Recommender Systems Handbook*. Springer, 2011.  
- SARWAR, B. et al. *Item-Based Collaborative Filtering*. WWW, 2001.

---

# 6. Repositório e Arquivos

**Repositório:**  
https://github.com/galvaodeoliveirab/projeto_aplicado_3

**Notebooks:**  
- `EDA_Udemy.ipynb`  
- `Preparacao_Udemy.ipynb`  
- `PoC_Recomendacao_Udemy.ipynb`

**Dados:**  
- `dataset/udemy_course_data.csv`  
- `dataset/udemy_courses_clean.csv`

**Modelos e relatórios:**  
- `models/best_pipeline.pkl`  
- `reports/eda/*.png`  
- `reports/poc/*.png`

---

<img src="https://capsule-render.vercel.app/api?type=waving&color=FF6666&height=120&section=footer" width="100%">
