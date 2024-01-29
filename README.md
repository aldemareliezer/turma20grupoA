Código inicial retirado to chat Discord, autoria de Luciana Paiva:


import random

def bem_vindo():
    print("Bem-vindo! Prepare-se para testar seus conhecimentos sobre programação. Boa Sorte")
    num_jogadores = int(input("Digite o número de jogadores (até 4): "))
    jogadores = [input(f"Digite o nome do Jogador {i+1}: ") for i in range(num_jogadores)]
    return jogadores

def criar_quizz():
    perguntas = [
        {"pergunta": "Qual é a linguagem de programação deste quizz?",
         "alternativas": {"A": "Java", "B": "C++", "C": "Python", "D": "Ruby"},
         "resposta_correta": "C"},
    ]

    perguntas += [
        {"pergunta": "Qual destes não é um tipo de dado em Python?",
         "alternativas": {"A": "String", "B": "Boolean", "C": "Float", "D": "Tudo é tipo de dado em Python"},
         "resposta_correta": "D"},

        {"pergunta": "O que é um algoritmo?",
     "alternativas": {"A": "Um tipo de linguagem de programação", "B": "Um conjunto de instruções para resolver um problema", "C": "Um bug no código", "D": "Uma variável em Python"},
     "resposta_correta": "B"},

        {"pergunta": "Qual é a diferença entre '==', 'is' e 'in' em Python?",
     "alternativas": {"A": "São todos operadores de comparação equivalentes", "B": "'==' compara valores, 'is' compara identidade de objetos, 'in' verifica a existência em sequências", "C": "São operadores de concatenação de strings", "D": "Não têm diferença"},
     "resposta_correta": "B"},
{"pergunta": "O que é a recursividade em programação?",
     "alternativas": {"A": "Um tipo de erro de compilação", "B": "Um conceito que envolve uma função chamando a si mesma", "C": "Um método de criptografia", "D": "Um loop infinito"},"resposta_correta": "B"},

       {"pergunta": "O que é um objeto em programação orientada a objetos?",
     "alternativas": {"A": "Uma função em Python", "B": "Uma variável global", "C": "Uma instância de uma classe que pode ter atributos e métodos", "D": "Um comentário no código"},
     "resposta_correta": "C"},

       {"pergunta": "Qual é o propósito do comando 'try...except' em Python?",
     "alternativas": {"A": "Criar loops", "B": "Manusear exceções e erros", "C": "Definir funções", "D": "Escrever comentários"},
     "resposta_correta": "B"},

       {"pergunta": "Qual é a função da tag <head> em um documento HTML?",
     "alternativas": {"A": "Definir o conteúdo principal", "B": "Inserir scripts e metadados", "C": "Criar uma tabela", "D": "Definir estilos de texto"},
     "resposta_correta": "B"},

       {"pergunta": "O que a sigla HTML5 representa?",
     "alternativas": {"A": "Hypertext Markup Language 5", "B": "High Tech Modern Language 5", "C": "Hyperlink and Text Markup Language 5", "D": "Hypertext and Table Markup Language 5"},
     "resposta_correta": "A"},

       {"pergunta": "Como você cria um link para uma página externa em HTML?",
     "alternativas": {"A": "<a href='external.html'>Link Externo</a>", "B": "<link external.html>", "C": "<a link='external.html'>Link Externo</a>", "D": "<a src='external.html'>Link Externo</a>"},
     "resposta_correta": "A"},
{"pergunta": "O que é uma tag de âncora (<a>) usada para?",
     "alternativas": {"A": "Inserir uma imagem", "B": "Criar uma lista", "C": "Definir um link", "D": "Comentar o código"},
     "resposta_correta": "C"},

     {"pergunta": "Qual é a função da tag <footer> em HTML?",
     "alternativas": {"A": "Criar uma barra lateral", "B": "Definir uma área de rodapé", "C": "Inserir uma tabela", "D": "Criar uma navegação"},
     "resposta_correta": "B"},

 
   {"pergunta": "Qual é a função da tag <div> em HTML?",
     "alternativas": {"A": "Definir uma tabela", "B": "Criar uma divisão ou seção", "C": "Inserir uma imagem", "D": "Definir um link"},
     "resposta_correta": "B"},

    {"pergunta": "Como você comenta um trecho de código HTML?",
     "alternativas": {"A": "<!-- Comentário -->", "B": "<comment>Comentário</comment>", "C": "<commentar>Comentário</commentar>", "D": "# Comentário"},
     "resposta_correta": "A"},

    {"pergunta": "Qual é a tag utilizada para inserir uma imagem em HTML?",
     "alternativas": {"A": "<img>", "B": "<picture>", "C": "<image>", "D": "<src>"},
     "resposta_correta": "A"},

    {"pergunta": "O que significa a sigla CSS em relação a HTML?",
     "alternativas": {"A": "Computer Style Sheets", "B": "Cascading Style Sheets", "C": "Content Style Sheets", "D": "Creative Style Sheets"},
     "resposta_correta": "B"},

    {"pergunta": "Qual é a tag correta para criar uma lista ordenada em HTML?",
     "alternativas": {"A": "<ol>", "B": "<ul>", "C": "<li>", "D": "<list>"},
     "resposta_correta": "A"},

    {"pergunta": "Qual é a tag utilizada para criar um link em HTML?",
     "alternativas": {"A": "<link>", "B": "<a>", "C": "<href>", "D": "<url>"},
     "resposta_correta": "B"},

    {"pergunta": "Como você define o título de uma página HTML?",
     "alternativas": {"A": "<title>", "B": "<header>", "C": "<h1>", "D": "<head>"},
     "resposta_correta": "A"},
{"pergunta": "Qual tag é usada para criar uma lista não ordenada em HTML?",
     "alternativas": {"A": "<ol>", "B": "<ul>", "C": "<li>", "D": "<list>"},
     "resposta_correta": "B"},

    {"pergunta": "Em HTML, como você insere uma quebra de linha?",
     "alternativas": {"A": "<break>", "B": "<br>", "C": "<lb>", "D": "<newline>"},
     "resposta_correta": "B"},

    {"pergunta": "Como você concatena duas strings em Python?",
     "alternativas": {"A": "strcat()", "B": "merge()", "C": "concat()", "D": "O operador '+'"},
     "resposta_correta": "D"},

    {"pergunta": "O que é um loop 'for'?",
     "alternativas": {"A": "Uma estrutura condicional", "B": "Um loop de repetição", "C": "Uma função matemática", "D": "Um operador lógico"},
     "resposta_correta": "B"},

    {"pergunta": "Qual é a principal função do comando 'if' em Python?",
     "alternativas": {"A": "Definir uma função", "B": "Iterar sobre uma lista", "C": "Executar um bloco de código condicionalmente", "D": "Declarar uma variável"},
     "resposta_correta": "C"},
     
     {"pergunta": "O que representa o operador '%' em Python?",
     "alternativas": {"A": "Multiplicação", "B": "Divisão", "C": "Módulo", "D": "Exponenciação"},
     "resposta_correta": "C"},

    {"pergunta": "O que é uma lista em Python?",
     "alternativas": {"A": "Um tipo de dado numérico", "B": "Um conjunto de caracteres", "C": "Uma estrutura de dados que armazena elementos ordenados", "D": "Uma função integrada"},
     "resposta_correta": "C"},

    ]

    random.shuffle(perguntas)
    return perguntas

def jogar_quizz(jogadores, perguntas):
    pontuacoes = {jogador: 0 for jogador in jogadores}

    for pergunta in perguntas:
        print("\n" + pergunta["pergunta"])
        for opcao, resposta in pergunta["alternativas"].items():
            print(f"{opcao}. {resposta}")

        resposta_jogadores = {}
        for jogador in jogadores:
            resposta_jogadores[jogador] = input(f"{jogador}, escolha a opção correta: ").upper()

        for jogador, resposta_jogador in resposta_jogadores.items():
            if resposta_jogador == pergunta["resposta_correta"]:
                pontuacoes[jogador] += 1

    print("\nJogo concluído! Pontuações finais:")
    for jogador, pontuacao in pontuacoes.items():
        print(f"{jogador}: {pontuacao} pontos")

def main():
    jogadores = bem_vindo()
    perguntas = criar_quizz()
    jogar_quizz(jogadores, perguntas)

if name == "main":
    main()



___________________________________________________________________________

Adicionado na penultima linha do codigo (correção Aldemar)


if __name__ == "__main__":

pois o mesmo não estava funcionando corretamente, o __ __ é uma maneira de verificar se o script está sendo executado diretamente como um programa independente (e não sendo importado como um módulo).
O que pode ter contecido é um erro no proprio chat pois o texto com as palavras main e name estão sublinhados na mensagen do discord.

___________________________________________________________________________________

Modificação Alexandre:


(Principal)
Fiz a condicional para caso seja adicionado mais de 4 jogadores ou menos de 1, seja recusado e o usuário precise consertar isso.

Segue a parte do código da qual estou mencionando.  

def bem_vindo():
    print("Bem-vindo! Prepare-se para testar seus conhecimentos sobre programação. Boa Sorte")
    num_jogadores = 0
    while num_jogadores <= 0 or num_jogadores > 4:
            num_jogadores = int(input("Digite o número de jogadores (até 4): ")) 
            if num_jogadores <= 0 or num_jogadores > 4:
                print("Por favor, insira um numero válido de jogadores (1 a 4)")
    jogadores = [input(f"'Digite o nome do Jogador {i+1}: ") for i in range(num_jogadores)]
    return jogadores

____________________________________________________________________________________

Modificação Aldemar. 

Adicionado no código para pedir apenas 5 perguntas


    perguntas = random.sample(quizz_completo, 5)

Explicação: O comando random seleciona as perguntas em modo aleatório enquanto o .sample é um copmplemento do comando random servindo como uma amostragem da seleção.

No caso substitui o (perguntas) do c;odigo original pelo (quizz_completo) aonde ele vai puxar todas as perguntas e fazer uma sele;cão aleatória das mesmas.


_____________________________________________________________________________________



    


