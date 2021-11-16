# Criação de um ambiente virtual no Python 3

### Requisitos mínimos para instalação:

>> Sistema operacional Linux (Ubuntu 20.04.2 LTS)  <br/>Memória RAM de 4GB ou mais  <br/>Python 3 instalado

Os ambientes virtuais no Python são muito úteis quando você quer criar várias aplicações Python em um único servidor, mas que cada aplicação tenha a necessidade de trabalhar com bibliotecas distintas ou até mesmo em comum só que com conversões diferentes. <br/>Exemplo de dois projetos de ciência de dados, onde o primeiro utilize as versões ````Pandas 1.3.2```` e ````NumPy 1.17```` e o segundo utilize o ````Pandas 1.3.4```` e ````Numpy 1.21````, supostamente por um possível comportamento diferente entre algumas funções ````Numpy````, isso pode ser útil quando for necessário atualizar a versão de alguma biblioteca em seus projetos que já estejam em produção, pois assim você teria duas versões do seu código fazendo os testes necessários na nova verão, sem colocar em risco seu programa principal.

- Aqui seria uma representação gráfica de como é a distribuição de ambientes virtuais em um servidor, que poderia ser uma máquina Linux, Windows ou MAC.

![Ambientes Virtuais](https://drive.google.com/uc?export=view&id=19N32y7QMMrJum-nOiJLvR5FXGI_clhAc)

# Criando um ambiente virtual 

Primeiro você tem que descobrir qual é a versão do Python 3 que está instalada em sua máquina. 

- Utilize o seguinte comando:

````
python3 -V
````
 
![Versão Python 3](https://drive.google.com/uc?export=view&id=1zq6YUCBXtRmzShJApmjxTIObJZLW3dI4)

Nesse nosso exemplo vamos utilizar o Python3 na sua versão ````Python 3.8.10````, caso você não tenha ele instalado instale com o seguinte comando:

````
sudo apt install python3.8 -y
````

- Pronto, agora vamos instalar a biblioteca ````VENV```` que é responsável pela criação dos ambientes virtuais.

````
sudo apt install python3.8-venv -y  
````

![Instalação VENV](https://drive.google.com/uc?export=view&id=1zrfv_pn2z9H47WgDkvSOdp-F2GDrPAo9)

Quando você for fazer a administração do seu ambiente instalando novas bibliotecas e removendo outras a ativação via terminal é importante, já na execução dos códigos pode ser feita pelo terminal com o ambiente ativo ou com o interpretador do ambiente em questão adicionado no cabeçalho de seus códigos.

- Criando o ambiente virtual ````env````

````
python3 -m venv env
````

- Ativar o ambiente virtual

````
source env/bin/activate
````

![Ativação ENV](https://drive.google.com/uc?export=view&id=1zrtv0BC3J3tN58eHHx2WMsZYY53M1oCk)

- Instalando bibliotecas no ambiente

````
pip install pandas 
````

![Instalando Pandas](https://drive.google.com/uc?export=view&id=1zxNNx2fou7DyTlR49Ksw-Bcxfv-tO0w2)

Agora temos que localizar o interpretador do nosso ambiente para adiciona-lo no cabeçalho do código Python.

- Com o ambiente ativo execute o comando ````which````, esse comando vai nos mostrar onde está no interpretador, e com ele em mãos vamos adicionar no nosso primeiro código em Python ````teste.py````.

````
which python3
````

![Executando Which](https://drive.google.com/uc?export=view&id=19-iSoLHBLEVoQz7hXwt7POA4APVh9uX5)

Crie o arquivo ````teste.py```` e adicione o interpretador.

![Print Arquivo teste.py](https://drive.google.com/uc?export=view&id=195WD6FhsD2Hhv-CSO5_nZPRZFNpgleRh)

Testando a execução do nosso código, nesse exemplo aqui vamos importar a biblioteca Pandas e executar um print, pois como nosso ambiente ````env```` tem o Pandas instalado nosso código vai ser executado com sucesso.

![Execução Arquivo teste.py](https://drive.google.com/uc?export=view&id=19JSZTvq-SHGRkOcoEYkpWsiKE8qDdTKt)

Pronto, agora você já sabe como criar ambientes virtuais no Python, como fazer sua administração e o melhor como executar seus códigos no ambiente.

Em breve volto com mais dicas de Python.

<b>Até!</b>

> **Referências:**  <br/><font size="1">Python.org, **Beginner's Guide to Python.** Disponível em: <https://wiki.python.org/moin/BeginnersGuide>. Acesso em: 12 nov. 2021.  <br/>Python.org, **venv - Criação de ambientes virtuais.** Disponível em: <https://docs.python.org/pt-br/3/library/venv.html>. Acesso em: 12 nov. 2021.  <br/>Python.org, **Instalando Módulos Python.** Disponível em: <https://docs.python.org/pt-br/3/installing/index.html#install-pip-in-versions-of-python-prior-to-python-3-4>. Acesso em: 12 nov. 2021.  <br/></font>
