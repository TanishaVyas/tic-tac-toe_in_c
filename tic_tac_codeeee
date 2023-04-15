#include <stdio.h>
#include <conio.h>
/* 
screen
x and o
coordinates
*/
char board[3][3];
const char playerA = 'X';
const char playerB = 'O';

void resetboard();
void printboard();
void player_A();
void player_B();
int Checkboard();
char result();
void announce(char winner);

void main(){
    //int choice;
    //printf("--------------MENU--------------");
    //printf("\n Start with:\n1. X\n2. O");
    //printf("\nEnter your choice:");
    //scanf("%d",&choice);
    char winner=' ';
    printf("\n Trial board:");
    printf("\n 1 | 2 | 3 ");
    printf("\n-----------");
    printf("\n 4 | 5 | 6 ");
    printf("\n-----------");
    printf("\n 7 | 8 | 9 ");
    printf("\n");
    printf("\n");
    printf("\n");
    resetboard();
    
    while(winner = ' ' && Checkboard()!=0){
        printboard();
        player_A();
        winner=result();
        printboard();
        if(winner != ' ' && Checkboard()==0){
            break;
        }
        player_B();
        winner=result();
        printboard();
        if(winner != ' ' && Checkboard()==0){
            break;
        }
    }
    
    
    
    announce(winner);
    // announce winner
}

void resetboard(){
    for (int i=0;i<3;i++){
        for(int j=0;j<3;j++){
            board[i][j] = ' ';
        }
    }
}
void printboard(){
    printf("\n");
    printf("\n");
    printf("\n %c | %c | %c ",board[0][0],board[0][1],board[0][2]);
    printf("\n-----------");
    printf("\n %c | %c | %c ",board[1][0],board[1][1],board[1][2]);
    printf("\n-----------");
    printf("\n %c | %c | %c ",board[2][0],board[2][1],board[2][2]);
}
void player_A(){
    int x,y;
    int place;
    do{
    printf("Enter place number(player A) :");
    scanf("%d",&place);
    if (place==1){
        x=0,y=0;
    }
    else if(place==2){
        x=0,y=1;
    }
    else if(place==3){
        x=0,y=2;
    }
    else if(place==4){
        x=1,y=0;
    }
    else if(place==5){
        x=1,y=1;
    }
    else if(place==6){
        x=1,y=2;
    }
    else if(place==7){
        x=2,y=0;
    }
    else if(place==8){
        x=2,y=1;
    }
    else if(place==9){
        x=2,y=2;
    }
    else{
        printf("\n Invalid Response");
    }
    
    if(board[x][y]==' '){
        board[x][y]=playerA;
        break;
    }
    else{
        printf("\n Invalid Response");
    }
    }while(board[x][y]!=' ');
 
}
void player_B(){
    int x,y;
    int place;
    do{
    printf("Enter place number(player B) :");
    scanf("%d",&place);
    if (place==1){
        x=0,y=0;
    }
    else if(place==2){
        x=0,y=1;
    }
    else if(place==3){
        x=0,y=2;
    }
    else if(place==4){
        x=1,y=0;
    }
    else if(place==5){
        x=1,y=1;
    }
    else if(place==6){
        x=1,y=2;
    }
    else if(place==7){
        x=2,y=0;
    }
    else if(place==8){
        x=2,y=1;
    }
    else if(place==9){
        x=2,y=2;
    }
    else{
        printf(" \n Invalid Response");
    }
    
    if(board[x][y]==' '){
        board[x][y]=playerB;
        break;
    }
    else{
        printf("\n Invalid Response");
    }
    }while(board[x][y]==' ');
}
int Checkboard(){
    char empty_space=9;
    for(int i=0;i<3;i++){
        for (int j=0;j<3;j++){
            if(board[i][j]!=' '){
                empty_space--;
            }
        }
    }
 
        return empty_space;
    
}
char result(){
    if (Checkboard()==0){
    //rows
    for (int i=0;i<3;i++){
        if(board[i][0]==board[i][1] && board[i][0]==board[i][2]){
            return board[i][0];
        }
    }
    // columns
    for (int i=0;i<3;i++){
        if(board[0][i]==board[1][i] && board[0][i]==board[2][i]){
            return board[0][i];
        }
    }
    //diagonal
    if (board[0][0]==board[1][1] && board[0][0]==board[2][2]){
        return board[0][0];
    }
    if (board[0][2]==board[1][1] && board[0][2]==board[2][0]){
        return board[1][1];
    }
    }
}
void announce(char winner){
   if(winner == playerA)
   {
      printf(" \n Winner: PLAYER A");
   }
   else if(winner == playerB)
   {
      printf(" \n Winner: PLAYER B");
   }
   else{
      printf("IT'S A TIE!");
   }
}
