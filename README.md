# exerc-cios-fixa-o
realizei alguns exercícios para fixar melhor algumas funções do Python:

# MONTAGEM DE ALGORITMO :

# dados : número sorteado e número escolhido pela pessoa
# o que fazer com os dados? compara-los e verificar se são iguais
# restrição: valor digitado deve ser de 1 a 10, inteiro e positivo
# resultado : programa encerra se os valores forem iguais e repete se não forem

# 1. sortear um número de 1 a 10
# 2. guardar o Valor
# 3. perguntar o número escolhido de 1 a 10 para a pessoa
# 4. guardar o valor
# 5. comparar os dois valores
# 6 se forem iguais encerra o programa
# 7 se forem diferentes o programa se repete a partir do passo 3

    import random
    numero_aleatorio = random.randint(1,11)
    acertou = False
    
    while not acertou: # o ciclo se repete enquanto acertou for false (valor!= numero_aleatorio)
        valor = int(input('Digite um número de 1 a 10:'))
        if valor == numero_aleatorio:
            print('Você acertou o número!')
            acertou=True # QUEBRA O LAÇO DE REPETIÇÃO - fim do código
        else:
            print('Errou tente de novo...')

# adicionando 1 a um valor de entrada 10 vezes:

    v = int(input('Digite uma valor: '))
     for a in range(10): 
         v = (v + 1 )
         print(v)

# SOMA DA LISTA COM REDUCE SEM USAR FUNÇÃO SUM:

    from functools import reduce
    
    idades = [15, 46, 75, 34, 23]
    total =  reduce(lambda x, y : x + y, idades )
    print(total)



