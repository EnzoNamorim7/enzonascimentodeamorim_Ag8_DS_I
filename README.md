import random

# Definindo a quantidade de entrevistados
# Teste com 10 conforme solicitado; altere para 50 para a versão final.
TOTAL_ENTREVISTADOS = 10

# Inicialização dos contadores conforme o enunciado
qtd_excelente = 0
qtd_bom = 0
qtd_ruim = 0

print("="*50)
print("SISTEMA DE PESQUISA DE SATISFAÇÃO - TUDOWEB")
print("="*50)

# Estrutura de repetição FOR para processar cada entrevistado
for i in range(1, TOTAL_ENTREVISTADOS + 1):
    # Simulação de dados (Nome e Idade variados)
    nome = f"Cliente_{i}"
    idade = random.randint(18, 65)
    
    # Gerando a opinião de forma aleatória entre 1 e 3
    # O random.choice garante uma distribuição equilibrada entre as opções
    opiniao = random.choice(['1', '2', '3'])
    
    # Estrutura de decisão para verificar e exibir a opinião
    desc_opiniao = ""
    if opiniao == '1':
        qtd_excelente += 1
        desc_opiniao = "1 - EXCELENTE"
    elif opiniao == '2':
        qtd_bom += 1
        desc_opiniao = "2 - BOM"
    elif opiniao == '3':
        qtd_ruim += 1
        desc_opiniao = "3 - RUIM"
    
    # Exibindo o retorno individual para validar a aleatoriedade
    print(f"Entrevistado {i:02d}: {nome} | Idade: {idade} | Resposta: {desc_opiniao}")

# Exibição dos resultados finais solicitados (Itens a e b)
print("\n" + "="*50)
print("RESUMO DA PESQUISA")
print("-" * 50)
print(f"a) Quantidade de respostas 'EXCELENTE': {qtd_excelente}")
print(f"b) Quantidade de respostas 'RUIM':      {qtd_ruim}")
print(f"   Quantidade de respostas 'BOM':       {qtd_bom}")
print("="*50)
