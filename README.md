package com.mycompany.mavenproject3;
import java.util.Scanner;

public class matrixagain {
    public static void main(String[] args) {
        Scanner input = new Scanner(System.in);

        System.out.print("Enter the rows = ");
        int rows = input.nextInt();
        System.out.print("Enter the columns = ");
        int cols = input.nextInt();

        int[][] matrix = new int[rows][cols];
        int[][] transpose = new int[cols][rows]; 

        System.out.println("Enter the matrix = ");
        for (int i = 0; i < rows; i++) {
            for (int j = 0; j < cols; j++) {
                matrix[i][j] = input.nextInt();
            }
        }

        for (int i = 0; i < rows; i++) {
            for (int j = 0; j < cols; j++) {
                transpose[j][i] = matrix[i][j]; 
            }
        }
        System.out.println("Transpose of the Matrix:");
        for (int i = 0; i < cols; i++) {
            for (int j = 0; j < rows; j++) {
                System.out.print(transpose[i][j] + " ");
            }
            System.out.println();
        }     
    }
}
