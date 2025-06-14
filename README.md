lista_compras = []
quantidade = []

while True:
    print('\n1 Adiconar item \n2 Remover item \n3 Ver lista \n4 Sair\n' )
    pergunta = input('Digite um número correspondente a ação que deseja fazer')
    if pergunta == '1':
        add = input('Nome do item que deseja adicionar:').capitalize()
        qtde = int(input('Digite a quantidade:'))
        lista_compras.append(add)
        quantidade.append(qtde)
        print('Item adicionado!')

    elif pergunta == '2':
        remover = input('Digite o nome do item que deseja remover').capitalize()
        if remover in lista_compras:
            i = lista_compras.index(remover)
            quantidade.remove(quantidade[i])
            lista_compras.remove(remover)
            print('Item removido')
        else:
            print(f'O item {remover} não está na lista')

    elif pergunta == '3':
        dicionario = dict(zip(lista_compras, quantidade))
        print(dicionario)

    elif pergunta =='4':
        print('Encerrando programa...')
        break
    else:
        print('Opção inválida! digite apenas números.')

        


