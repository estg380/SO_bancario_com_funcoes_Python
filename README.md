# SO_bancario_com_funcoes_Python
Sistema bancário basico com funções Python


print("BANCO TEM!")
# Nome do banco
print(" ")

#variaveis de identificação
usuario  = " "
senha = " "
inicio  = " "
nome = " "
id = " "
key = " "


def idetificação():
    while True:
        
        inicio  = str(input("Seja bem vinda ao Banco Tem! você ja possui conta? [S/N]:")).upper()

        if inicio == "N":
            nome = str(input("\nVamos cadastrar a sua conta! Por favor digite o seu nome: "))
            usuario = str(input(f"Olá {nome} Por favor escolha o sue nome de usuário: "))
            senha = str(input("Agora escolha  sua senha: "))
            print("USUARIO CADASTRADO!")
            print(" ")
            
            print("Voltando ao inicio!")
            

        if inicio == "S":
            id = str(input("Digite seu usuario: "))
            key = str(input("Digite sua senha: "))
            
            if id  != usuario:
                print(" ")
            if key != senha:
                print("ACESSO NEGADO! USUÁRIO OU SENHA INVÁLIDOS")
               
            if id  == usuario:
                print(" ")
            if key == senha:
                print("ACESSO PERMITIDO")
                print (f"\nSEJA BEM VINDO {nome}! ")
                break



#variaveis de operação
saldo = 500
deposito = 0
saque = 0
extrato = " "
limite_saque = 3
soma = 0
                                
def operação ():       
      while True:
          menu= int(input("DEPOSITO[1]\nSAQUE   [2]\nEXTRATO [3]\n\nEscolha uma das opçoes acima: "))
                          
          if menu == 1:
               deposito = int(input ("Por favor, Digite o valor do seu depósito: "))
               print (f"\nO seu novo saldo é de:  {deposito + saldo}")
         
          if  menu == 2:
               saque = int(input("Digite o valor do seu saque: "))
               print (f"\nVocê sacou o valor de  {saque}, seu novo saldo é de : {saldo + deposito - saque} ")
               
          if  menu == 3:
               print(f"\nSEGUE SEU EXTRATO :\nValor deposito {deposito}\nValores de saque: {saque}\nSeu saldo é de: {saldo + deposito - saque} ")
          
          continuar_parar = str(input("\nDESEJA CONTINUAR? [S/N]: ")).upper()
          if continuar_parar != "S":
               print ("\nObrigado por usar nossos serviços tenha um bom dia!")
               soma += 1
               break
     
                    

idetificação()
operação ()
