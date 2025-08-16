# Projetos

[Meu_bot.py](https://github.com/user-attachments/files/21813653/Meu_bot.py)
 

[Cursos.py](https://github.com/user-attachments/files/21813670/Cursos.py)CURSOS_INFO = {
    1: "--- ADMINISTRAÇÃO ---\nO curso de Administração prepara você para...",
    2: "--- ANÁLISES CLÍNICAS ---\nO curso de Análises Clínicas envolve ...",
    3: "--- EDIFICAÇÕES ---\nO curso de Edificações qualifica você para ...",
    4: "--- ELETRÔNICA ---\nO curso de Eletrônica foca no projeto, montagem e manutenção de sistemas eletrônicos. Você aprenderá sobre circuitos, microcontroladores, telecomunicações e automação.",
    5: "--- ELETROTÉCNICA ---\nO curso de Eletrotécnica prepara você para trabalhar com sistemas elétricos de potência, instalação e manutenção de equipamentos elétricos. Inclui estudos sobre máquinas elétricas, segurança do trabalho e energias renováveis.",
    6: "--- ENFERMAGEM ---\nO curso de Enfermagem capacita profissionais para cuidar da saúde de indivíduos e comunidades, prestando assistência em diversas áreas. Aborda temas como primeiros socorros, anatomia, fisiologia e saúde pública.",
    7: "--- INFORMÁTICA ---\nO curso de Informática desenvolve habilidades em programação, desenvolvimento de sistemas, redes de computadores e manutenção de software e hardware. Você aprenderá linguagens de programação, banco de dados e lógica de programação.",
    8: "--- MECÂNICA ---\nO curso de Mecânica forma profissionais para atuar na fabricação, instalação e manutenção de máquinas e equipamentos. Estuda elementos de máquinas, processos de fabricação, automação industrial e robótica.",
    9: "--- MEIO AMBIENTE ---\nO curso de Meio Ambiente prepara você para identificar e propor soluções para problemas ambientais, gerenciando recursos naturais e promovendo a sustentabilidade. Abrange ecologia, legislação ambiental e gestão de resíduos.",
    10:"--- METALURGIA ---\nO curso de Metalurgia foca nos processos de extração, produção e transformação de metais. Você estudará propriedades dos materiais, processos siderúrgicos e metalografia.",
    11:"--- QUÍMICA ---\nO curso de Química qualifica para trabalhar em laboratórios, indústrias e pesquisa, aplicando conhecimentos de processos químicos. Inclui química orgânica, inorgânica, analítica e físico-química."
}

sair=1
while sair != 0:
      
    sair=int(input( " 1 - MATRICULA\n" \
                    " 2 - CONHEÇA NOSSOS CURSOS\n" \
                    " 3 - INFORMAÇÕES\n"\
                    " 0 - ENCERRAR\n"))
    if sair == 0:
        print (" \nAté mais! ")
    
    elif sair == 1:
         print( "\nPor aqui você tem acesso ao processo de matrícula," \
                " onde você receberá um arquivo em PDF." \
                " Que deverá ser entregue preenchido a caneta azul ou preta" \
                " até a data prevista em edital no endereço da instituição.")
    
         while True:
             op1=input("DESEJA RECEBER O PROCESSO DE MATRICULA S/N ?")
             if op1 == 'S':
                 print("ARQUIVO PDF (Imagine que o PDF foi enviado aqui)\n")
                 break
             elif op1 == 'N':
                 print(" Ok, voltando aõ menu principal!")
                 break
             else:
                 print("Comando inválido.  Por favor, digite 'S' para Sim ou 'N' para Não.")                     
    elif sair == 2:
        from Cursos import CURSOS_INFO
        continuarexe = True
        while continuarexe:
            try:
             opcao=int(input("\n1 - ADMINISTRAÇÃO\n"
                            "2 - ANÁLISES CLÍNICAS\n"
                            "3 - EDIFICAÇÕES\n" 
                            "4 - ELETRÔNICA\n" 
                            "5 - ELETROTÉCNICA\n"
                            "6 - ENFERMAGEM\n"
                            "7 - INFORMÁTICA\n"
                            "8 - MECÂNICA\n"
                            "9 - MEIO AMBIENTE\n"
                           "10 - METALURGIA\n"
                           "11 - QUÍMICA\n" 
                           "0 - VOLTAR AO MENU PRINCIPAL\n"
                           "Digite o número do curso para mais informações ou 0 para voltar:\n "))
            except ValueError:
               print(" Por favor digite um número Válido para as opçoes dos cursos.")
               continue
            if opcao == 0:
                break         
            elif opcao in CURSOS_INFO:           
                print(CURSOS_INFO[opcao])
                escolha_pos_curso = 1
                while escolha_pos_curso != 0:
                 try:
                    escolha_pos_curso=int(input(" 1- Ver outros Cursos\n" \
                                                " 0- Voltar ao menu principal\n"))
                    if escolha_pos_curso == 1:
                        break
                    elif escolha_pos_curso == 0:
                        continuarexe = False
                    else:
                     print("Opção inválida. Digite 1 para ver outros cursos ou 0 para sair")
                 except ValueError:
                        print("Por favor, escolha uma das opções válidas. 0 ou 1")
                        
        # eu consigo fazer com que o usuario escolha sair do primeiro loop
