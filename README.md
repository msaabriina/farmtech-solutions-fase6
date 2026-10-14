# FIAP

<p align="center">
<a href="https://www.fiap.com.br/"><img src="assets/logo-fiap.png" alt="FIAP - Faculdade de Informática e Administração Paulista" border="0" width=40% height=40%></a>
</p>

<br>

# FarmTech Solutions — Fase 6

## 👨‍🎓 Integrantes

- [Karina Garta Szewczuk — RM569309](https://www.linkedin.com/in/)
- [Maria Sabrina Feitosa da Silva — RM568714](https://www.linkedin.com/in/)
- [Nicolas Lima Apolinário — RM570741](https://www.linkedin.com/in/)
- [Roger Gabriel de Souza Jesus Costa — RM573659](https://www.linkedin.com/in/)

## 👩‍🏫 Professores

### Tutor(a)
- [Sabrina Otoni](https://www.linkedin.com/in/)

### Coordenador(a)
- [André Godói](https://www.linkedin.com/in/)

## 📜 Descrição

O projeto FarmTech Solutions atende uma fazenda de médio porte (~200 hectares) e nesta Fase 6 a gente explora **visão computacional** pra detecção e classificação de objetos em imagens. O trabalho é dividido em duas entregas:

**Entrega 1 — Detecção de objetos com YOLOv5:** montamos uma base de 80 imagens (40 de cada objeto), rotulamos tudo no Make Sense AI (formato YOLO) e treinamos a YOLOv5 com transfer learning a partir dos pesos pré-treinados (`yolov5s.pt`). O treino é feito duas vezes — com 30 épocas e com 60 épocas — pra comparar como o número de épocas influencia a precisão, recall e mAP. No final rodamos a detecção em imagens de teste que o modelo nunca viu.

**Entrega 2 — Comparação de três abordagens de visão computacional:** pegamos a mesma base e colocamos três técnicas lado a lado:
1. **YOLO adaptada** — o modelo que treinamos na Entrega 1, com detecção dos nossos objetos;
2. **YOLO padrão** — a YOLOv5 pré-treinada na COCO (80 classes genéricas), sem nenhum treino nosso;
3. **CNN treinada do zero** — uma rede convolucional montada no Keras/TensorFlow, classificando a imagem inteira (não localiza o objeto).

Comparamos as três em facilidade de uso, precisão, tempo de treino e tempo de inferência.

## 📁 Estrutura de pastas

- **`.github`** — arquivos de configuração do GitHub
- **`assets`** — imagens usadas na documentação (logo, gráficos)
- **`config`** — parâmetros e ajustes do projeto
- **`document`** — documentos do projeto, com subpasta `other` pra materiais complementares
- **`scripts`** — scripts auxiliares
- **`src`** — notebooks e arquivos-fonte:
  - `MariaSabrinaFeitosaDaSilva_rm568714_pbl_fase6.ipynb` — notebook da Entrega 1 (YOLO)
  - `MariaSabrinaFeitosaDaSilva_rm568714_pbl_fase6_entrega2.ipynb` — notebook da Entrega 2 (comparação)
- **`README.md`** — este arquivo

## 🔧 Como executar o código

### Pré-requisitos

- Conta Google (pra usar o Colab e o Drive)
- Google Colab com **GPU habilitada** (T4)
- 80 imagens dos dois objetos, já rotuladas no [Make Sense AI](https://www.makesense.ai/) no formato YOLO
- Estrutura de pastas no Drive conforme descrito no notebook

### Passo a passo

1. **Suba a base no Drive** na estrutura:
   ```
   MyDrive/farmtech_fase6/
   └── dataset/
       ├── images/ (train/ val/ test/)
       └── labels/ (train/ val/)
   ```
2. **Entrega 1:** abra o notebook da Entrega 1 no Colab, ligue a GPU, ajuste os nomes das classes na célula de configuração e rode tudo (`Ctrl+F9`)
3. **Entrega 2:** abra o notebook da Entrega 2 no Colab (o `best.pt` já foi salvo no Drive pela Entrega 1), ligue a GPU e rode tudo

### Bibliotecas usadas

- PyTorch (via YOLOv5)
- TensorFlow / Keras (CNN da Entrega 2)
- OpenCV, Matplotlib, Pandas, NumPy
- Todas são instaladas automaticamente pelo notebook

## 🎥 Vídeos demonstrativos

- [Vídeo Entrega 1 — YOLO treinamento e detecção]([a gravar])
- [Vídeo Entrega 2 — Comparação das três abordagens]([a gravar])

## 🗃 Histórico de lançamentos

- 0.6.0 — 14/10/2026
  - Fase 6: visão computacional com YOLOv5 (detecção e comparação de abordagens)
- 0.5.0 — 08/09/2026
  - Fase 5: Machine Learning e Computação em Nuvem (repo separado)

## 📋 Licença

<img style="height:22px!important;margin-left:3px;vertical-align:text-bottom;" src="https://mirrors.creativecommons.org/presskit/icons/cc.svg?ref=chooser-v1"><img style="height:22px!important;margin-left:3px;vertical-align:text-bottom;" src="https://mirrors.creativecommons.org/presskit/icons/by.svg?ref=chooser-v1">

Este modelo está licenciado sob [Attribution 4.0 International](http://creativecommons.org/licenses/by/4.0/?ref=chooser-v1).
