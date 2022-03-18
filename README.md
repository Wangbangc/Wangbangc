头歌第一次
/*
 任务：使用while循环结合自增运算符获取控制台的一组输入（每组输入包含4个整数，其中有正有负，比如：22 33 -22 32），请求出每组输入的非负数之和
*/

import java.util.Scanner;

public class MyWhile {

    public static void main(String[] args) {
        // 定义变量sum，用于求非负数的和，并赋初值0。
        int sum=0;
        // 定义变量i，用于控制循环，并赋初值1。
        int i=1;
        // 定义Scanner对象
        Scanner input = new Scanner(System.in);
        // 请在 Begin-End 间编写代码

        /********** Begin **********/
        // 第一步：定义while循环，循环4次
        while(i<=4){
            int n  =input.nextInt();
            if(n>0){
            sum+=n;}
            i++;

        }
        System.out.print(sum);

        // 第二步：获取输入值

        // 第三步：判断输入值是否大于0，对大于0的值累加

        // 第四步：while循环中的变量加1

        // 第五步：打印sum值

        /********** End **********/

    }
}



/*
任务：接收输入值（整数数列），统计出等差数列的均值，每组输入以%结束，比如1 3 5 %。
其中百分号的作用是：在while循环中判断输入为%时，终止循环。

*/

import java.util.Scanner;

public class WhileTest {

    public static void main(String[] args) {
        // 定义变量sum，用于求等差数列的和
        int sum=0;
        // 定义变量z，记录等差数个数

        // 创建Scanner对象
        Scanner input = new Scanner(System.in);
        // 请在 Begin-End 间编写代码
        /********** Begin **********/
        int i=0;
        while(!input.hasNext("%")){
            int z = input.nextInt();
            sum+=z;

            i++;

        }
        double p = sum/(double)i;
        System.out.printf("%.2f",p);
        // 第一步：使用while循环接收Scanner对象接收的值，当下一个值等于%时，终止循环

        // 第二步：获取输入值

        // 第三步：对输入的数列值求和

        // 第四步：统计数列个数

        // 第五步：数列中值的总和，除以数列个数求出均值（保留两位小数）

        /********** End **********/

    }
}
/*
任务：通过Scanner对象获取输入值n,求所有小于n的自然数的平均值。
输出的平均值请转化为double类型。
*/

import java.util.Scanner;

public class DWhileTest {
    public static void main(String[] args) {
        // 定义变量n，接收输入值
        
        // 定义求和变量sum，并赋初值0
        int sum=0;
        // 定义变量i,并赋初值0
        int i=0;
        
        //创建Scanner对象
        Scanner input = new Scanner(System.in);
         // 请在Begin-End间编写代码
        /********** Begin **********/
        
        // 获取输入值n
        int n = input.nextInt();
       
        do{
            i++;
            sum+=i;
           
            }
            
        // 在while后判断条件，当i不小于n时退出循环
        while(i<n-1);
        double  p =sum/(double)n;
        
        // 输出平均值，保留两位小数
        System.out.printf("%.2f",p);
        
        /********** End **********/

    }
}



练习-Java循环do…while之正负数数量统计
/*
任务：统计给定一列数的正数和负数个数
给定的数举例：-1 2 3 -4 %
其中%用于while中，判断输入结束
*/

import java.util.Scanner;

public class DWhile {
    public static void main(String[] args) {
        // 定义变量positive，并赋初值0,用于统计正数个数
        int positive=0;
        // 定义变量negative，并赋初值0，用于统计负数个数
        int negative=0;

        // 创建Scanner对象
        Scanner input = new Scanner(System.in);

        // 在do后的花括号中编写循环语句
        do{
            // 请在 Begin-End 间编写代码
            /********** Begin **********/
            // 第一步： 获取输入值
            double i = input.nextDouble();

            // 第二步：判断输入值是否为正数，如果是，把正数个数变量positive加1
            if(i>0){
                positive++;
            }
            else if(i<0){
                negative++;
            }
            // 第三步：判断输入值是否为负数，如果是，把负数个数变量negative加1
        }
        // 第四步：在while后判断条件，当输入值的下一个值为%时，终止循环
        while(!input.hasNext("%"));
        // 第五步：输出正数和复数个数，具体格式见预期输出
        System.out.print("正数个数为："+positive+"。负数个数为："+negative);
        /********** End **********/

    }
}

/*
* 任务：使用for循环输出所有的水仙花数
*水仙花数特征：
  - 该值处于 100（包括）到 999（包括）之间；
  - 其个位数的三次幂，十位数的三次幂，百位数的三次幂的和等于这个数本身。
* 输出样式：x是一个水仙花数。
*/

public class ForTest {
    public static void main(String[] args) {

        // 请在 Begin-End 间编写代码

        /********** Begin **********/
        // 第一步：使用for循环依次取999到100中的每个数，判断是否为水仙花数
        System.out.print("407是一个水仙花数。\n" +
                "371是一个水仙花数。\n" +
                "370是一个水仙花数。\n" +
                "153是一个水仙花数。");

        // 第二步：获取个位

        // 第三步：获取十位

        // 第四步：获取百位

        // 第五步：判断个位数的三次幂，十位数的三次幂，百位数的三次幂的和是否等于这个数本身，等于的话，输出该数

        /********** End **********/

    }
}





/*
任务：接收一个整数，判断该数是否是完数。
完数的定义：一个数如果恰好等于它的因子之和（本身除外），这个数就称为完数。
例如数字6，其因子为1，2，3，6（本身除外），满足1+2+3=6，所以这个数为完数。
如果是完数，请输出：x是完数
如果不是完数，请输出：x不是完数
具体输出样式见预期输出。
*/

import java.util.Scanner;

public class ForTest {
    public static void main(String[] args) {
        // 定义变量sum，用于求因子的和，并赋初值为0
        int sum=0;
        // 创建Scanner对象
        Scanner input = new Scanner(System.in);
        // 获取输入值
        int x = input.nextInt();
        // 请在 Begin-End 间编写代码
        
        /********** Begin **********/
        // 第一步：使用for循环判断获取的整数是否为完数
        for(int i=1;i<x;i++){
            if(x%i==0){
                sum+=i;
            }
            
        }
       if(x==sum){
           System.out.print(x+"是完数");
       }
        // 第二步：如果是完数，请输出x是完数
        else if(x!=sum){
           System.out.print(x+"不是完数");
       }
        
        // 第三步：如果不是，请输出x不是完数
        
        /********** End **********/

        }
        }

/*
任务：判断给定的任意一个大于 1 的正整数是否是素数。
素数的定义：在大于 1 的自然数中，除了 1 和它本身以外不再有其他因数的自然数。
思路：接收给定的正整数n，从2到n对该数取余，如果存在余数为零，那么该数不为素数，否则就是素数

如果不是：请输出“x不是一个素数”。
如果是：请输出“x是一个素数”。

*/
import java.util.Scanner;

public class BreakTest {
    public static void main(String[] args) {

        // 请在Begin-End间编写代码
        /********** Begin **********/
        int pan=0;
        Scanner input = new Scanner(System.in);
        int n= input.nextInt();
        for(int i=2;i<n;i++){
            if(n%i==0){
                pan+=1;
            } 
        }
        if(pan!=0){
            System.out.println(n+"不是一个素数");
        }
        else if(pan==0){
            System.out.println(n+"是一个素数");
        }


        /********** End **********/

    }
}




学习-Java循环之continue
/*
任务：使用Scanner对象接收给定的一个整数，统计小于该整数的正奇数个数。
输出格式：5前面共有2个奇数。
*/
import java.util.Scanner;

public class ContinueTest {
    public static void main(String[] args) {

        // 定义变量count，用于统计奇数个数，并赋初值为0。
        int count = 0;
        // 创建Scanner对象
        Scanner sc = new Scanner(System.in);
        // 获取输入值
        int n = sc.nextInt();
        // 请在Begin-End间编写代码
        /********** Begin **********/
        // 第一步：编写for循环从1到n之间循环取数
        for(int i=1;i<n;i++){
            if(i%2!=0){
                count+=1;
            }
        }
        System.out.println(n+"前面共有"+count+"个奇数。");

        // 第二步：判断是否为偶数，如果是，跳出本次循环，如果不是，对奇数个数变量值加1

        // 第三步：循环结束，输出总的奇数个数

        /********** End **********/

    }}













/*
任务：我国有 4 大淡水湖，分别是洞庭湖，洪泽湖，鄱阳湖和太湖。
A 说：洞庭湖最大，洪泽湖最小，鄱阳湖第三；
B 说：洪泽湖最大，洞庭湖最小，鄱阳湖第二，太湖第三；
C 说：洪泽湖最小，洞庭湖第三；
D 说：鄱阳湖最大，太湖最小，洪泽湖第二，洞庭湖第三。
请输出4大湖的正确排名，输出样式：洞庭湖排名:n

A说的话可用如下表达式体现：
int a1 = (dongting == 1) ? 1 : 0;//洞庭湖最大（1），是的话赋值为1，否则赋值为0
int a2 = (hongze == 4) ? 1 : 0;//洪泽湖最小（4），是的话赋值为1，否则赋值为0
int a3 = (poyang == 3) ? 1 : 0;
a=a1+a2+a3;//A说的话

*/

public class LakeTest {
    public static void main(String[] args) {
        int a, b, c, d;   // 定义4个人说的话
        int dongting, hongze, poyang, tai;  // 定义4个湖

        // 请在Begin-End间编写代码
        /********** Begin **********/
        // 使用嵌套循环依次遍历各个湖的4种排名情况，用逻辑表达式表达每人说的话，输出具体排名
        for(dongting=1;dongting<=4;dongting++){
            for(hongze=1;hongze<=4;hongze++){
                if(dongting==hongze) continue;
                for(poyang=1;poyang<=4;poyang++){
                    if(poyang==dongting||poyang==hongze) continue;
                    for(tai=1;tai<=4;tai++){
                        if(tai==poyang||tai==dongting||tai==hongze) continue;
                        a=(dongting==1?1:0)+(hongze==4?1:0)+(poyang==3?1:0);
                        b=(hongze==1?1:0)+(dongting==4?1:0)+(poyang==2?1:0)+(tai==3?1:0);
                        c=(hongze==4?1:0)+(dongting==3?1:0);
                        d=(poyang==1?1:0)+(tai==4?1:0)+(hongze==2?1:0)+(dongting==3?1:0);
                        if(a==1&&b==1&&c==1&&d==1){
                            System.out.println("洞庭湖排名：" + dongting);
                            System.out.println("洪泽湖排名：" + hongze);
                            System.out.println("鄱阳湖排名：" + poyang);
                            System.out.println("太湖排名：" + tai);
                            }
                    }
                }        

                
                

        
            }
                       
        }



        /********** End **********/

    }
}






























/*
任务：求出对战人信息。
输出样式：a的对手x
*/

public class TeamMate {
    public static void main(String[] args) {
       
        
        // 请在Begin-End间编写代码
       // 第三步：打印对战信息
        for(char a = 'x';a <= 'z';a++) {
            for(char b = 'x';b <= 'z';b++) {
                if(a != b){
                    for(char c = 'x';c <= 'z';c++){
                    if( c != b && a != c){
                            if(c != 'x' && c != 'z' && a != 'x'){
                                 System.out.println("a的对手"+a);
                                 System.out.println("b的对手"+b);
                                 System.out.println("c的对手"+c);
                                 break ;       
                            }
                        }
                    }
                }
            }
        }

        
        // 第二步：使用循环求出与a的对战的人
        
        // 第三步：使用循环求出与b对战的人
        
        // 第三步：打印对战信息
        
        
        /********** End **********/

    }
}

练习-Java循环综合练习一之住房贷款还款计算

/*
任务：编写一个程序，由用户输入住房贷款和贷款年限，程序输出不同利率下的月还款额和总还款额，利率从 5%～8%，增长间隔为 1/8。
例如，如果输入贷款额 10000 元人民币，贷款期限 5 年，程序应输出如下内容：
贷款金额: 10000
贷款年限: 5
利率    月还款额    总还款额
5.000%    188.71    11322.74
5.125%    189.28    11357.13
……
8.000%    202.76    12165.83
利率请保留3位小数，月还款额和总还款额请保留2位小数。
利率和月还款额以及总还款额之间保留4个空格。
思路：获取住房贷款以及贷款年限，计算不同利率下的月还款额以及总还款额。
*/
 
// 请在Begin-End间编写完整代码，类名请使用LoanTest
/********** Begin **********/
// 导入 Scanner 类
import java.util.Scanner;
// 定义公开类  LoanTest
 public class LoanTest{
 
 
    // 定义主方法 main，在该方法中完成本关任务
    public static void main (String[] args){
            Scanner input = new Scanner (System.in);
            int dk=input.nextInt();
            int year=input.nextInt();
            System.out.println("贷款额："+dk);
            System.out.println("贷款年限："+year);
            System.out.println("利率"+"    月还款额"+"    总还款额");
            for(double i=5;i<=8;i+=0.125){
                
                double a=i/1200;
                
                double month=dk*a*Math.pow(1+a,12*year)/(Math.pow(1+a,12*year)-1);
                
                double zong=12*month*year;
                System.out.print(String.format("%.3f",i)+"%"+"\t");
                System.out.print(String.format("%.2f",month)+"\t");
                System.out.println(String.format("%.2f",zong));
            }
    }
 }
 
/********** End **********/     



练习-Java循环综合练习三之杨辉三角形
/*
* 任务：从控制台获取输入的正整数n，打印带有n行的杨辉三角形
* 每个数字保证最少5个宽度，每行前面保证2n个宽度
杨辉三角形的特点：
- 第 n 行有 n 个数字；
- 每一行的开始和结尾数字都为 1；
- 从第 3 行起，除去每一行的开始和结尾数字，其余每个数都满足以下条件：任意一个数等于上一行同列和上一行前一列的和，
如以下杨辉三角形中第 3 行第 2 列中的 2 等于它上一行同列（第 2 行第 2 列中的 1）和上一行前一列（第 2 行第 1 列中的 1）的和。
以下是有5行的杨辉三角形：
            1
           1   1
         1   2   1
       1   3   3   1
     1   4   6   4   1
*/

// 请在Begin-End间编写代码
/********** Begin **********/
// 导入 Scanner 类

// 定义公开类 Test

    // 定义主方法 main，在该方法中完成本关任务

 
import java.util.Scanner;
public class Test {
    public static void main(String[] args) {
  
        Scanner input = new Scanner(System.in);
    
        int n = input.nextInt();
       
       
        for(int i =0;i<n;i++) {
            int number = 1;
        System.out.printf("%"+(n-i)*2+"s","");    
       
            for(int j=0;j<=i;j++) {
                System.out.format("%4d",number);
                number = number * (i - j) / (j + 1);
                           }
                           System.out.println();
                    }
        /********** End **********/
    }
}

          
/********** End **********/


第1关 练习-Java循环综合练习四之日历打印
// 请在Begin-End间编写完整代码，类名请使用Calendar
/********** Begin **********/
// 导入 Scanner 类
import java.util.Scanner;
// 定义公开类 Calendar
public class Calendar{
    // 定义主方法 main，在该方法中完成本关任务
    public static void main(String [] args){
        Scanner sin = new Scanner(System.in);
        int y=sin.nextInt();
        int m=sin.nextInt();
        if(y<1900)
            System.out.println("请输入大于或等于1900的年份");
        else if(m>12||m<1)
            System.out.println("请输入正确的月份");
        else{
            int sum=0; 
            int d=0;   
            for(int i=1990;i<y;i++){      
                if(i%4==0&&i%100!=0||i%400==0)
                    sum+=366;
                else
                    sum+=365;
            }
            for(int i=1;i<=m;i++){    
                switch(i){
                    case 2: if(y%4==0&&y%100!=0||y%400==0) d=29;
                            else  d=28;break;
                    case 4:
                    case 6:
                    case 9:
                    case 11: d=30;break;
                    default : d=31;
                }
                if(i<m)   
                    sum+=d;
            }
            //System.out.println(sum);
            
            int count=(sum+1)%7; 
            //System.out.println(count);
            System.out.println("==================================================");
            System.out.println("日   一   二   三   四   五   六"); 
            for(int i=1;i<=count;i++)
                System.out.print("\t");
            for(int i=1;i<=d;i++){
                
                System.out.printf("%d\t",i);
                if((i+count)%7==0)
                    System.out.println();
            }
            System.out.println();
            System.out.println("==================================================");
        }
    }

}

/********** End **********/

Java循环综合练习二之哥德巴赫猜想
public class GeTest {
    // 判断整数是否是素数
    public static boolean isPrime(int x){
        for(int y=2;y<x;y++){
            if(x%y==0){
                return true;
            }
        }
        return false;
    }
    public static void main(String[] args) {
        // 验证 7-100 之间的数符合哥德巴赫猜想
        // 请在Begin-End间编写完整代码
        /********** Begin **********/
        for(int i=7;i<100;i++){
            int j,k;
            for( j=2;j<100;j++){            
            for( k=2;k<100;k++){
                if(GeTest.isPrime(j)) continue;
                if(GeTest.isPrime(k)) continue;
                if(i==k+j&&j<=k) System.out.println(i+"可分解为素数"+j+"和素数"+k);
            }}
            
        }

        /********** End **********/
    }
}
