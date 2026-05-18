flowchart LR
    Cliente([Cliente])
    Vendedor([Vendedor])
    Admin([Administrador])

    subgraph Sistema_de_Vendas
        UC1((Realizar Login))
        UC2((Cadastrar Cliente))
        UC3((Consultar Produtos))
        UC4((Realizar Venda))
        UC5((Emitir Fatura))
        UC6((Gerenciar Estoque))
        UC7((Gerar Relatórios))
    end

    Cliente --> UC3
    Cliente --> UC4

    Vendedor --> UC1
    Vendedor --> UC2
    Vendedor --> UC3
    Vendedor --> UC4
    Vendedor --> UC5

    Admin --> UC1
    Admin --> UC6
    Admin --> UC7
