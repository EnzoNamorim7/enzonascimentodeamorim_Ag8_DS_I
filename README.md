import random

# Definimos os 10 entrevistados
TOTAL = 10

# Criamos uma lista com opiniões variadas para garantir que o contador tenha o que contar
# 1=Excelente, 2=Bom, 3=Ruim
dados_da_pesquisa = ['1', '2', '3', '1', '2', '3', '1', '1', '2', '3']

# Zera os contadores antes de começar
excelente = 0
bom = 0
ruim = 0

# O loop FOR vai passar por cada item da lista acima
for opiniao in dados_da_pesquisa:
    
    # IMPORTANTE: Verificamos se a opinião é igual ao texto '1', '2' ou '3'
    if opiniao == '1':
        excelente = excelente + 1
    elif opiniao == '2':
        bom = bom + 1
    elif opiniao == '3':
        ruim = ruim + 1

# Saída limpa e direta
print("Soma total das respostas:")
print(f"EXCELENTE: {1}")
print(f"BOM: {2}")
print(f"RUIM: {3}")
