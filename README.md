# enzonascimentodeamorim_Ag8_DS_I
Código de pesquisa de usuários
import random

# Constante para testes
TOTAL_ENTREVISTADOS = 10

qtd_excelente = 0
qtd_bom = 0
qtd_ruim = 0

print(f"--- Simulando Pesquisa TudoWeb: {TOTAL_ENTREVISTADOS} Entrevistados ---")

for i in range(1, TOTAL_ENTREVISTADOS + 1):
    # Simulando a entrada de dados
    nome = f"Candidato {i}"
    idade = random.randint(18, 70)
    
    # Gera uma opinião aleatória entre 1, 2 e 3
    opiniao = str(random.randint(1, 3))
    
    # Mapeamento para exibição
    status = ""
    if opiniao == '1':
        qtd_excelente += 1
        status = "EXCELENTE"
    elif opiniao == '2':
        qtd_bom += 1
        status = "BOM"
    elif opiniao == '3':
        qtd_ruim += 1
        status = "RUIM"

    # Exibe o que foi "coletado" para conferência
    print(f"Entrevistado: {nome} | Idade: {idade} | Opinião: {status}")

print("\n" + "="*30)
print("      RESULTADO FINAL")
print("="*30)
print(f"EXCELENTE: {qtd_excelente}")
print(f"RUIM:      {qtd_ruim}")
print(f"BOM:       {qtd_bom}")
print("="*30)
