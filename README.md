Desafio 8 - Cadastro de Funcionários
O que o programa faz
Cadastra 5 funcionários pedindo nome e senha. A senha só é aceita quando atende todas as regras.
Como rodar
bashpython desafio8_cadastro_funcionarios.py
Regras da senha

mínimo 6 caracteres
máximo 12 caracteres
pelo menos 1 letra maiúscula
pelo menos 1 letra minúscula
pelo menos 1 número
senha e confirmação iguais

O que aparece na tela
=== CADASTRO DE FUNCIONARIOS ===

Funcionario 1 de 5 - Nome: João Silva
Senha: 6 a 12 caracteres, maiuscula, minuscula e numero
Senha: abc
Confirma: abc
erro: minimo 6 caracteres (digitou 3), falta maiuscula, falta numero

Senha: Joao123
Confirma: Joao123
ok! João Silva cadastrado em 2 tentativa(s)
O que acontece se errar a senha
ErroMensagemCampo vazioerro: senha vaziaMenos de 6 caractereserro: minimo 6 caracteres (digitou X)Mais de 12 caractereserro: maximo 12 caracteres (digitou X)Sem letra maiúsculaerro: falta maiusculaSem letra minúsculaerro: falta minusculaSem númeroerro: falta numeroConfirmação diferenteerro: senhas diferentes
Ao finalizar os 5 cadastros
todos cadastrados!

ENTER pra repetir ou S pra sair:

ENTER → começa um novo cadastro de 5 funcionários
S → encerra o programa

Estrutura do código

for → usado para percorrer os 5 funcionários (quantidade fixa e conhecida)
while → usado para validar a senha (não sabemos quantas tentativas o usuário vai precisar)
