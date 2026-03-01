# Challenge TelecomX pt2

📍 Projeto é de uso pessoal e educacional , desenvolvido através do : `Challenge Telecom X: análise de evasão de clientes - Parte 2`  da  `@Alura` + `@oracle_university`.
Este notebook documenta um projeto de Machine Learning , a análise e predição de evasão de clientes na empresa.

# **Transformação do dataset:**
- Arquivo usado : `dados_telecom.csv`

- As variáveis categóricas foram transformadas em numéricas para ser realizado o calculo da correlação e logo após para o encoding dos dados

# **Correlação :**
- Gênero , cobrança total e serviço de telefone são variáveis irrelevantes ou por *multicolinearidade* por isso foram apagadas

- Idosos têm leve tendência maior de evasão

A uma correlaçao alta entre os serviços :
- segurança_online
- backup_online
- suporte_tecnico
- protecao_dispositivo
- tv_streaming
- filmes_streaming

# **Balanceamento dos dados:**
Por conta de o numero de clientes em que ouve a evasão ser MENOR do que os clientes que permaneceram com:
- 26% de evasão e 71% de permanência

O modelo poderia 'chutar' o resultado para permanência do cliente , por ter a maior porcentagem de dados


Foi realizado um balanceamento de dados de classes com Undersampling onde Reduz a quantidade de exemplos da classe majoritária para equilibrar com a classe minoritária.
Mas não foi utilizado pois ouve muita perda de dados e uma acurácia média de 71%

### **Modelo Base utilizado foi o DummyClassifier com 71% de acurácia**

## **Modelo Implementados:**


### **DecisionTreeClassifier**
com 77% de Acurácia e onde as features mais importantes foram :

- segurança online , meses de contrato , serviço de internet e tipo de contrato


**Para modelos como SVM , KNeighborsClassifier e LogisticRegression foi realizado a normalização dos dados**


### **Modelo SVM obteve 77% de Acurácia**

### **Modelo KNeighbornsClassifier obteve 74% de acurácia**

*Ambas as bibliotecas não tem suporte para FeatureImportance, logo não é possível visualizar as features mais importantes*


---
### **Modelo LogisticRegression teve 78% de acurácia.**

Em que a veriável contrato deve mais importância , logo contratos mensal geram maior evasão
e contratos de 2 anos geram menor evasão

- Serviços de internet também influenciam na evasão de clientes

- Faturas Digitais  tendem a diminuir a chance de evasão

- Clientes casados também tem menor probabilidade

---
# **Recomendações**

- Incentivar pagamento digital / automático
- Melhorar o serviço de internet pois Fibra óptica tem a maior porcentagem de evasão
- Icentivar o uso de serviços adicionais mencionados em *correlação*
- Recomendar planos de maior duração






# Tecnologias Utilizadas 🔨
- Pandas
- numpy
- matplotlib
- seaborn
- scikit-learn
- Python
