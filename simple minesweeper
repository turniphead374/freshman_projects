#include <stdio.h>
#include <stdlib.h>

#define EMPTY 0
#define KING 1
#define TRAP 2
#define THRONE 3

void kingsCrossing(int roads[6][6], int kingX, int kingY){
   printf("\a");
   printf("\n");

   for(int i=0;i<6;i++){
    printf("|---");
}
printf("|\n");

for(int i=0;i<6;i++){
    for(int j=0;j<6;j++){
       printf("| ");
        if(i==kingX&&j==kingY){
           printf("K ");
        }
        else if(roads[i][j]==TRAP){
            printf("  ");
        }
        else if(roads[i][j]==THRONE){
            printf("T ");
        }
        else{
            printf("  ");
        }
    }
    printf("|\n");

    for(int i=0;i<6;i++){
        printf("|---");
    }
    printf("|\n");

}

}

int main(){

  printf("Minesweeper 2: Throne adventure.");

  int roads[6][6]={
  {EMPTY, EMPTY, EMPTY, TRAP, EMPTY, TRAP},
  {EMPTY, TRAP, EMPTY, EMPTY, EMPTY, EMPTY},
  {EMPTY, EMPTY, TRAP, EMPTY, TRAP, EMPTY},
  {EMPTY, TRAP, EMPTY, EMPTY, EMPTY, EMPTY},
  {EMPTY, EMPTY, EMPTY, TRAP, TRAP, EMPTY},
  {EMPTY, TRAP, EMPTY, EMPTY, TRAP, THRONE},
  };

  int x=0, y=0;
  char move;

  while(1){
    kingsCrossing(roads, x, y);

    printf("\nMove(up/down/left/right): ");
    scanf(" %c", &move);

    int newX=x, newY=y;

    if(move=='u'){
        newX--;
    }else if(move=='d'){
        newX++;
    }else if(move=='l'){
        newY--;
    }else if(move=='r'){
        newY++;
    }

    if(newX<0||newX>5||newY<0||newY>5){
        printf("Invalid move. Try again.");
        continue;
    }

    if(roads[newX][newY]==TRAP){
        printf("\nYou have been trapped. The king has been usurped.");
        break;
    }
    if(roads[newX][newY]==THRONE){
        printf("\nYou've reached the throne! God save the King!");
        break;
    }

    x=newX;
    y=newY;

    }

    getch();

    return 0;
  }

