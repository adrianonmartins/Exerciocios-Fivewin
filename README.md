#Include"Fivewin.ch"
//
Function main()
//   
	Exercicio42()
//
return nil  
//
Function Exercicio41()
//
local nNumero1  
nNumero1:= 0.00
//
//
msgget("Exercicio 04.1","Informe o numero",@nNumero1,)
//
MsgInfo(STR((nNumero1*nNumero1),10,2),"Resultado do Numero ao Quadrado")
MsgInfo(nNumero1^2,"Resultado do Numero ao Quadrado")
MsgInfo(SQRT(nNumero1),"Raiz Quadrada")
MsgInfo(STR(Int(nNumero1),10,2),"Parte Inteira do Numero")
MsgInfo(Mod(nNumero1),"Parte Fracionaria")
//
Return nil 
//
//
Function Exercicio42()
//
Local kmInicial           
Local kmFinal          
Local qtdLtGasto         
Local precoLtCombt          
Local cptanque
Local kmPorLitro
Local custoViagem
//
kmInicial:= 0.00          
kmFinal:= 0.00          
qtdLtGasto:= 0.00          
precoLtCombt:= 0.00          
cptanque:= 0.00
//
//
MsgGet("Exercicio 4.2","Informe o KM INICIAL",@kmInicial)          
MsgGet("Exercicio 4.2","Informe o KM FINAL",@kmFinal)          
MsgGet("Exercicio 4.2","Informe o QUANTIDADE DE LITROS GASTOS",@qtdLtGasto)          
MsgGet("Exercicio 4.2","Informe o PREÇO DO COMBUSTIVEL",@precoLtCombt)          
MsgGet("Exercicio 4.2","Informe a CAPACIDADE DO TANQUE",@cptanque)
//
//
MsgInfo(STR((kmFinal-kmInicial),10,2),"A quilometragem rodada foi:")          
MsgInfo(STR(((kmFinal-kmInicial)/qtdLtGasto),10,2),"Km por Litro:")
//
kmPorLitro:= (kmFinal-kmInicial)/qtdLtGasto
atVeiculo :=  kmPorLitro*cptanque
MsgInfo(STR((atVeiculo),10,2),"Autonomia do veículo:")
//
custoViagem:= precoLtCombt*((kmFinal-kmInicial)/kmPorLitro)
MsgInfo(STR((custoViagem),10,2),"Custo da viagem:")
//
