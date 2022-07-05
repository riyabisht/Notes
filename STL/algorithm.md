---
layout: default
title: Commanly used build in algorithms
parent: STL
---
# Comman function of algorithms

```cpp
#include<algorithm>
#include<vector>
vector<int>v
```

## sort

```cpp
// ascending order
sort(v.begin(),v.end());  
// decending order
sort(v.begin(),v.end(),greater<int>());  
```

or

```cpp

bool comapre(int a,int b)
{
return a>b;
}
// decending order
sort(v.begin(),v.end(),compare);
```

## reverse

```cpp
reverse(v.begin(),v.end());
```

## for_each

```cpp
//Print every element of vector 
void print(int n)
{
    cout<<n<<" ";
}
for_each(v.begin(),v.end(),print);
```
or

```cpp
for_each(v.begin(), v.end(), [](int n){ cout << n << " "; });
```



## max and min 

```cpp
*max_element(v.begin(),v.end())
*min_element(v.begin(),v.end())
```

## sum

"numeric" header file for accumulate 

```cpp
accumulate(v.begin(),v.end(),0);
```

## find

- n=element want to search
- return address

```cpp
// element we want to find
*find(v.begin(),v.end(),n)

// index of the element
find(v.begin(),v.end(),4)-v.begin()
```

## count

```cpp
count(v.begin(),v.end(),element)
```

## binnary_search

return true if element is present 

```cpp
if(binnary_search(v.begin(),v.end(),element))
cout<<"present";
else
cout<<"not present";
```

## lower_bound

return the  address of first occurance where the element is present

```cpp
lower_bound(v.begin(),v.end(),element);
```
for returning index

```cpp
lower_bound(v.begin(),v.end(),element)-v.begin();
```

## upper_bound

return the address next to the last occurence where the element is present

```cpp
upper_bound(v.begin(),v.end(),element)-v.begin();
```

## next_permutation

return value: 
- true : if the function could rearrange the object as a lexicographically greater permutation.
- false: to indicate that the arrangement is not greater than the previous, but the lowest possible (sorted in ascending order).

```cpp
 next_permutation(v.begin(),v.end());
```

## prev_permutation

```cpp
prev_permutation(v.begin(),v.end());
```
## all_of

return true if all are positive

```cpp
bool positive(int n)
{
    return n>0;
}

if(all_of(v.begin(),v.end(),positive))
cout<<"all positive\n";
else
cout<<"at least one negavtive is present\n";
```
## any_of

return true any of is positive

```cpp
bool positive(int n)
{
    return n>0;
}

if(any_of(v.begin(),v.end(),positive))
cout<<"Positive is present\n";
else
cout<<"Positive is not present\n";
```
## none_of

```cpp
bool positive(int n)
{
    return n>0;
}
if(none_of(var.begin(),var.end(),positive))
cout<<"none of the elemnts is positive\n";
else
cout<<"atleat one of the elemnts is positive ";
```

