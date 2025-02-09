Este é um projeto fictício. A empresa, o contexto e as perguntas de negócios não são reais. Este portfólio está seguindo as recomendações do blog  da [Comunidade DS](https://www.comunidadedatascience.com/os-5-projetos-de-data-science-que-fara-o-recrutador-olhar-para-voce/).

O notebook com todos os passos realizados está disponivel [aqui](https://github.com/fernandachuerubim/curso_ds_producao/blob/main/m04_v01_store_sales_prediction.ipynb).
O BOT com os produtos de dados em produção pode ser acessado via Telegram, pesquisando por [fernanda_rossmann_bot](http://t.me/fernanda_rossmann_bot). Ao enviar uma mensagem para o BOT, a resposta pode haver uma lentidão para aparecer, pois, o Render depois de um tempo sem uso desliga a aplicação.
O dataset está disponivel no [Kaggle](https://www.kaggle.com/c/rossmann-store-sales/data).


## 1. Problema de negócios
### 1.1 Problema
O CFO da empresa fez uma reunião com todos os Gerentes de Loja e pediu para que cada um deles trouxesse uma previsão das próximas 6 semanas de vendas. 
Depois dessa reunião, todos os Gerentes entraram em contato, requisitando uma previsão de vendas de suas lojas.

### 1.2 Motivação
O CFO está querendo fazer uma reforma nas lojas e está querendo pegar uma parte da receita de cada loja para fazer esta reforma das lojas.


### 1.3 Demandas de negócio

Produto de dados solicitado:
* Uma previsão de vendas das próximas semanas de todas as lojas da Rossmann.


## 2. Premissas de negócio
- Todos os produtos de dados entregues devem ser acessíveis via internet.
- O planejamento da solução será validado com os times de negócio, visando garantir que as soluções desenvolvidas sejam úteis na sua tomada de decisão.

As variáveis do dataset original são:

Variável | Definição
------------ | -------------
|id | Um Id que representa uma tupla (Store, Date) dentro do conjunto de testes.|
|Store | Um ID exclusivo para cada loja.|
|Sales | O volume de negócios para um determinado dia.|
|Customers | O número de clientes em um determinado dia. |
|Open | Um indicador para saber se a loja estava aberta: 0 = fechado, 1 = aberto |
|StateHoliday | Indica um feriado estadual. Normalmente todas as lojas, com poucas exceções, estão fechadas nos feriados estaduais. Observe que todas as escolas estão fechadas nos feriados e fins de semana. a = feriado, b = feriado da páscoa, c = natal, 0 = nenhum. |
|SchoolHoliday | Indica se a (Loja, Data) foi afetada pelo fechamento de escolas públicas. |
|StoreType | Diferencia entre 4 modelos de loja diferentes: a, b, c, d |
|Assortment | Descreve um nível de sortimento: a = básico, b = extra, c = estendido. |
|CompetitionDistance| Distância em metros até a loja concorrente mais próxima. |
|CompetitionOpenSince [Month/Year] | Fornece o ano e o mês aproximados em que o concorrente mais próximo foi aberto. |
|Promo | Indica se uma loja está executando uma promoção naquele dia. |
|Promo2 | Promo2 é uma promoção contínua e consecutiva para algumas lojas: 0 = a loja não está participando, 1 = a loja está participando. |
|Promo2Since[Year/Week] | Descreve o ano e a semana do calendário em que a loja começou a participar do Promo2 |
|PromoInterval | Descreve os intervalos consecutivos em que a Promo2 é iniciada, nomeando os meses em que a promoção é iniciada novamente. Por exemplo, "fevereiro, maio, agosto, novembro" significa que cada rodada começa em fevereiro, maio, agosto, novembro de qualquer ano para essa loja. |

## 3. Planejamento da solução
### 3.1. Produto final
O que será entregue efetivamente?
- Um bot no Telegram onde vai ser necessário enviar um código da loja.

 ### 3.2. Ferramentas
Quais ferramentas serão usadas no processo?
- Visual Studio code;
- Jupyter Notebook;
- Git, Github;
- Python;
- Telegram;
- Cloud Render.
 ## 4. Os 3 principais insights dos dados

#### 1 Lojas com competidores mais próximos deveriam vender menos.
* **FALSA** Lojas com COMPETIDORES MAIS PRÓXIMOS vendem MAIS.

* Insight de negócio: Verificar quais os locais onde ficam as lojas que vendem mais,  para encontrar uma forma de reproduzir o cenário, pois, o volume de pessoas no local como shopping também podem influenciar.

#### 2 Lojas com competidores à mais tempo deveriam vender mais.
* **FALSA** Lojas com COMPETIDORES À MAIS TEMPO vendem MENOS


* Insight de negócio: Percebe que há uma tendência de as vendas se manterem em equilíbrio com o tempo. Isso pode ser mudada criando algum tipo de alavanca para o negócio. 

#### 3 Lojas com maior sortimento deveriam vender mais.
* **FALSA** Lojas com MAIOR SORTIMENTO vendem MENOS.

* Insight de negócio: Pelos dados analisados conseguimos perceber que lojas classificadas como extra são as que vendem menos em relação às que são classificadas como básicas e estendidas.

## 5. Resultados para o negócio
De acordo com os critérios definidos, foi feita uma previsão de vendas das próximas 6 semanas. Como resultado para o negócio foram criados:

* Uma API onde será feita a previsão de vendas

* Um BOT no Telegram onde o CFO e os gerentes de lojas poderão enviar o código da loja para prever a venda.

## 5. Conclusão
* O objetivo do projeto foi alcançado, dado que os produtos de dados propostos foram gerados com sucesso. O CFO e os gerentes já podem utilizar a solução para a tomada de decisão.

O Bot no Telegram pode ser  acessado por [fernanda_rossmann_bot](http://t.me/fernanda_rossmann_bot).

Abaixo mostra um exemplo de uso do bot para fazer a previsão de vendas.

<img src="https://user-images.githubusercontent.com/95532957/204401359-98453aca-c0e7-48b8-a4fb-2dddeedf7e58.gif" title="Exemplo de uso" lign="center" height="400" class="center"/>

## 7. Próximos passos

Algumas melhorias no projeto podem ser incrementadas no futuro:

* Fazer um autenticação, pois se trata de um produto para empresa;
* Mostrar mais informações sobre a loja como qual o gerente, quantos funcionários;
* Mostra métricas como CAC e LTV.

## 6 Referências
* Este Projeto foi feito como parte do curso "DS em Produção", da [Comunidade DS](https://www.comunidadedatascience.com/).
* O Dataset foi obtido no [Kaggle](https://www.kaggle.com/c/rossmann-store-sales/data).
