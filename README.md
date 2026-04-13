import random

# Simulação para 10 entrevistados (conforme solicitado para o teste)
# 1 = Excelente, 2 = Bom, 3 = Ruim
votos = ['1', '2', '3', '1', '1', '2', '3', '1', '2', '3']

# Contadores iniciados em zero
excelente = 0
bom = 0
ruim = 0

# Estrutura de repetição FOR
for opiniao in votos:
    # Estrutura de decisão para contagem
    if opiniao == '1':
        excelente += 1
    elif opiniao == '2':
        bom += 1
    elif opiniao == '3':
        ruim += 1

# Saída exatamente como você pediu
print("Soma total das respostas:")
print(excelente)
print(bom)
print(ruim)
