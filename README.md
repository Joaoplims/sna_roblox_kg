# Roblox Social Network Analysis & Knowledge Graph

Este repositório contém os notebooks e scripts Python utilizados para a construção, tratamento e análise topológica da rede social do Roblox, desenvolvidos como parte da pesquisa acadêmica em Análise de Redes Sociais (SNA) e modelagem de Grafos de Conhecimento (KG).

O projeto investiga padrões de afiliação e a clusterização de usuários iniciantes em torno de *hubs* de grande engajamento, utilizando uma abordagem metodológica baseada em dados pseudonimizados.

## 🛠️ Metodologia Técnica

O pipeline de processamento foi desenhado para lidar com grandes volumes de dados de forma eficiente:

1.  **Coleta:** Técnica de amostragem em bola de neve (*Snowball Sampling*) via Roblox Open API.
2.  **Modelagem:** Utilização da biblioteca `NetworkX` para a construção de Grafos Direcionados (`nx.DiGraph`).
3.  **Otimização:** Instanciação de grafos via `itertuples` para garantir performance em larga escala.
4.  **Sanitização:** Aplicação de filtros `Regex` para expurgo de artefatos de texto não conformes com UTF-8.
5.  **Privacidade:** Política de minimização de dados, operando exclusivamente com IDs numéricos (pseudonimização) para adequação ética.

## 📊 Visualização e Análise

O tratamento final, o cálculo de métricas de centralidade e a espacialização foram realizados no software **Gephi**, utilizando os layouts:

*   **OpenOrd:** Detecção de comunidades e separação de ilhas.
*   **ForceAtlas2:** Refinamento espacial baseado na distribuição de forças gravitacionais.

## ⚠️ Limitações Metodológicas

Os resultados devem ser interpretados sob as seguintes restrições:
*   **Viés de Vizinhança:** A rede foi induzida por um nó semente específico, o que hiper-representa a vizinhança topológica do estúdio inicial.
*   **Escopo:** O recorte de 72.889 nós representa uma fração específica do ecossistema global do Roblox.

---
*Desenvolvido como parte das atividades de pesquisa para o Programa de Pos Graduação em Informática da PUC-Minas.*
