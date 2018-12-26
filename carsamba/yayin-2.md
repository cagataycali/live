# Yayın 2:
---

:hourglass: Başlık: **Beraber Öğreniyoruz - CS50**

> Yazılıma nereden başlamalıyım?

:dizzy: **Çıkarımlar:**

- https://www.tutorialspoint.com/cprogramming/index.htm
- https://www.learn-c.org/ *
- https://www.cprogramming.com/tutorial/c-tutorial.html
- https://www.w3schools.in/c-tutorial/
- https://www.geeksforgeeks.org/fundamentals-of-algorithms/ *
- https://www.toptal.com/developers/sorting-algorithms

:mega: **Konuşulanlar:**

- https://www.hackerrank.com/dashboard


#### Örnek algoritma:
* Önce suyu ısıt
* Isıtılan suyu bardağa koy
* Kahve kavanozunu aç
* Kahve kavanozundan 2 çay kaşığı kahve al
* Bardağa kahveyi koy
* Kaşık ile karıştır.


* Arama Algoritmaları

Örnek dizi: [15, 23, 16, 8, 42, 50, 4]

*Linear Search*

https://www.geeksforgeeks.org/linear-search/

```markdown
*for each* element in array
    *if* element you're looking for
        *return* true
return false
```

*Binary Search*

Örnek dizi: [4, 8, 15, *16*, 23, *42*, **50**]
Aranan: 50
İlk bakılan: 16
İkinci bakılan: 42
Üçüncü bakılan: 50

https://www.geeksforgeeks.org/binary-search/

```
look at middle of sorted array
if element you're looking for
    return true
else if element is to left
    search left half of array
else if element is to right
    search right half of array
else
    return false
```


* Sıralama Algoritmaları

*Insertion Sort*

https://www.geeksforgeeks.org/insertion-sort/

En kötü durumda: O(n2)
> https://www.toptal.com/developers/sorting-algorithms/insertion-sort

```
for i = 2:n,
    for (k = i; k > 1 and a[k] < a[k-1]; k--)
        swap a[k,k-1]
    → invariant: a[1..i] is sorted
end
```

*Bubble Sort*

https://www.geeksforgeeks.org/bubble-sort/

En kötü durumda: O(n2)

> https://www.toptal.com/developers/sorting-algorithms/bubble-sort

> https://visualgo.net/bn/sorting

> https://www.youtube.com/watch?v=S74CRUi5kNI&app=desktop

```
for i = 1:n,
    swapped = false
    for j = n:i+1,
        if a[j] < a[j-1],
            swap a[j,j-1]
            swapped = true
    → invariant: a[1..i] in final position
    break if not swapped
end
```

*Selection Sort*

https://www.geeksforgeeks.org/selection-sort/

En kötü durumda: O(n) swap - O(n2) comparison


```
for i = 1:n,
    k = i
    for j = i+1:n, if a[j] < a[k], k = j
    → invariant: a[k] smallest of a[i..n]
    swap a[i,k]
    → invariant: a[1..i] in final position
end
```


*Merge Sort*

https://www.geeksforgeeks.org/merge-sort/

En kötü durumda: O(n * log n)

```
# split in half
m = n / 2

# recursive sorts
sort a[1..m]
sort a[m+1..n]

# merge sorted sub-arrays using temp array
b = copy of a[1..m]
i = 1, j = m+1, k = 1
while i <= m and j <= n,
    a[k++] = (a[j] < b[i]) ? a[j++] : b[i++]
    → invariant: a[1..k] in final position
while i <= m,
    a[k++] = b[i++]
    → invariant: a[1..k] in final position
```
