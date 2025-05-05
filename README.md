
# 🧠 DCGAN com CelebA — Geração de Rostos com IA

Este projeto implementa uma **Deep Convolutional Generative Adversarial Network (DCGAN)** usando PyTorch para gerar imagens realistas de rostos humanos com base no dataset **CelebA** (Celeb Faces Attributes Dataset).

> O objetivo é treinar uma rede neural que aprenda a criar rostos de pessoas fictícias a partir de ruído aleatório.

---

## 📂 Dataset - CelebA

- **Fonte**: [CelebA Dataset](http://mmlab.ie.cuhk.edu.hk/projects/CelebA.html)
- **Conteúdo**: Mais de 200.000 imagens de rostos de celebridades
- **Formato**: Imagens JPG 178x218, alinhadas e recortadas
- **Uso**: Comum em pesquisas de GANs e geração de rostos

---

## ⚙️ Arquitetura do Modelo

### Generator
- Camadas `ConvTranspose2D` para upsampling
- `BatchNorm` + `ReLU`
- `Tanh` na saída para normalizar as imagens [-1, 1]

### Discriminator
- Camadas `Conv2D` para downsampling
- `BatchNorm` + `LeakyReLU`
- `Sigmoid` para saída binária (real ou fake)

> Baseado no paper [DCGAN - Radford et al., 2015](https://arxiv.org/abs/1511.06434)

---

## 🔧 Como Executar o Projeto

### 1. Clonar o repositório
```bash
git clone https://github.com/Viitor22/DCGAN.git
cd DCGAN
```

### 2. Instalar dependências
```bash
pip install -r requirements.txt
```

### 3. Baixar o dataset CelebA
- Registre-se e baixe em: http://mmlab.ie.cuhk.edu.hk/projects/CelebA.html
- Extraia para a pasta `data/img_align_celeba/`

### 4. Treinar o modelo
- Rode o notebook

### 5. Visualizar resultados
As imagens geradas são salvas em:

```
outputs/real/
```

Você também pode usar o TensorBoard (se estiver rodando localmente):

```bash
tensorboard --logdir logs
```

---

## 🧪 Tecnologias Utilizadas

- Python 3.8+
- PyTorch
- Torchvision
- TensorBoard
- Matplotlib

---

## 📜 Licença

Este projeto é distribuído sob a licença MIT.

---

## 🤝 Créditos

- Baseado no artigo original [Unsupervised Representation Learning with DCGANs](https://arxiv.org/abs/1511.06434)
- Dataset: [CelebA](http://mmlab.ie.cuhk.edu.hk/projects/CelebA.html)
