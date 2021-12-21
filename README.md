#include <stdio.h>
#include <stdlib.h>
#include <locale.h>
#include <string>
#include <iostream>
#include <math.h>
#include <iomanip>

using namespace std;





int main(){
	
	
	setlocale (LC_ALL, "portuguese");
	cout << fixed << setprecision (2);
	
	
	
	float i, j;
	int cont = 1, a, aux, aux2, mes;
	cout << "\n";
	
	cout << "\nRegras: \n\n" << "Não está descontando imposto de renda nem IOF dos calculos.\n\n" << "O valor máximo de base é de ate 7000 reais.\n\n";
	cout << "O programa ira iniciar agora!\n\n";
	
	system ("pause");
	inicio:
	system ("cls");
	
		cout << "========================= Taxa Selic atual para cálculo 9,25% ao ano ========================= \n\n";
	
	
		
	cout << "Digite um valor inicial em reais para começar a investir (use ponto no lugar de virgula): \n\n";
	cin >> a;
	
	cout << "Por quanto tempo quer poupar? (use número de mêses como referência) \n\n";
	cin >> mes;
	
	cout << "\nQuanto pretende colocar de valor fixo todo mês? \n\n";
	cin >> aux;
	
		 
				
	cout << "\n";
	
	/* A formula está calculando o valor investido  "a" com jurus ao longo de 1 mês (aproximadamente 30 dias)
	 e está subindo a quantidade de mês digitado pelo usuário de 1 ao tempo de investimento digitado pelo usuário "mes"*/
	
	for (aux2 = 0; aux2 < 10000; aux2 = aux2 + aux){
		
		if (cont <= mes){
				i = (a +aux2) *pow (1.007625, cont) ;
				cout << "Ao fim do " << cont << "° mês: " <<i << "\n";
		cont ++;
		}
		
		
	}
		
	char letra;	
	cout << "\n\nDeseja digitar outros Valores para comparação? [ s / n ]";
	cin >> letra;
	if (letra == 's' or letra == 'S'){
		goto inicio;
	}else {
		cout << "\nO programa será encerrado!!\n\n";
	}
	
	
	
	
	cout << "\n";
	
	
	
	
	
	
	system ("PAUSE");
	
	return 0;
	
	
}