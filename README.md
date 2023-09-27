# FirstRepeatingElement

package com.fk.feturnse;

import java.util.HashSet;

/**
 * Amdocs 1+ years of Experience.
 * 
 * Print First Repeating number in array.
 * 
 * int arr[]={1,3,5,6,3,7,8,22};
 * 
 * Output:- Fist Repeating Elements is 3.
 * 
 * @author Firoj
 * 
 * @since 2023-09-27
 * 
 */

public class FirstRepeatingElement {

	public static void main(String[] args) {
 
		int arr[]={1,3,5,6,3,7,8,22};
  
		firstRepeatingNumber(arr);
  
	}
 
		static void firstRepeatingNumber(int arr[]) {
  
			// This will hold first repeated element of index.
			int min=-1;
   
			// I try to declare Hash Set 
			HashSet<Integer> set=new HashSet<Integer>();
   
			// Iterate through 
			for(int i=0;i<=arr.length-1;i++) {
   
				if(set.contains(arr[i])) {
    
					min=i;
     
					break;
     
				}
    
				else {
    
					set.add(arr[i]);
     
				}
    
			}
   
			if(min!=-1) {
   
				System.out.println("Repeating Element is:-"+arr[min]);
    
			}else {
   
				System.out.println("No Repeating Element");
    
			}
   
		}

}
