# Swap-even-and-odd-bits-in-8-bit-int
Given an unsigned 8-bit integer, swap its even and odd bits. The 1st and 2nd bit should be swapped, the 3rd and 4th bit should be swapped, and so on.  For example, 10101010 should be 01010101. 11100010 should be 11010001.


#include <bits/stdc++.h> 
using namespace std; 
  
// Function to swap even  
// and odd bits  
unsigned int swapBits(unsigned int x)  
{  
    // Get all even bits of x  
    unsigned int even_bits = x & 0xAAAAAAAA;  
  
    // Get all odd bits of x  
    unsigned int odd_bits = x & 0x55555555;  
  
    even_bits >>= 1; // Right shift even bits  
    odd_bits <<= 1; // Left shift odd bits  
  
    return (even_bits | odd_bits); // Combine even and odd bits  
}  
  
// Driver code 
int main()  
{  
    unsigned int x = 23; // 00010111  
  
    // Output is 43 (00101011)  
    cout<<swapBits(x);  
  
    return 0;  
}  
