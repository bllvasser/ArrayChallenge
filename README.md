# ArrayChallenge
package com.company;

import java.util.Arrays;
import java.util.Collections;
import java.util.Scanner;

public class Main {

    private static Scanner scanner = new Scanner(System.in);

    public static void main(String[] args) {


        int[] myIntegers = getIntegers(5);
        //int[] sorted = sortArrays(myIntegers);
        int[] sorted = sortIntegers(myIntegers);
        printArrays(sorted);

    }

    public static int[] getIntegers(int capacity) {
        int[] getArrays = new int[capacity];
        System.out.println("Enter Capacity");
        for (int i = 0; i < getArrays.length; i++) {
            getArrays[i] = scanner.nextInt();
        }
        return getArrays;
    }

    public static void printArrays(int[] getArrays) {
        for (int i = 0; i < getArrays.length; i++) {
            System.out.println("enter integers" + getArrays[i]);
        }
    }
    public static void printArray(int[] intArray) {
        for (int i = 0; i < intArray.length; i++) {
            System.out.println("Element " + i + " contents " + intArray[i]);
        }
    }

    public static int[] sortIntegers(int[] array){
        int[] sortedArray = new int[array.length];
        for(int i = 0; i < array.length; i++){
            sortedArray[i] = array[i];
        }
        //int[] sortedArray = Arrays.copyOf(array, array.length);

        boolean flag = true;
        int temp;
        while(flag){
            flag = false;
            for(int i = 0; i < sortedArray.length - 1; i++){
                if(sortedArray[i] < sortedArray[i+1]){
                    temp = sortedArray[i];
                    sortedArray[i] = sortedArray[i + 1];
                    sortedArray[i + 1] = temp;
                    flag = true;
                }
            }
        }
        return sortedArray;
    }
}

   // public static int[] sortArrays(int[] getArrays) {
      //  int temp = 0;


      //  int[] sortedArrays = Arrays.copyOf(getArrays, getArrays.length);
        //Arrays.sort(getArrays, Collections.reverseOrder());
      //  return getArrays;

        //for(int i = 0; i < sortedArrays.length; i++){
        //    for(i = i+1; i+1 < sortedArrays.length; i++ ){
        //        if(sortedArrays[i] > sortedArrays[i + 1]){
         //           temp = sortedArrays[i];
         //           sortedArrays[i] = sortedArrays[i+1];
          //          sortedArrays[i + 1] = temp;
         //       }
          //  }
        //}
      //  return sortedArrays;
   // }
//}

    //public static void example(){
     //   Integer[] test = {7,3,9,1,6};
      //  for(int i = 0; i<test.length; i++){
      //      Arrays.sort(test, Collections.reverseOrder());
       //     System.out.println(test[i]);
       
/Library/Java/JavaVirtualMachines/amazon-corretto-11.jdk/Contents/Home/bin/java "-javaagent:/Applications/IntelliJ IDEA CE.app/Contents/lib/idea_rt.jar=50395:/Applications/IntelliJ IDEA CE.app/Contents/bin" -Dfile.encoding=UTF-8 -classpath /Users/Bilaal/IdeaProjects/ArrayChallenge/out/production/ArrayChallenge com.company.Main
Enter Capacity
5
160
15
5
26
enter integers160
enter integers26
enter integers15
enter integers5
enter integers5

Process finished with exit code 0



