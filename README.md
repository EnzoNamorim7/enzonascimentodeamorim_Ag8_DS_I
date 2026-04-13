# Pesquisa de Satisfação - TudoWeb

# Constante para facilitar os testes 
TOTAL_ENTREVISTADOS = 10

# Inicialização dos contadores
qtd_excelente = 0
qtd_bom = 0
qtd_ruim = 0

print("--- Início da Pesquisa de Satisfação: TudoWeb ---")

for i in range(1, TOTAL_ENTREVISTADOS + 1):
    print(f"\nEntrevistado nº {i}")
    
    # Coleta de dados básicos
    nome = input("Digite o nome: ")
    idade = input("Digite a idade: ")
    
    # Coleta e validação da opinião
    print("Opinião sobre o atendimento:")
    print("1: EXCELENTE | 2: BOM | 3: RUIM")
    opiniao = input("Sua resposta: ")

    # Estrutura de decisão para contabilizar os votos
    if opiniao == '1':
        qtd_excelente += 1
    elif opiniao == '2':
        qtd_bom += 1
    elif opiniao == '3':
        qtd_ruim += 1
    else:
        print("Opção inválida! Este voto não será contabilizado.")

# Exibição dos resultados finais
print("\n" + "="*30)
print("      RESULTADO DA PESQUISA")
print("="*30)
print(f"Quantidade de respostas EXCELENTE: {qtd_excelente}")
print(f"Quantidade de respostas RUIM:      {qtd_ruim}")
print(f"Total de participantes:            {TOTAL_ENTREVISTADOS}")
print("="*30)
