# Detecção e Análise de Copas de Árvores Urbanas com YOLOv11 e K-Means

## Descrição do Projeto
Este projeto utiliza técnicas de **aprendizado profundo** (YOLOv11) e **agrupamento** (K-Means) para detectar e analisar copas de árvores urbanas em imagens aéreas. O objetivo é fornecer uma ferramenta eficiente para monitoramento ambiental, planejamento urbano e gestão de áreas verdes.

---

## Funcionalidades
1. **Detecção de Copas de Árvores:**
   - Uso do modelo **YOLOv11** para detectar copas de árvores em imagens aéreas.
   - Métricas de desempenho: **Precisão (73%)**, **Revocação (76%)**, **F1-Score (0.745)**, **mAP50 (0.75-0.80)** e **mAP50-95 (0.40-0.45)**.
   - Tempo de inferência: **30-40ms por imagem** (em GPU).

2. **Análise de Tamanho das Copas:**
   - Aplicação do algoritmo **K-Means** para classificar as copas detectadas em três categorias: **pequeno**, **médio** e **grande**.
   - Insights sobre a distribuição dos tamanhos das árvores, útil para planejamento urbano e estudos ecológicos.

3. **Pipeline Completo:**
   - Pré-processamento de imagens.
   - Treinamento e validação do modelo YOLOv11.
   - Extração de métricas e análise de resultados.

---

## Tecnologias Utilizadas
- **Linguagem de Programação:** Python.
- **Frameworks:** Ultralytics (YOLOv11), Scikit-learn (K-Means).
- **Ferramentas:** Google Colab, Pandas, NumPy, OpenCV, Matplotlib.

---

## Estrutura do Código
1. **Pré-processamento:**
   - Conversão de arquivos de anotação (.txt) para DataFrame.
   - Divisão dos dados em conjuntos de treinamento e validação.
   - Normalização e conversão das coordenadas das bounding boxes para o formato YOLO.

2. **Treinamento do Modelo:**
   - Configuração do arquivo YAML para treinamento do YOLOv11.
   - Treinamento com 200 épocas e avaliação das métricas de desempenho.

3. **Inferência e Análise:**
   - Aplicação do modelo treinado nas imagens de validação.
   - Geração de bounding boxes preditas e cálculo das áreas das copas.
   - Classificação das copas em clusters usando K-Means.

4. **Visualização:**
   - Plotagem das imagens com bounding boxes e clusters.
   - Geração de gráficos de métricas (precisão, revocação, F1-Score, mAP).

---

## Resultados
- O modelo YOLOv11 demonstrou alta eficiência na detecção de copas de árvores urbanas, com **mAP50 de 0.75-0.80**.
- A análise de clusters com K-Means revelou a distribuição dos tamanhos das copas, fornecendo insights para **gestão de áreas verdes** e **planejamento urbano**.
- O tempo de inferência rápido (**30-40ms por imagem**) torna o modelo adequado para aplicações em tempo real.

---

## Instruções para Uso
1. **Clone o Repositório:**
   ```bash
   git clone https://github.com/BrenoBragaGalvao/TreeCrown-Detection-YOLO-KMeans.git
