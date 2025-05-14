# 🔢 Conversor de Algarismos Cistercienses com Visão Computacional

Este projeto permite converter números entre o sistema **arábico** (1–9999) e o sistema **cisterciense**, utilizando técnicas de **visão computacional com Python (OpenCV)** e uma interface frontend com **Node.js/HTML/CSS**.  
A aplicação pode tanto **gerar a imagem de um número cisterciense** a partir de um número arábico digitado, quanto **reconhecer e interpretar** uma imagem cisterciense enviada pelo usuário.

---

## 📚 Contexto Histórico

O sistema cisterciense foi desenvolvido por monges da Ordem de Cister entre os séculos XII e XV. Seu diferencial era representar números de 1 até 9999 com **um único símbolo gráfico**, composto por uma linha vertical com traços nas extremidades que indicavam unidades, dezenas, centenas e milhares.

Utilizado principalmente em manuscritos, catálogos e registros, o sistema caiu em desuso com a consolidação dos algarismos arábicos.

---

## ⚙️ Funcionalidades

### ✅ Conversão Arábico ➜ Cisterciense
- **Entrada**: Número entre 1 e 9999
- **Saída**: Imagem em PNG do número representado no sistema cisterciense

### ✅ Conversão Cisterciense ➜ Arábico
- **Entrada**: Imagem carregada pelo usuário
- **Saída**: Número arábico correspondente (por comparação de similaridade)

### ✅ Interface Web integrada
- Gerador de número visual
- Upload de imagem com resultado imediato
- Visualização lado a lado dos resultados

---

## 🧰 Tecnologias Utilizadas

### Backend
- **Python 3.12+**
  - Flask (API)
  - OpenCV (processamento de imagem)
  - scikit-image (SSIM para similaridade)
  - Pillow

### Frontend
- **Node.js 18+**
  - HTML, CSS, JS puro
  - Pode ser acessado diretamente com Live Server ou HTTP server

---

## 📁 Estrutura do Projeto

```plaintext
NumerosCistercienses/
├── dataset-numbers/              # Imagens para reconhecimento da imagem inserida
├── node_modules/                 # arquivos nescessários para o node
├── number-images/                # Imagens para gerar o numero inserido pelo usuário em tela
├── output/                       # Imagem do numero inserido
├── public/
│   └── index.html                # Interface com frontend completo
│   └── style.css                 # Style do frontend
├── python/
│   └── recognize_number.py       # Verificação da imagem inserida pelo usuário
│   └── requirements.txt          # Dependências 
├── uploads/                      # Arquivo temporário da imagens inserirdas
├── utils/
│   └── imageComposer.js          # Gerador da imagem referente ao número digitado
└── app.js                        # Arquivo princial da aplicação node
└── README.md                     # Este arquivo


