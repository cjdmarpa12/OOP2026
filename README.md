<details>
<summary><b>hw1~5</b></summary>
	
### homework1
```homework1

public class Homework1{
  public static void main(String []args){
    int i, j;
    for(i=0; i<10; i++) {
      for(j=0; j<10; j++) {
        System.out.print("#");
      }
      System.out.println("");
    }
  }
}
```
![Alt homework11](./image/homework1.png)



### homework2
```homework2

public class homework2 {
    public static void main(String[] args) {
        int n = 20; // 피보나치 횟수

        System.out.println(n);
        fibonacci(n);
        //피보나치 횟수 출력
    }

    public static void fibonacci(int n) {
        if (n <= 0) return;

        long first = 0;
        long second = 1;

        for (int i = 1; i <= n; i++) {
        	//20까지 계산
            System.out.print(first + " ");

            //이전 값과 지금값 합산
            long next = first + second;
            first = second; // 이전 값을 세이브
            second = next;  // 이전값 세이브
        }
        System.out.println();
    }
}
```
![Alt homework11](./image/homework2.png)

### homework3
```homework3
package oop;

public class homework3 {
    public static void main(String[] args) {
        int n = 20;

        System.out.println(n);
        fibonacci(n);
    }

    public static void fibonacci(double n) {
        if (n <= 0) return;

        double first = 1;
        double second = 2;
        double third = 1;
        double fourth = 1;

        for (double i = 1; i <= n; i++) {
            System.out.println(second / fourth);

            double next = first + second;
            first = second;
            second = next;
            
            double under = third + fourth;
            third = fourth;
            fourth = under;
        }
    }
}
```
![Alt homework11](./image/homework3.png)

### homework4
```
package oop;

public class homework4 {

	public static void main(String[] args) {
		
				for(int i=1; i<10; i++) {
					for(int j=1; j<10; j++) {
						System.out.println(i + " X " + j + " = " + j*i + " ");
					}
					System.out.println();
				}
			

		
	}

}

```
![Alt homework11](./image/homework4.png)
### homework5
```
package oop;

public class homework5 {
    public static void main(String[] args) {
        double sum = 0.0;
        double root_twelve = Math.sqrt(12);
        
        for (int k = 0; k < 25; k++) {
            sum += Math.pow(-1.0 / 3.0, k) / (2 * k + 1);
            
            double Pi = root_twelve * sum;

            System.out.printf("%.15f\n", Pi);
        }
    }
}
```
![Alt homework11](./image/homework5.png)

</details>

<details>
<summary><b>hw6~8</b></summary>
	
### homework6
```
package oop;

public class homework6 {
	public static void main(String[] args) {
        
        int rows = 7;
        
        int[][] binomial = new int[rows][rows];

        for (int i = 0; i < rows; i++) {
            for (int j = 0; j <= i; j++) {
            	
                if (j == 0 || j == i) {
                    binomial[i][j] = 1;
                } else {
                    binomial[i][j] = binomial[i - 1][j - 1] + binomial[i - 1][j];
                }
            }
        }

        for (int i = 0; i < rows; i++) {
            for (int j = 0; j <= i; j++) {
                System.out.print(binomial[i][j] + " ");
            }
            System.out.println();
        }
    }
}

```
![Alt homework11](./image/homework6.png)

### homework7
```
public class homework7 {
    public static void main(String[] args) {
        //0~99개 난수 20개 만들기
        int data[] = new int[20];
        for(int i=0; i<20; i++) {
            data[i]=(int)(Math.random()*100);
        }
        //정렬전 데이터 출력
        for(int i=0; i<20; i++) {
            System.out.print(data[i] + " ");
        }
        System.out.println();

        for(int i = 0; i < data.length - 1; i++){
            int minindex = i; //현재 채워야 할 자리를 가장 작은 값의 위치로 가정

            //이후의 값들을 훑으며 최솟값의 위치를 탐색
            for(int j = i + 1; j < data.length; j++) {
                if(data[j] < data[minindex]) {
                    minindex = j; //더 작은값을 찾으면 그 위치를 기록
                }
            }

            //최솟값을 찾았으니 i와 minindex자리를 교환
            if (i != minindex) {
                int temp = data[i];
                data[i] = data[minindex];
                data[minindex] = temp; 
            }
        }
        //정렬한 결과 값 출력
        for(int i = 0; i < 20; i++) {
            System.out.print(data[i] + " ");
        }
    }
}

```
![Alt homework11](./image/homework7.png)

### homework8
```
package hw;
public class homework8 {

    public static void main(String[] args) {
        
        int student = 30;
        int[][] testsum = new int[student][4];

        System.out.println(" 번호 |  국어  영어  수학  과학 || 합계");
        System.out.println("---------------------------------------");


        for (int i = 0; i < student; i++) {
            int sum = 0;
            System.out.printf("%3d번째 학생 : ", (i + 1));

            for (int j = 0; j < 4; j++) {

                testsum[i][j] = (int)(Math.random() * 101);
                System.out.printf("%3d   ", testsum[i][j]);
                sum = sum + testsum[i][j];
            }

            System.out.printf("|| 합계: %3d점\n", sum);
        }
    }
}
```

</details>

<details>
<summary><b>hw10~14</b></summary>
	
### homework10
```
package hw;

public class homework10 {
    public static void main(String[] args) {
        int array_count, max_value, bin_size, display_scale, hist_size;

        
        if (args.length == 4) {
            array_count = Integer.parseInt(args[0]);
            max_value = Integer.parseInt(args[1]);
            bin_size = Integer.parseInt(args[2]);
            display_scale = Integer.parseInt(args[3]);
        } else {

            array_count = 50;
            max_value = 100;
            bin_size = 10;
            display_scale = 1;
        }
        
        hist_size = max_value / bin_size;
        
        int[] arr = new int[array_count];
        int[] hist = new int[hist_size];
        

        for (int i = 0; i < array_count; i++) {
            arr[i] = (int) (Math.random() * max_value);
        }
        for (int i = 0; i < array_count; i++) {
            System.out.print(arr[i] + " ");
        }
        System.out.println();
        

        for (int i = 0; i < array_count; i++) {
            hist[arr[i] / bin_size]++;
        }
        for (int i = 0; i < hist_size; i++) {
            System.out.print(hist[i] + " ");
        }
        System.out.println("\n");

        System.out.println("=== 히스토그램 (별 1개당 " + display_scale + "개) ===");
        for (int i = 0; i < hist_size; i++) {
            int start = i * bin_size;
            int end = (i + 1) * bin_size - 1;
            System.out.printf("%3d ~ %3d (%2d개) : ", start, end, hist[i]);

            int star_count = hist[i] / display_scale;
            for (int j = 0; j < star_count; j++) {
                System.out.print("*");
            }
            System.out.println();
        }
    }
}
```
![Alt homework11](./image/homework10.png)

### homework11
```
package hw;

import java.util.Arrays;
public class homework11 {
    public static void main(String[] args) {
        int array_count;
        
        if (args.length == 1) {
            array_count = Integer.parseInt(args[0]);
        } else {
            array_count = 100; 
        }

        int[] arr = new int[array_count];

        for (int i = 0; i < array_count; i++) {
            arr[i] = (int) (Math.random() * 100) + 1;
        }

        System.out.print("데이터 : ");
        for (int i = 0; i < array_count; i++) {
            System.out.print(arr[i] + " ");
        }
        System.out.println("\n");

        double sum = 0.0;
        double prod = 1.0;
        double logSum = 0.0;
        double reciprocalSum = 0.0;

        for (int i = 0; i < array_count; i++) {
            sum += arr[i];
            prod *= arr[i];
            logSum += Math.log(arr[i]);
            reciprocalSum += (1.0 / arr[i]);
        }

        double arithmeticMean = sum / array_count;
        
        double geometricMean = Math.pow(prod, 1.0 / array_count);
        if (Double.isInfinite(geometricMean)) {
            geometricMean = Math.exp(logSum / array_count);
        }
        
        double harmonicMean = array_count / reciprocalSum;

        Arrays.sort(arr);

        System.out.print("정렬된 데이터 : ");
        for (int i = 0; i < array_count; i++) {
            System.out.print(arr[i] + " ");
        }
        System.out.println("\n");

        double median;
        if (array_count % 2 == 1) {
            median = arr[array_count / 2];
        } else {
            median = (arr[(array_count / 2) - 1] + arr[array_count / 2]) / 2.0;
        }


        System.out.printf("arithmetic mean (산술평균) = %f\n", arithmeticMean);
        System.out.printf("geometric mean  (기하평균) = %f\n", geometricMean);
        System.out.printf("harmonic mean   (조화평균) = %f\n", harmonicMean);
        System.out.printf("median          (중앙값)   = %f\n", median);
    }
}


```
![Alt homework11](./image/homework11.png)

</details>
