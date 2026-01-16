# exerc-cios-fixa-o
realizei alguns exercícios para fixar melhor algumas funções do Python:

# EXERCÍCIO 1:
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

    numero_aleatorio = random.randint(1, 11) # Gera um número entre 1 e 11 (inclusive)
    acertou = False

    while not acertou:
        try:
            valor = int(input('Digite um número de 1 a 10: ')).strip() # Pede o número
            if valor == numero_aleatorio:
                print('Você acertou o número!')
                acertou = True # Quebra o laço, pois acertou
            elif valor<1 or valor>10:
                print("Digite um valor positivo e inteiro de 1 a 10!")
            else:
                # Este else está no nível do if, dentro do try/while
                print('Errou, tente de novo...') # Informa que errou e continua o loop-1
        except ValueError:
            print('Você deve digitar um número válido...') # Trata erro se não for um número


# EXERCÍCIO 2:
# adicionando 1 a um valor de entrada 10 vezes:

    v = int(input('Digite uma valor: '))
     for a in range(10): 
         v = (v + 1 )
         print(v)

# EXERCÍCIO 3:
# SOMA DA LISTA COM REDUCE SEM USAR FUNÇÃO SUM:

    from functools import reduce
    
    idades = [15, 46, 75, 34, 23]
    total =  reduce(lambda x, y : x + y, idades )
    print(total)



