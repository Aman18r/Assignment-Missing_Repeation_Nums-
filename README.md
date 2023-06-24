# Assignment-Missing_Repeation_Nums-

import java.io.*;

class Main{
    static void printTwoElements(int[] arr, int n){

        int[] temp = new int[n];
        int repeatingNumber = -1;
        int missingNumber = -1;

        for(int i = 0; i < n; i++){
            temp[arr[i] - 1]++;
            if(temp[arr[i] - 1] > 1){
                repeatingNumber = arr[i];
            }
        }
        for(int i = 0; i < n; i++){
            if(temp[i] == 0){
                missingNumber = i + 1;
                break;
            }
        }
        System.out.println("The Repeating Number is: " + repeatingNumber);
        System.out.println("The Missing Number is: " + missingNumber);

    }

    public static void main(String[] args) {
        int[] arr = {1,2,2,4};
        int n = arr.length;
        printTwoElements(arr, n);
    }
}
