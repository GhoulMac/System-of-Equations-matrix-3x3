package DA1;
import java .util.*;
/**
 *
 * @author Aditya
 */
public class DA1app6 {


    public static void main(String args[]){
        int i, j, k;
    float det = 0;
    float mat[][] = new float[3][3];
    float invmat[][] = new float[3][3];
    Scanner sc = new Scanner(System.in);
    System.out.println("Enter elements of matrix row wise:");
    for(i = 0; i < 3; ++i)
    for(j = 0; j < 3; ++j)
    mat[i][j] = sc.nextFloat();
        for(i = 0; i < 3; i++)
            det = det + (mat[0][i] * (mat[1][(i+1)%3] * mat[2][(i+2)%3] - mat[1][(i+2)%3] * mat[2][(i+1)%3]));
    System.out.println("\ndeterminant = " + det);
    for(i = 0; i < 3; ++i) {
    for(j = 0; j < 3; ++j)
        invmat[i][j]=(((mat[(j+1)%3][(i+1)%3] * mat[(j+2)%3][(i+2)%3]) - (mat[(j+1)%3][(i+2)%3] * mat[(j+2)%3][(i+1)%3]))/ det);
        }
    float[] c = new float[3];
    for(i=0;i<3;i++){
        c[i]=sc.nextFloat();
    }
    float[] sum= new float[3];
        for ( i= 0 ; i < 3 ; i++ )

        for ( j= 0 ; j <3;j++)
        {
        for ( k= 0 ; k <3;k++ )
            {
            sum[i] +=invmat[i][k]*c[k] ;

            }
            }
    for(i=0;i<3;i++){
        System.out.println(sum[i]/3);
    }
    }
}
