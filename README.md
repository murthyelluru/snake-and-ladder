# snake-and-ladder
code for snake and ladder game
public class HelloWorld{

     public static void main(String []args){
        int count=0;
        int count1=0;
        boolean value=true;
        int i=0;
        while(value)
        {
            if(count==100 || count1==100)
            {
                System.out.println("game finished");
                break;
            }
            else
            {
                if(i % 2 == 0)
                {
                    System.out.println("users turn");
                    int a=(int) (Math.random()*(6 - 1)) + 1;
                    count=count+a;
                    int c=usersturn(count);
                    if(c!=0)
                        count=c;
                    if(count>100)
                        count=count-a;
                    System.out.println("user:"+count);
                    
                }
                else if(i % 2 != 0)
                {
                    System.out.println("computers turn");
                    int a=(int) (Math.random()*(6 - 1)) + 1;
                    count1=count1+a;
                    int c=usersturn(count);
                    if(c!=0)
                        count1=c;
                    if(count1 > 100)
                        count1=count1-a;
                    System.out.println("computer:"+count1);
                
                }
            }
            i++;
        }
     }
    static int usersturn(int r)
     {
         if(r==28)
            return 6;
        if(r==45)
            return 15;
        if(r==65)
            return 40;
        if(r==9)
            return 40;
        if(r==67)
            return 92;
        return 0;
     }
     static int compturn(int r)
     {
         if(r==28)
            return 6;
        if(r==45)
            return 15;
        if(r==65)
            return 40;
        if(r==9)
            return 40;
        if(r==67)
            return 92;
        return 0;
     }
     
}
