# Inicializando os contadores (as variáveis que vão guardar os números)
excelente = 0
bom = 0
ruim = 0

# O loop vai rodar 10 vezes pedindo os dados
for i in range(10):
    print(f"Entrevistado {i+1}")
    nome = input("Nome: ")
    idade = input("Idade: ")
    voto = input("Opinião (1-Excelente, 2-Bom, 3-Ruim): ")

    # AQUI É O CONTADOR: Ele não printa nada, ele SOMA na memória
    if voto == '1':
        excelente += 1
    elif voto == '3':
        ruim += 1
    elif voto == '2':
        bom += 1

# FINAL: O programa cospe o que acumulou nas variáveis
print("\nSoma total das respostas:")
print(f"EXCELENTE: {excelente}")
print(f"RUIM: {ruim}")
