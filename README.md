# Machine Learning na Pratica
![Azure](https://img.shields.io/badge/azure-%230072C6.svg?style=for-the-badge&logo=microsoftazure&logoColor=white)
## Atividade do Bootcamp Microsoft Azure AI Fundamentals - na DIO

##### [Documentação Completa](https://microsoftlearning.github.io/mslearn-ai-fundamentals/Instructions/Labs/01-machine-learning.html)


 -Quando o trabalho automatizado de aprendizado de máquina for concluído, click em "Nome do algoritmo" na parte de Melhor Resumo de Modelo(na parte inferior direita).

![Captura de tela de 2024-03-08 03-24-05](https://github.com/MarcioCosta013/Machine-Learning-na-Pratica/assets/87935294/667d1fcc-7fd7-4228-9d93-7c31319f7146)

Apos clicar vai para essa tela:

![Captura de tela de 2024-03-08 03-31-49](https://github.com/MarcioCosta013/Machine-Learning-na-Pratica/assets/87935294/66e381a2-3537-4ef5-9dbd-9ec3d1a465c9)

Na guia *Modelo* do melhor modelo treinado pelo seu trabalho automatizado de machine learning, selecione **Implantar** e use a opção de **serviço Web** para implantar o modelo com as seguintes configurações:
- Nome : prever-aluguéis
- Descrição : Prever aluguel de bicicletas
- Tipo de computação : Instância de Contêiner do Azure
- Habilitar autenticação : selecionado
Aguarde o início da implantação – isso pode levar alguns segundos. O status de implantação do endpoint de previsão de aluguel será indicado na parte principal da página como Running .
Aguarde até que o status da implantação mude para Succeeded . Isso pode levar de 5 a 10 minutos...

![Captura de tela de 2024-03-08 03-33-58](https://github.com/MarcioCosta013/Machine-Learning-na-Pratica/assets/87935294/ba94a3f5-aec7-4533-bce5-ccfa5c83bbb1) 

![2](https://github.com/MarcioCosta013/Machine-Learning-na-Pratica/assets/87935294/c1a79495-493e-4c94-8413-cbb0c72d2b36)

### Testar o serviço implantado

Agora você pode testar seu serviço implantado.

- No estúdio Azure Machine Learning, no menu esquerdo, selecione **Pontos de Extremidade** ou Endpoint e abra o ponto final em tempo real de *prever-alugueis*.
- Na página do Pontos de Extremidade em tempo real de *prever-alugueis*, visualize a guia **Testar** .

![1](https://github.com/MarcioCosta013/Machine-Learning-na-Pratica/assets/87935294/fae50a5a-ee6c-4a89-9666-038f5aa526f6)

![2](https://github.com/MarcioCosta013/Machine-Learning-na-Pratica/assets/87935294/741dc60b-b3de-436a-bf51-412ec61f1045)


No painel Dados de entrada para testar o Pontos de Extremidade , substitua o modelo JSON pelos seguintes dados de entrada [(Desse Arquivo)](https://github.com/MarcioCosta013/Machine-Learning-na-Pratica/blob/main/test.json):

````
 {
   "Inputs": { 
     "data": [
       {
         "day": 1,
         "mnth": 1,   
         "year": 2022,
         "season": 2,
         "holiday": 0,
         "weekday": 1,
         "workingday": 1,
         "weathersit": 2, 
         "temp": 0.3, 
         "atemp": 0.3,
         "hum": 0.3,
         "windspeed": 0.3 
       }
     ]    
   },   
   "GlobalParameters": 1.0
 }

````
- Cleque em Testar e esse vai ser o Resultado:

````
{1 item
  "Results":[1 item
    0:float434.0838880916473
  ]
}
````
![Captura de tela de 2024-03-08 03-53-49](https://github.com/MarcioCosta013/Machine-Learning-na-Pratica/assets/87935294/7720f71c-8e56-42a9-a396-c82145817d29)

E pronto! Tudo certo! 
