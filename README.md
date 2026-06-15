# projeto2026_SCM
projeto de  software 2026

# Sistema simples para gerenciamento de tarefas
# Não consegui abrir Git  Bush e nem salvar pelo vscode

tarefas = []

def adicionar_tarefa():
    tarefa = input("Digite a tarefa: ")
    tarefas.append(tarefa)
    print("Tarefa adicionada com sucesso!")

def listar_tarefas():
    if len(tarefas) == 0:
        print("Nenhuma tarefa cadastrada.")
    else:
        print("\nLista de Tarefas:")
        for i, tarefa in enumerate(tarefas, start=1):
            print(f"{i}. {tarefa}")

def remover_tarefa():
    listar_tarefas()

    if len(tarefas) > 0:
        try:
            indice = int(input("Digite o número da tarefa que deseja remover: "))
            removida = tarefas.pop(indice - 1)
            print(f"Tarefa '{removida}' removida com sucesso!")
        except:
            print("Opção inválida.")

def menu():
    while True:
        print("\n=== GERENCIADOR DE TAREFAS ===")
        print("1 - Adicionar tarefa")
        print("2 - Listar tarefas")
        print("3 - Remover tarefa")
        print("4 - Sair")

        opcao = input("Escolha uma opção: ")

        if opcao == "1":
            adicionar_tarefa()
        elif opcao == "2":
            listar_tarefas()
        elif opcao == "3":
            remover_tarefa()
        elif opcao == "4":
            print("Encerrando o sistema...")
            break
        else:
            print("Opção inválida.")

menu()

