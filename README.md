# -11-603

//сортировка массива через функцию

import java.util.*;

public class Homework{

	public static int[] sort(int[] a){

	for(int i = (a.length - 1); i > 0; i--){//сортируем

			for(int j = 0; j < i; j++){

				if(a[j] > a[j+1]){

					int save = a[j+1];
					a[j+1] = a[j];
					a[j] = save;				}
			}
		}

		return a;
	}


	public static void main(String[] args){

		int[] a = new int[10];
		int[] b = new int[a.length];

		Random rand = new Random();

		for(int i = 0; i < a.length; i++){//рандомно заполняем массив  и выводим его
			a[i] = rand.nextInt(100) - 50;

			System.out.print(a[i] + " ");

		}

		System.out.println();

		b = sort(a);

		for(int i = 0; i < b.length; i++)
			System.out.print(b[i] + " ");	
	}
}
