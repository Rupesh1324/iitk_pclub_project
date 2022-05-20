#include <stdio.h>
#include <time.h>
  
int main()
{
    clock_t tim;
    tim = clock();
    int num_of_times=0;
    
    printf("program starts \n");
    
    while(!(tim==1000000))
    {
        num_of_times+=1;
        tim = clock() - tim;
    }
    
    double ti_me=((double)tim);
    double time_taken = ti_me/CLOCKS_PER_SEC; 
    
    printf("program excecutes %d time in %f seconds \n",num_of_times,time_taken);
     printf("program ends \n");
     
    return 0;
}
