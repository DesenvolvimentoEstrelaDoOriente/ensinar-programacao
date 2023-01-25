# Exercício Catrada de Metrô


## Nível 1 - Passagem pela catraca

Cenários:  
- Dado que a catraca está fechada  
    Quando o passageiro tenta passar por ela  
    Então a catraca deve bloquear o passageiro

- Dado que a catraca está aberta  
    Quando o passageiro passa por ela  
    Então a catraca deve ir para o modo Fechada


## Nível 2 - Ticket de metrô

Cenários:  
Deve atender a todos os cenários do Nível 1, e mais estes:  

- Dado a catraca está fechada    
    Quando e o bilhete do metro é inserido  
    Então ela deve mudar para o modo Aberta

- Dado que a catraca está em modo Aberta  
    Quando o bilhete do metro é inserido  
    Então ela deve continuar em modo Aberto  
    E o bilhete deve ser retornado 

## Nível 3 - Bilhete Único

Agora, além de entrar no metrô usando um ticket, o passageiro pode acessar usando um bilhete único contendo um valor de saldo nele.
Ao passar o bilhete, o valor da passagem será debitado do saldo total do bilhete e a catraca será liberada.
Cenários:  
Deve atender a todos os cenários do Nível 2, e mais estes:
- Dado que a catraca está fechada  
    Quando o bilhete único é usado  
    E o bilhete contém saldo suficiente  
    Então o valor da passagem é debitado do saldo  
    E a catraca é aberta  

- Dado que a catraca está fechada  
    Quando o bilhete único é usado  
    E o bilhete não contém saldo suficiente  
    Então passageiro recebe uma mensagem "Saldo Insuficiente"  
    E a catraca permanece fechada  

Ideias: valor da tarifa proporcional a distancia viajada (estilo Washinton), com cartão e com bilhetes; Taxas diferentes dependendo do horário de funcionamento.