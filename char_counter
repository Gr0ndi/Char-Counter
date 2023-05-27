#include <stdio.h>
#include <stdlib.h>
#include <string.h>
int main(int argc, char *argv[]){
  
  if (argc != 2){
    printf("you can only supply 1 argument - filename\n");
    return -1;
  }

  printf("the first argument is %s\n", argv[1]);
  char* FNAMESTR;
  FNAMESTR = malloc(strlen(argv[1]));
  if(FNAMESTR != NULL) {
    strcpy(FNAMESTR, argv[1]);
  }


  FILE * pFile;
  pFile = fopen(FNAMESTR,"r");
  
  if(pFile == NULL){
    printf("file couldn't be opened!\n");
    return 1;
  }

  char ch;
  int count = 0;
  while ((ch = fgetc(pFile)) != EOF){
    if(ch == 'a' || ch == 'A') {
      count++;
    }
  }
  free(FNAMESTR);
  printf("the file containts %d 'a' chars.\n", count);
  fclose(pFile);

}
