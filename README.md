# CV6

// CV6.cpp: Definuje vstupní bod pro aplikaci.
//

#include "CV6.h"
using namespace std;

//int numAlpha(char* t);


//int numLogost(char* t);



int numAlpha( char *text)
{
	int i = 0;

	for (int a = 0; text[a] != '\0'; a++)
	{
		if (isalpha(text[a])) 
		{
			i++;
		}
	}
	return i;
}


int numNum( char* text) 
{
	int pocet = 0;
	for (int b = 0; text[b] != '\0'; b++)
	{
		if (isdigit(text[b])) 
		{
			pocet++;
		}
	
	}
	return pocet;
}

int numLongost(char* text) {

	int maxLen = 0;
	int currentLen = 0;
	for (int c = 0; text[c] != '\0'; c++) {

		if (isalnum(text[c]))
		{
			currentLen++;
		}
		else 
		{
			
		if (currentLen > maxLen) {
			maxLen = currentLen;
		}
			currentLen = 0;
		}
	}
		if (currentLen > maxLen) 
		{
		maxLen = currentLen;
		}
	
	
	return maxLen;
}

int main()
{
	
	char text[] = "Toto jsou 2 vzorkove vety, ktere budou zpracovavany Vasemi funkcemi. Auto Hyunday ix35 ma pres 120 konskych sil";

	printf("Pocet pismen: %d\n", numAlpha(text));
	printf("Pocet cisel: %d\n", numNum(text));
	printf("Nejdelsi slovo ma %d znaku \n!", numLongost(text));

	return 0;





}

