# Classificador de Imagens com AlexNet e Integração Telegram

Este repositório contém uma implementação genérica para classificação de imagens utilizando AlexNet. O código permite que os usuários definam suas próprias classes e datasets para treinar e avaliar o modelo. Além disso, há um script para integração com um bot do Telegram que permite a classificação de imagens diretamente pelo aplicativo.

## Introdução

Este projeto oferece uma estrutura flexível para tarefas de classificação de imagens usando a arquitetura AlexNet. Os usuários podem especificar seus próprios datasets e classes para treinar um modelo personalizado. O código é projetado para ser amigável e adaptável a várias necessidades de classificação.

## Recursos

- Classificação genérica de imagens com AlexNet
- Classes e datasets definidos pelo usuário
- Aumento de dados e pré-processamento
- Divisão de dados para treinamento, validação e teste
- Early stopping e salvamento de checkpoints do modelo
- Métricas de desempenho: Acurácia, Precisão, Recall, F1 Score
- Integração com bot do Telegram para classificação de imagens

## Requisitos

- Python 3.6+
- PyTorch
- Torchvision
- NumPy
- Scikit-learn
- Google Colab (se usar Google Drive para o dataset)
- pyTelegramBotAPI

## Uso

Clone o repositório:
```bash
git clone https://github.com/seuusuario/image-classifier-alexnet-telegram.git
cd image-classifier-alexnet-telegram
```

## Instale os pacotes necessários:
```
pip install -r requirements.txt
```

## Monte seu Google Drive (se usar Colab):
```
from google.colab import drive
drive.mount('/content/drive')

```

## Abra o arquivo de script e defina o caminho para seu dataset e as classes:
```
path_to_images = '/content/drive/MyDrive/caminho-do-seu-dataset'
classes = ['classe1', 'classe2', 'classe3']

```

## Execute o script:

```
python main.py

```

O modelo é treinado com o dataset e classes especificadas. O script lida com aumento de dados, treinamento, validação e early stopping. Após o treinamento, o modelo é avaliado no conjunto de teste. O script fornece métricas como acurácia, precisão, recall e F1 score. Os resultados da avaliação são exibidos no console e incluem um relatório de classificação detalhado.

# Bot do Telegram
Para usar o bot do Telegram, siga os passos abaixo:

## Crie um bot no BotFather do Telegram e obtenha o token.
Instale a biblioteca pyTelegramBotAPI:

```
pip install pyTelegramBotAPI

```

## Configure o token do bot no script api_telegram.py

```
TOKEN = "SEU_TOKEN_AQUI"

```

## Execute o script api_telegram.py:

```
python api_telegram.py

```

Envie uma imagem para o bot no Telegram para receber a classificação.

Contribuições são bem-vindas para melhorar a funcionalidade e o desempenho deste projeto. Por favor, siga estes passos para contribuir: Faça um fork do repositório. Crie uma nova branch (git checkout -b feature-branch). Commit suas mudanças (git commit -am 'Adicionei nova funcionalidade'). Push para a branch (git push origin feature-branch). Crie um novo Pull Request.

Este projeto está licenciado sob a Licença MIT - veja o arquivo LICENSE para detalhes.
