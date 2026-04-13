import random

# Configuração do teste
TOTAL_ENTREVISTADOS = 10

# Criamos uma lista com 10 opiniões para garantir a variedade no resultado final
# Aqui definimos exatamente quantos de cada tipo queremos para o teste
opinioes_predefinidas = ['1', '1', '1', '1', '2', '2', '2', '3', '3', '3']

# Embaralhamos a lista para que a ordem mude a cada execução
random.shuffle(opinioes_predefinidas)

# Inicialização dos contadores
qtd_excelente = 0
qtd_bom = 0
qtd_ruim = 0

print("="*60)
print("SISTEMA DE PESQUISA TUDOWEB - VALIDAÇÃO DE DADOS")
print("="*60)

# O loop FOR percorre a lista de opiniões variadas
for i in range(TOTAL_ENTREVISTADOS):
    nome = f"Cliente_{i+1:02d}"
    idade = random.randint(20, 50)
    
    # Pegamos a opinião da nossa lista embaralhada
    opiniao = opinioes_predefinidas[i]
    
    # Estrutura de decisão para contagem e exibição
    status = ""
    if opiniao == '1':
        qtd_excelente += 1
        status = "1 - EXCELENTE"
    elif opiniao == '2':
        qtd_bom += 1
        status = "2 - BOM"
    elif opiniao == '3':
        qtd_ruim += 1
        status = "3 - RUIM"
    
    print(f"Entrevistado: {nome} | Idade: {idade} | Resposta: {status}")

# Exibição da soma total conforme solicitado
print("\n" + "="*60)
print("SOMA TOTAL DAS RESPOSTAS")
print("-" * 60)
print(f"a) Quantidade de respostas 'EXCELENTE': {qtd_excelente}")
print(f"b) Quantidade de respostas 'RUIM':      {qtd_ruim}")
print(f"   Quantidade de respostas 'BOM':       {qtd_bom}")
print("-" * 60)
print(f"TOTAL DE ENTREVISTADOS PROCESSADOS: {qtd_excelente + qtd_bom + qtd_ruim}")
print("="*60)
