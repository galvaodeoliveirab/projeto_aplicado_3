<img src="https://capsule-render.vercel.app/api?type=waving&color=FF6666&height=120&section=header" width="100%" align="center"> <img src="http://meusite.mackenzie.br/rogerio/mackenzie_logo/UPM.2_horizontal_vermelho.jpg" width="100%" align="center"> <br><br><br>
Projeto Aplicado III — Sistema de Recomendação de Cursos Online (Udemy) | ODS 4 🎓📚

Universidade Presbiteriana Mackenzie — Faculdade de Computação e Informática

Autores

Bruno Galvão de Oliveira Lima — TIA: 10441285

Vitória Ferreira Corrêa — TIA: 10441482

Lucas Santos Borba de Araújo — TIA: 10176256

Anna Teresa Soares Sacchi — TIA: 10441273

Docente

Profa. Carolina Toledo Ferraz

São Paulo — 2025

Resumo

Desenvolvimento de um sistema de recomendação de cursos online com base no Udemy Course Recommendation Dataset (Kaggle), visando personalizar trilhas de aprendizagem e apoiar o ODS 4 – Educação de Qualidade. A solução inicial utiliza recomendação baseada em conteúdo (TF-IDF + Similaridade do Cosseno), com análise exploratória, preparação de dados e prova de conceito implementadas em Python.

Sumário

Introdução

1.1 Contexto do trabalho

1.2 Motivação

1.3 Justificativa

1.4 Objetivos gerais e específicos

Referencial Teórico

Metodologia

3.1 Resultados Parciais (Prova de Conceito)

Referências Bibliográficas

Repositório e Arquivos

1. Introdução
1.1 Contexto do trabalho

Sistemas de recomendação reduzem sobrecarga informacional e personalizam a experiência do usuário em plataformas digitais (ex.: Netflix, Amazon, YouTube). No e-learning, a abundância de cursos exige mecanismos que considerem preferências e nível de conhecimento para evitar dispersão e evasão, alinhando-se ao ODS 4.

1.2 Motivação

A quantidade massiva de cursos em ambientes como Udemy/Coursera/edX dificulta a escolha. Propõe-se um sistema que facilite o acesso a conteúdos relevantes, aumente motivação/permanência e permita aplicar técnicas modernas de ciência de dados em cenário real, com impacto social (ODS 4).

1.3 Justificativa

Uso do Udemy Course Recommendation Dataset (Kaggle) pela amplitude e riqueza de atributos (título, link, gratuidade, preço, inscritos, avaliações, nível, duração), adequados à modelagem de recomendação. O projeto favorece democratização do ensino com sugestões personalizadas.

1.4 Objetivos gerais e específicos

Geral: desenvolver e avaliar um sistema de recomendação de cursos online alinhado ao ODS 4.
Específicos: EDA; tratamento/padronização; implementação e comparação de conteúdo/colaborativa/híbrida; avaliação com precisão@N, recall@N, NDCG, diversidade e cobertura; análise de cold start; diretrizes para uso educacional.

2. Referencial Teórico

Abordagens clássicas: filtragem colaborativa (vizinhança/itens), baseada em conteúdo (características dos itens) e híbrida (combinação de ambas). Fundamentação em Ricci, Rokach e Shapira; Sarwar et al.; Lops, De Gemmis e Semeraro; Burke; e estudos nacionais que discutem personalização e retenção em AVAs.

3. Metodologia

Bibliotecas: pandas, numpy, matplotlib, seaborn, scikit-learn.
EDA: estatísticas, inspeção de colunas e visualizações (preço, nível, inscritos, avaliações, duração).
Tratamento/Preparação: limpeza e padronização textual, seleção de atributos, geração do arquivo udemy_cleaned_for_training.csv.
Técnica (etapa atual): baseada em conteúdo com TF-IDF (representação textual) e Similaridade do Cosseno (proximidade entre cursos).
Avaliação (planejada): precisão@N (relevância nos top-N), recall@N, NDCG (qualidade do ranqueamento), cobertura (percentual do catálogo recomendável) e diversidade/novidade (variedade das sugestões).

3.1 Resultados Parciais (Prova de Conceito)

Dataset limpo e pronto para modelagem (udemy_cleaned_for_training.csv).

Protótipo funcional que recomenda cursos semelhantes via TF-IDF + Cosseno.

Notebooks e código disponíveis no repositório.

4. Referências Bibliográficas

RICCI, F.; ROKACH, L.; SHAPIRA, B. Recommender Systems Handbook. Springer, 2011/2022.

SARWAR, B. et al. Item-Based Collaborative Filtering Recommendation Algorithms. WWW, 2001.

LOPS, P.; DE GEMMIS, M.; SEMERARO, G. Content-based Recommender Systems: State of the Art and Trends. In: Ricci et al., 2011.

BURKE, R. Hybrid Recommender Systems: Survey and Experiments. UMUAI, 2002.

Estudos nacionais sobre personalização e retenção em AVAs (ex.: Machado & Silva, 2020; Lima & Andrade, 2022).

5. Repositório e Arquivos

Repositório: https://github.com/galvaodeoliveirab/projeto_aplicado_3

Notebooks: EDA_Udemy.ipynb, Preparacao_Udemy.ipynb, PoC_Recomendacao_Udemy.ipynb

Dados (entrada): udemy_course_data.csv

Dados (tratado): udemy_cleaned_for_training.csv

Dataset (fonte): Kaggle — https://www.kaggle.com/datasets/evilspirit05/udemy-course-recommendation/data

Estrutura e seções alinhadas ao documento da entrega 2 (PDF). 

Proj Aplicado 3 - Entrega 2

<img src="https://capsule-render.vercel.app/api?type=waving&color=FF6666&height=120&section=footer" width="100%" align="center"> ::contentReference[oaicite:1]{index=1}
