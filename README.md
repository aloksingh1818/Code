# Code

White Space: (c++)

#include <bits/stdc++.h>
using namespace std;
int main() {
string a,b;
getline(cin,a);
getline(cin,b);
//don't read the input if the function is provided with strings as arguments
int ac = 0 , bc = 0 ;
int i;
for( i = 0 ; i < a.length() ; i++ ){
if( isspace( a[i]) )ac++;
}
for( i = 0 ; i < b.length() ; i++ ){
if( isspace( b[i]) )bc++;
}
if( abs(ac-bc) % 2 == 0 )cout<<"Even"<<abs(ac-bc)<<endl;
else cout<<"Odd"<<abs(ac-bc)<<endl;
}

#Difference bw white spaces in str 1 and 2
#Approach 1

s = input()
s2 = input()
cnt = 0
cnt2 = 0
for char in s:
if char == " ":
cnt += 1
for char in s2:
if char == " ":
cnt2 += 1
print(cnt - cnt2)

#Approach 2
s = input()
s2 = input()
cnt = s.count(' ')
cnt2 = s2.count(' ')
print(cnt - cnt2)
Even odd indices
def difference( N,A): sum_odd_index = 0 xor_even_indices = 0 for i in range(N):
if i%2==0: xor_even_indices ^= A[i]
else:
sum_odd_index += A[i]
return sum_odd_index-xor_even_inidces N = int(input())
A = list(map(int, input().split()))
result = differences(N,A)
print(result)

2.Special Fibonacci:
#include <bits/stdc++.h>
using namespace std;
int main() {
int n;
cin>>n;
vector<int>a(n+1);
a[0] = 1;
a[1] = 1;
int i;
int modd = 47;
for( i = 2 ; i <= n ; i++ ){
a[i] = ( (( a[i-2]*a[i-2] )%modd) + (( a[i-1]*a[i-1] )%modd) )%modd;
}
cout<<a[n]%47<<endl;
}

3.Reverse Array
arr = list(map(int, input().split()))
n = int(input())
i=0
j=n-1
while i < j:
arr[i], arr[j] = arr[j], arr[i] # Swap elements
i += 1
j -= 1
sum_even_indices = 0
for i in range(0, n, 2):
sum_even_indices += arr[i]
print(sum_even_indices)

4)Lower Case Count with Characters:
#include <bits/stdc++.h>
using namespace std;
int main() {
string s;
cin>>s;
int i;
string ans = "";
int cnt = 0 ;
for( i = 0 ; i < s.length(); i++ ){
if( islower(s[i]) ){
ans += s[i];
cnt++;
}
}
cout<<ans<<cnt<<endl;

}

6.Canopy/Area of circle
a = int(input())
A = 3.14*a*a
if A-int(A)> 0.5:
print(int(A)+1)
else:
print(int(A))

5. Halloween and Candies
#include <bits/stdc++.h>
using namespace std;
int main() {
int n,m,cnt=0;
cin>>n;
int i;
vector<int>a(n);
for( i = 0 ; i < n ; i++ )cin>>a[i];
cin>>m;
sort(a.begin(),a.end());
for( i = 0 ; i < n ; i++ ){
if( a[i]%5==0 )
cnt++;
else{
if( a[i] <= m ){
cnt++;
m -= a[i];
}
}
}

cout<<cnt<<endl;
}

description- you are leading an arctic expedition
Input1: a = Array
Input2: Size of array
MX=0
for i in range(input2-2,-1,-1):
result =1
while a[i] > a[i+1] and i>=0:
result+=1
i-=1
if result > MX:
MX=result
if MX >= 3:
return MX

Second largest number count
int[] arr={1,2,4,5,8,2,4,5,5};
int n=arr.length;
Arrays.sort(arr);
int i=n-2;

while(i>0&&arr[i]==arr[n-1]){
i--;
}
if(i==0)System.out.println(-1);
int j=i;
int count=0;
while(j>0&&arr[j]==arr[i]){
j--;
count++;
}
System.out.println(count);


Hello World//Calculate the spaces in the string

def calculate_space_difference(input1: str, input2: str):
spaces_in_input1 = input1.count(' ')
spaces_in_input2 = input2.count(' ')
difference = abs(spaces_in_input1 - spaces_in_input2)
if difference % 2 == 0:
result = "even"
else:
result = "odd"
return result, difference
input1 = "Hello world"
input2 = "Hello world"
result, difference = calculate_space_difference(input1, input2)
print(f"The difference is {difference} and it is {result}."

Matching words in dictionary with position

def match_words_with_positions(text: str, words_dict: dict):
# Split the text into words
words = text.split()

positions = {}
for i, word in enumerate(words):
if word in words_dict:
positions[word] = i + 1 # Positions are 1-based
return positions
text = "apple banana orange apple mango"
words_dict = {"apple": None, "mango": None, "grape": None}
positions = match_words_with_positions(text, words_dict)
print(positions)

Calculate the dividend

If dividend present in the array ,then return index of dividend
Or else
Return -1

Input1:array elements
Input2:D-Divisor
Input3:Q-quotient
Input4:R-remainder
Input5:length of the array
(Formula for calculating dividend is
Divisor*quotient+remainder)

Testcase1:

Input1:{36,27,12,13}
Input2:5
Input3:5
Input4:1
Input5=4

Output:-1

Testcase2:
Input1:{12,24,35,9}
Input2:8
Input3:3
Input4:0
Input5:4

Output:1Coding question

Calculate the dividend
If dividend present in the array ,then return index of dividend
Or else
Return -1

Input1:array elements
Input2:D-Divisor
Input3:Q-quotient
Input4:R-remainder
Input5:length of the array
(Formula for calculating dividend is
Divisor*quotient+remainder)

Testcase1:

Input1:{36,27,12,13}

Input2:5
Input3:5
Input4:1
Input5=4

Output:-1

Testcase2:
Input1:{12,24,35,9}
Input2:8
Input3:3
Input4:0
Input5:4

Output:1

1.EVEN OR ODD
#include <bits/stdc++.h>
using namespace std;
int main() {
// Write C++ code here
int n;
string res="";
cin>>n;
int arr[n];
for(int i=0;i<n;i++)
{
cin>>arr[i];
if(arr[i]%2==0)
{
res=res+"even";
}
else
{
res=res+"odd";
}
}
cout<<res;
return 0;

2.SUM XOR
#include <bits/stdc++.h>
using namespace std;
int main() {
// Write C++ code here
int n;
cin>>n;
int arr[n];
int odd=0,even=0;
for(int i=0;i<n;i++)
{
cin>>arr[i];
if(i%2==0)
{
even=(even^arr[i]);
}
else

{
odd+=arr[i];
}
}
cout<<odd-even;;
return 0;
}
3.MAX PAIR PRODUCT\
#include <bits/stdc++.h>
using namespace std;
int main() {
// Write C++ code here
int n;
cin>>n;
int arr[n];
map<int,int> mp;
for(int i=0;i<n;i++)
{
cin>>arr[i];
mp[arr[i]]++;
}
int ans=0;
int first=0,second=0;
for(int i=0;i<n;i++)
{
if(mp[18-arr[i]]>0)
{
if(arr[i]==9&&mp[9]==1)
continue;
int temp=arr[i]*(18-arr[i]);
if(temp>ans)
{
ans=temp;
first=max(arr[i],18-arr[i]);
second=min(arr[i],18-arr[i]);
}
}
}
// int res[2];
// res[0]=first;
// res[1]=second;
// return res;

cout<<first<<" "<<second;
return 0;
}
4.BALL HEIGHT
#include <bits/stdc++.h>
using namespace std;
int main() {
int h,v,vn;
cin>>h>>v>>vn;
int en=v/vn;
int e2n=pow(en,2);
int h1=h*e2n;
cout<<h1;
return 0;
}
5.SPECIAL FIBONACI
#include <bits/stdc++.h>
using namespace std;
int main() {
int n;
cin>>n;
long long f[100000];
f[0]=1;
f[1]=1;
for(int i=2;i<n;i++)
{
f[i]=f[i-1]*f[i-1]+f[i-2]*f[i-2];
f[i]=f[i]%47;
}
cout<<f[n-1];
return 0;
}
6.MAX PERMUTATION
def fact(n):
if n<=1:
return 1
return n*fact(n-1)

val=0
for word in input1:
res=""
for char in word.lower():
if char not in "aeiou":
res+=char
if len(res!=0):
val=max(val,fact(len(res)))
return val

7.REVERSE ARRAY
int eversum(vector<int>& input1, int input2) {
vector<int> x = input1;
reverse(x.begin(), x.end());
int sum = 0;
for (int i = 0; i < input2; ++i) {
if (i % 2 == 0) {
sum += x[i];
}
}
return sum;
}

8.FILE VERSION
import re
if input2==0
return -1
maxversion = -1
pattern =r"File_(\d+)"
for file in inputl:
match = re.match(pattern, file.strip())
if match:
version=int(match.group(l))
maxversion=max(maxversion, version)
return maxversion


9.HALLOWEEN
#include <bits/stdc++.h>
using namespace std;
int main() {
int n;
cin>>n;
int a[n];

for(int i=0;i<n;i++)
{
cin>>a[i];
}
int tot;
cin>>tot;
int ans=0;
sort(a,a+n);
for(int i=0;i<n;i++)
{
if(a[i]%5==0)
{
ans++;
}
else
{
if(tot>=a[i])
{
tot-=a[i];
ans++;
}
}
}
cout<<ans;
return 0;

10.RHYMA
res="No Word"
max_val=ø
t=inputl[ ::-1]
for word in input2:
if word!=input1:
curr=0
s=word[::-1]
i=0
while i<min(len(s),len(t)):
if s[i]==t[i]:
curr+=l
else:
break
i+=1
if curr>max_val:
max_val=curr

res=word
return res

11.CANOPY AREA

A=3.14*input1* input2
if A-int(A)>0.5:
return int (A)+1
else:
return int(A)

12.ISLAND LIFE

days=input3-input3//7
required=input2*input3
maximum=input1*days
if required >maximum:
return -1
box=required//input1
if required%input1!=0:
box+=1
return box

13.NAME ENTRY

return input1.lower()+"
"+input2. upper()

14.HIKE TRAIL
return max(input1)

15.PRIME NUMBER PICNIC
bool is Prime (int m) {
if (n<=1)
return false
for (i=2; i<=sqrt(n);i++) {
if (n%i==0)
return false;
}
return true;
}
int main() {
int n;
cout <<"";
cin>>n;
int sum=0,

for (int 1=2;1<=n;i++) {
if (isprime(i)) {
sum+=i;
}
}
cout<<sum<<endl;
return 0;
}

16.STABILIZE THE SYSTEM
x=str(input 1) . replace( '0',' 5' )
return int ( x)


17.PRODUCT PAIR
int main() {
int n;
cin>>n;
int a[n];
map<int,int> mp;
for(int i=0;i<n;i++)
{
cin>>a[i];
mp[a[i]]++;
}
int ans=0;
vector<int> v;
for(auto x:mp)
{
v.push_back(x.first);
}
n=v.size();
for(int i=0;i<n;i++)
{
if(v[i]%3==0)
{
ans+=n-i-1;
}
}
cout<<ans;
return 0;
}

18.CHOCOLATE JAR
arr=input1
c=0

for i in arr:
if i==0:
continue
if i<=3:
c+=1
else:
if i%3==0:
c+=(i//3)
else:
c+=(i//3)+1
return c

19.ROCK PAPER SCISSOR

d={"scissors":"rock","paper":"scissors","rock":"paper"}
return d[input1]
20.FINANCIAL DISTRICT\
c=0
for i in input1:
if i<0:
c+=1
return c

21.MAGICAL NUMBER

c=0
for i in range(1,input1+1):
temp=list(map(int,bin(i)[2:]))
s=sum(temp)+len(temp)
if s%2!=0:
c+=1
return c

22.CHARACTER COUNT

class UserMainCode(object):
@classmethod
def count(cls, input1, input2, input3):
# Return the count of the character input3 in the string input1
return input1.count(input3)

# Example usage
result = UserMainCode.count("helloworld", 10, "l")
print(result) # Output will be 3

23.DANIEL(e**2)

class UserMainCode(object):
@classmethod
def rebound(cls, inputi, inputz, inputs):
"""
inputi: int
inputz: int
inputs: int
Expected return type: int
"""
e = inputz / inputs # e = 20 / 5 = 4.0
res = inputi * (e ** 2) # res = 10 * (4.0 ** 2) = 10 * 16.0 = 160.0
return int(res) # Returns 160 as an integer
# Example usage
output = UserMainCode.rebound(10, 20, 5)
print(output) # This will print: 160

Character count

def count_character(input1, input2, input3):
return input1.count(input3)
Or
def count_character(input1, input2, input3):
count = 0
for char in input1:
if char == input3:
count += 1
return count
input1 = input()
input2 = int(input())
input3 = input()
output = count_character(input1, input2, input3)
print(output)

Ball rebound height

def rebound_height(H, V, V_final):
e = V_final / V
return int(H * (e ** 2))
input1 = int(input())
input2 = int(input())
input3 = int(input())
output = rebound_height(input1, input2, input3)
print(output)

Even odd

def even_odd_labels(A, N):
return ' '.join(['even' if x % 2 == 0 else 'odd' for x in A])
Or
def even_odd_labels(A, N):
result = []

for x in A:
if x % 2 == 0:
result.append('even')
else:
result.append('odd')
return ' '.join(result)
input1 = list(map(int,input().split())
input2 = int(input())
output = even_odd_labels(input1, input2)
print(output)

Maximum Permutation Value

import math
def max_permutation_value(strings, N):
vowels = set('aeiouAEIOU')
total_permutable_characters = 0
for string in strings:
for char in string:
if char not in vowels:
total_permutable_characters += 1
if total_permutable_characters == 0:
return 0
return math.factorial(total_permutable_characters)

Or

import math
from functools import lru_cache
@lru_cache(None) # Caching factorial results for better performance
def factorial(n):
if n <= 1:
return 1

return n * factorial(n - 1)
def max_permutation_value(strings, N):
vowels = {'a', 'e', 'i', 'o', 'u'}
total_permutable_characters = 0
for string in strings:
for char in string:
if char.lower() not in vowels:
total_permutable_characters += 1
if total_permutable_characters == 0:
return 0
return factorial(total_permutable_characters)
input1 = list(map(int,input().split())
input2 = int(input())
output = max_permutation_value(input1, input2)
print(output)

Reverse Array


def positions_reversed(A, N):
return sum(A[i] for i in range(0, N, 2))
Or
def positions_reversed(A, N):
reversed_A = A[::-1]
even_position_sum = 0
for i in range(N):
if i % 2 == 0:
even_position_sum += reversed_A[i]
return even_position_sum
input1 = list(map(int,input().split())
input2 = int(input())
output = positions_reversed(input1, input2)
print(output)

Even Odd label

def even_odd_labels(A, N):
result = []
for num in A:
if num % 2 == 0:
result.append('even')
else:
result.append('odd')
return ' '.join(result)
input1 = list(map(int,input().split())
input2 = int(input())
output = even_odd_labels(input1, input2)
print(output)

Halloween Candies

def max_candies(n, prices, money):
count = 0
for price in prices:
if price % 5 == 0:
count += 1
elif money >= price:
money -= price
count += 1
return count
input1 = int(input())
Input2 = list(map(int,input().split())
input3 = int(input())
output = max_candies(input1, input2, input3)
print(output)

Stabilize the System

def stabilize_system(value):
return int(str(value).replace('0', '5'))input= int(input())
output = stabilize_system(input_value)
print(output)

Product Pair

def count_product_pairs(arr):
from collections import defaultdict
count = 0
freq = defaultdict(int)
for num in arr:
if num % 3 == 0:
freq[num] += 1
for num in freq:
if freq[num] > 1:
count += 1
return count
array = list(map(int,input().split())
output = count_product_pairs(array)
print(output)

Chocolate Jar

def chocolates_for_A(jars):
total_chocolates = 0
for i in range(len(jars)):
if i % 3 == 0:
total_chocolates += jars[i]
return total_chocolates

input_jars = list(map(int,input().split())
output = chocolates_for_A(input_jars)
print(output)

Circle area

import math
def area_circle(radius):
return round(math.pi * radius * radius)
input_radius = in(input())
print(area_circle(input))

Financial Dataset

def count_negative_growth_days(A, N):
count = 0
for i in range(1, N):
if A[i] < A[i - 1]:
count += 1
return count
input1 = list(map(int,input().split())
input2 = int(input())
output = count_negative_growth_days(input1, input2)
print(output)


Magical Number

def count_magical_numbers(N):
count = 0
for num in range(1, N + 1):
binary_str = bin(num)[2:]
modified_str = binary_str.replace('10', '1').replace('1', '2')
digit_sum = sum(int(char) for char in modified_str)
if digit_sum % 2 != 0:
count += 1
return count
input1 = int(input())
output = count_magical_numbers(input1)print(output)


Longest Increasing Subsequence in string


def longest_increasing_subsequence(s):
s = list(s)
n = len(s)
lis = [1] * n
for i in range(1, n):
for j in range(0, i):
if s[i] > s[j] and lis[i] < lis[j] + 1:
lis[i] = lis[j] + 1
return max(lis)
input_string = input()
output = longest_increasing_subsequence(input_string)
print(output)



Second Largest Number in an Array


def second_largest_number(arr):
if len(arr) < 2:
return None
unique_arr = sorted(set(arr), reverse=True)
if len(unique_arr) < 2:
return None
return unique_arr[1]
input_array = list(map(int,input())
output = second_largest_number(input_array)
print(output)



Find Sum of Prime Numbers till N

def sum_of_primes(N):
if N < 2:
return 0
primes = [True] * (N + 1)
p=2
while (p * p <= N):

if (primes[p] == True):
for i in range(p * p, N + 1, p):
primes[i] = False
p += 1
return sum(i for i in range(2, N + 1) if primes[i])
input_N = int(input())
output = sum_of_primes(input_N)
print(output)


Refueling Vehicles

def refueling_stops(X, N):
return (N - 1) // X + 1

input1 = int(input())
input2 = int(input())
output = refueling_stops(input1, input2)
print(output)
Or
def refueling_stops(X, fuel):
stops = 0
for i in range(len(fuel)):
while fuel[i] < X:
fuel[i] += X
stops += 1
return stops
input_X = int(input())
input_fuel = list(map(int,input().split())
output = refueling_stops(input_X, input_fuel)
print(output)


Hike Trail

def find_summit_elevation(A, N):
peak = 0
for i in range(1, N-1):
if A[i-1] < A[i] > A[i+1]:

peak = A[i]
break
return peak
input1 = list(map(int,input().split())
input2 = int(input())
output = find_summit_elevation(input1, input2)
print(output)

or

def hike_trail(arr):
peak = arr[0]
for i in range(1, len(arr)):
if arr[i] > peak:
peak = arr[i]
return peak
input_array = list(map(int,input().split())
output = hike_trail(input_array)
print(output)


Rock paper scissor

def winning_move_for_B(M):
if M == 'rock':
return 'paper'
elif M == 'paper':
return 'scissors'
elif M == 'scissors':
return 'rock'
else:
return 'Invalid move'

input1 = input()
output = winning_move_for_B(input1)
print(output)

Name Entry

def format_name(F, L):
return F[0].lower() + F[1:] + " " + L.upper()

input1 = input()
input2 = input()
output = format_name(input1, input2)
print(output)

Questions related to strings

First Repeating Character
Given a string of characters, find the first repeating character.

def RepeatingCharacter(s):
cnt={}
for char in s:
if char in cnt:
cnt[char] += 1
return char
else:
cnt[char] = 1
return '.'

T=int(input())
for i in range(T):
s=input().strip()
result=RepeatingCharacter(s)
print(result)

Longest Palindromic Substring

Given a string, find the length of the Longest Palindromic Substring

def lp(s,n):
ans=1
for p in range(0,n-1):
ans=max(ans,palinlen(s,n,p,p+1))
ans=max(ans,palinlen(s,n,p-1,p+1))
return ans
def palinlen(s,n,p1,p2):
while(p1>=0 and p2 <n and s[p1]==s[p2]):
p1 -= 1
p2 += 1
return p2-p1-1
t=int(input())
for i in range(t):
n=int(input())
s=input()
print(lp(s,n))

Words, Vowels and Consonants
Given a sentence containing only uppercase/lowercase english alphabets and spaces, you have to
count the number of words, vowels and consonants.

def count_wordvowelconsonant(s):
vowels=set('aeiouAEIOU')
words=s.split()
wordcount=len(words)
vowels_count=0
consonant_count=0
for char in s:

if char.isalpha():
if char in vowels:
vowels_count+=1
else:
consonant_count += 1
return wordcount,vowels_count,consonant_count
n=int(input())
for i in range(n):
s=input().strip()
words,vowels,consonants=count_wordvowelconsonant(s)
print(words,vowels,consonants)

Finding Frequency
Given an array, you have to find the frequency of a number x.

# Enter your code here. Read input from STDIN. Print output to
STDOUT
def fun(arr,n,queries):
cnt={}
for i in arr:
if i in cnt:
cnt[i] += 1
else:
cnt[i] = 1

result=[]
for x in queries:
if x in cnt:
result.append(cnt[x])

else:
result.append(0)
return result

n=int(input())
arr=list(map(int,input().split()))
q=int(input())

queries=[int(input()) for _ in range(q)]
results=fun(arr,n,queries)
for i in results:
print(i)

Unique Elements
Print unique elements of the array in the same order as they appear in the input.

# Enter your code here. Read input from STDIN. Print output to STDOUT
n=int(input())
arr=list(map(int,input().split()))
count ={}
for num in arr:
if num in count:
count[num] += 1
else:
count[num] =1
unique=[num for num,freq in count.items() if freq == 1]
print(' '.join(map(str,unique)))

Finding Missing Number
Given an array of size N, it contains all the numbers from 1 to N+1 inclusive, except one number.
You have to find the missing number.

t=int(input())
for i in range(t):
n=int(input())
lst=list(map(int,input().split()))
sumlst=sum(lst)
N=((n+2)*(n+1))//2
no=N-sumlst
print(no)

Power of 2
Given a number, check if it is a power of 2.

def power(n):
if n<=0:
return False
while n>1:
if n%2 != 0:
return False
n=n>>1
return True

t=int(input())
for i in range(t):
n=int(input())
power(n)
if power(n)==True:
print("True")
else:
print("False")

First and Last
You are given an array A of size N, containing integers. Your task is to find the first and last
occurrences of a given element X in the array A and print them.

n=int(input())
arr=list(map(int,input().split()))
x=int(input())
foccur=-1
loccur=-1
for i in range(n):
if arr[i] == x:
if foccur == -1:
foccur = i
loccur =i
print(foccur,loccur)


