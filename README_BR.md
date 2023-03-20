# Vibrações


## Resumo

Essa pasta contém códigos feitos para o curso de vibrações na UnB.
Em resumo, a EDO de dinâmica é dada por

$$m \ddot{x} + c \dot{x} + k x = f$$

Tem-se os seguintes casos:

* Vibração livre (```f = 0```):
    * Resolução analitica da equação
    * Implementação da solução numérica
* Vibração harmônica (```f = f0*exp(i*w*t)```):
    * Resolução analitica da equação
    * Implementação da solução numérica
    * Análise de frequência do sistema
* Vibração não oscilatória (```f``` transiente):
    * Resolução analítica usando transformada de Laplace
    * Implementação da solução numérica
* Sistema de vários graus de liberdade:
    * Decomposição modal
    * Absorvedor dinâmico de vibrações
* Experimental: Estimar parâmetros
    * Experimento de vibração livre
    * Experimento de vibração harmônica

Alguns documentos estão escritos em Ingles (indicados por ```EN```) e outros em Português (```BR```).

## Documentos

* Homework
    * ```BR``` - ```Homework/1_VigaMassaEquivalente.pdf```: Dada uma viga com resistência à flexão ```EI``` e densidade linear ```mu```, estimamos a massa ```m``` and mola ```k```  equivalente do primeiro modo de frequência.
    * ```BR``` - ```Homework/2_EquacoesGovernantes.pdf```: Modela dois objetos (encontrar a EDO) usando a equação diferencial da mecânica lagrangeana.
    * ```EN``` - ```Homework/3_DropMass.ipynb```: Modela a colisão de um objeto livre em outro conectado a uma mola e amortecedor.
    * ```BR``` - ```Homework/4_MassaDesbalanceada.pdf```: Modela um rotor desbalanceado que rotaciona com velocidade angular ```w```.
    * ```EN``` - ```Homework/5_VaribleForce.ipynb```: Encontra a posição ```x``` do sistema massa-mola-amortecedor com força ```f``` decomposta em ```degrau``` e ```rampa``` usando a transformada de laplace.
* Experimental
    * ```BR``` - ```Experimental/first_experiment/```: Usando um martelo em uma viga em balanço, encontramos os parâmetros vibracionais ```xi``` e ```wn``` do decaimento exponencial da resposta ```a``` medido por um acelerômetro. Utiliza a teoria do arquivo ```estimate-exponential-decay.ipynb```.
    * ```BR``` - ```Experimental/second_experiment/```: Usando uma viga em balanço conectada a um pistão oscilante na sua extremidade, encontramos os parâmetros ```m```, ```c``` e ```k``` dos gráficos temporais da força ```f``` e aceleração ```a``` com diferentes frequências. Usa a teoria do arquivo ```estimate-forced-harmonic.ipynb```.
* ```EN``` - ```dynamic-vibration-absorber.ipynb```: Tranforma um sistem massa-mola-amortecedor de 1 GL (grau de liberdade) em um sistema com dois GLs para minimizar o ganho ```X1``` do primeiro objeto (```m1```, ```c1```, ```k1``` fixos) adicionando um outro massa-mola-amortecedor (```m2```, ```c2```, ```k2``` variável)
* ```EN``` - ```estimate-exponential-decay.ipynb```: Usando gráficos temporais 'medidos' (dados ruidosos gerados artificialmente) da aceleração ```a``` de um sistema massa-mola-amortecedor, encontramos os melhores parâmetros ```xi``` e ```wn``` para ajudar a curva ```x``` usando o método dos mínimos quadráticos não linear com o método de newton. Feito para o primeiro experimento ```first_experiment```.
* ```EN``` - ```estimate-forced-harmonic.ipynb```: Usando gráficos temporais 'medidos' (dados ruidosos gerados artificialmente) da força ```f``` e aceleração ```a``` com diferentes frequências ```w``` de um sistema massa-mola-amortecedor, encontramos os melhores valores para ```m```, ```c``` e ```k``` do sistema utilizando o método dos mínimos quadráticos. Feito para o segundo experimento ```second_experiment```.
* ```BR``` - ```forcamento-harmonico.ipynb```: Usando um sistema massa-mola-amortecedor com força harmônica aplicada ```f0*exp(i*w*t)```, calculamos a resposta analítica e numérica dados parâmetros  ```m```, ```c``` e ```k``` com condições iniciais ```x0``` e ```v0```.
* ```BR``` - ```sistema-massa-mola.ipynb```: Usando um sistema massa-mola-amortecedor livre (```f=0```) com parâmetros ```m```, ```c``` e ```k``` com condições iniciais ```x0``` e ```v0```, nós calculamos a resposta analítica e numérica do sistema.
* ```EN``` - ```multi-dofs-system.ipynb```: Tem a teoria e uma implementação numérica da decomposição modal para um sistema de ```N``` graus de liberdade.