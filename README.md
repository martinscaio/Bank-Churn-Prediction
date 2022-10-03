# Bank Churn Prediction


## Business Problem:


Houve um aumento no número de clientes que abandonaram o serviço de cartão de crédito do banco. 

## Objetivo:

Construir um modelo de churn para prever os clientes com maior probabilidade, potencial de desistência

Assim, sabendo quais são os clientes com antecedência, é possível que o banco ofereça melhores condições para os potenciais churn.


## Dados:

O banco de dados foi obtido no [Kaggle](https://www.kaggle.com/datasets/sakshigoyal7/credit-card-customers)

Consiste no registro de 10.127 clientes contendo informações como idade, salario, limite do cartão de crédito, tipo de cartão de crédito,
o número de vezes que entrou em contato com o banco no último ano, número de meses que ficou inativo... etc. 

É possível consultar todas as variáveis no 'dicionário de variáveis'

16% dos registros - 1627 - são de clientes que fecharam suas contas. O restante 84% - 8500 são de clientes que permanecem utilizando os serviços de cartão de crédito.



## Metodologia:

Construção de um modelo de classificação para prever churn utilizando Random Forest, Decision Tree e Logistic Regression. 
O modelo final selecionado utiliza o Random Forest por ser o modelo mais promissor. Neste modelo utilizamos pre processing (One Hot Encoding), Feature Selection
(Teste Univariado F), tunagem de hiperparametros...

Fiz um modelo preliminar em R também, mas o modelo completo e final está feito em Python


## Resultados e métricas do modelo


Por que selecionamos o Random Forest ? Justamente por ser o modelo mais promissor como podemos ver na imagem abaixo

#### Comparativo entre os modelos:


![imagem_2022-09-08_170111394](https://user-images.githubusercontent.com/75284489/189214656-0fae9cbc-589a-4aa7-bd95-a2d4ea7b873e.png)



#### Qual a performance do Modelo Final utilizando Random Forest ? 

![imagem_2022-09-08_170625083](https://user-images.githubusercontent.com/75284489/189215495-88311e79-c1f0-4456-9d7b-a6b7caa30c90.png)


Importante em modelos de classificação checar outras métricas como Recall & Precision, já que accuracy é enganosa quando se trata de dados desbalanceados


#### Classification Report:


![classification_report](https://user-images.githubusercontent.com/75284489/189215997-a02c4532-373b-41e0-80f2-a7b44f06411b.png)


#### Curva ROC:

![curva_roc](https://user-images.githubusercontent.com/75284489/189216002-b3dd6215-bc32-47f2-8588-71637b20b257.png)


#### Mas afinal, quais foram as variáveis selecionadas ?

![imagem_2022-09-08_171534970](https://user-images.githubusercontent.com/75284489/189217034-07f11599-23d4-4c97-915e-b8cc2cabc7e9.png)

