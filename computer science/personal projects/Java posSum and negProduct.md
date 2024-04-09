``` Java
package utilities;
  

public class NumberChecker {

  

public static void main(String[] args) {

int[] myVowels = {10,-5 , 20, -3, 40, -2};

int range = myVowels.length;

int count = 0;

for (int i = 0; i < range; i++) {

if(myVowels[i] < 0) {

count += 1;

}

}

int j = 0;

int k = 0;

int[] posNum = new int[myVowels.length - count];

int[] negNum = new int[count];

for (int i = 0; i < range; i++) {

if(myVowels[i] >= 0) {

posNum[j] = myVowels[i];

j++;

}

if(myVowels[i] < 0) {

negNum[k] = myVowels[i];

k++;

}

}

int posSum = 0;

int negProduct = 1;

for(int i = 0; i < negNum.length; i++) {

negProduct *= negNum[i];

}

for(int i = 0; i < posNum.length; i++) {

posSum += posNum[i];

}

System.out.println("Sum of positive numbers: " + posSum);

System.out.println("Product of negative numbers: " + negProduct);

}

  

}
```

just thought it was decent work tbh
