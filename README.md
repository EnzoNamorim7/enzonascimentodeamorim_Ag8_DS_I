import random

# 1. Definimos os dados (isso aqui simula o que seria digitado)
votos = ['1', '2', '3', '1', '1', '2', '3', '1', '2', '3']

# 2. OS CONTADORES (Eles começam em zero)
total_excelente = 0
total_bom = 0
total_ruim = 0

# 3. A LÓGICA DE CONTAGEM (O 'for' passa por cada voto e o 'if' soma no contador)
for resposta in votos:
    if resposta == '1':
        total_excelente += 1  # Aqui o contador de excelente SOBE 1
    elif resposta == '2':
        total_bom += 1        # Aqui o contador de bom SOBE 1
    elif resposta == '3':
        total_ruim += 1       # Aqui o contador de ruim SOBE 1

# 4. EXIBIÇÃO DO TOTAL ACUMULADO
print("Soma total das respostas:")
print(f"Total Excelente: {total_excelente}")
print(f"Total Ruim: {total_ruim}")
