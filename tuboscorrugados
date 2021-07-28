#include <stdio.h>

//Dimensões das embalagens 1,2,3,4 e 5 (em mm)
int x_pack[] = {500, 600,  700, 800, 900};
int y_pack[] = {500, 600,  700, 800, 900};
int z_pack[] = {2000, 3000, 4000, 5000, 6000};

//Dimensões do tubo (em mm)
int d_conduit = 20;
int z_conduit = 1000;    

//Escolha da embalagem
void main(){
int z_emb = 0;
int idx = 0;
int qty = 0;

if(z_conduit < z_pack[0]){
  z_emb = z_pack[0];
  idx = 0;
}
else{
  for(int i = 1; i <= sizeof(z_pack); i++){
    if(z_conduit < z_pack[i]){
      if(z_pack[i-1] < z_conduit){
        z_emb = z_pack[i];
        idx = i;
        break;
      }
    }
  }
}
qty = x_pack[idx]/d_conduit + y_pack[idx]/d_conduit;
printf("Será usada a embalagem %d e nela conterá %d tubos. \n", idx, qty);
}

