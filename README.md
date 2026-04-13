import random

# Configuração para 10 entrevistados
TOTAL = 10

# Garantindo opiniões variadas para o teste
votos_simulados = ['1', '1', '1', '1', '2', '2', '3', '3', '3', '2']
random.shuffle(votos_simulados)

# Contadores
excelente = 0
bom = 0
ruim = 0

# Processamento
for i in range(TOTAL):
    opiniao = votos_simulados[i]
    
    if opiniao == '1':
        excelente += 1
    elif opiniao == '2':
        bom += 1
    elif opiniao == '3':
        ruim += 1

# Exibição limpa conforme solicitado
print("Soma total das respostas:")
print(f"EXCELENTE: {excelente}")
print(f"BOM: {bom}")
print(f"RUIM: {ruim}")
