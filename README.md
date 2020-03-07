# 抱佛脚罢了

## C++



## C#



## 数据结构和算法

### 数据结构

stack(FIFO), queue(LIFO), linked list

hash table

binary search trees （二叉搜索树。。。左子树上所有节点小于根节点，右子树上所有节点大于根节点，递归定义

[更多有关二叉树的，完美完全完满](https://www.cnblogs.com/idorax/p/6441043.html)

[红黑树](https://www.jianshu.com/p/e136ec79235c)就是一种自平衡二叉查找树（红黑树是STL里map的原型



### 图相关算法



### 游戏相关

[A*算法](https://blog.csdn.net/hitwhylz/article/details/23089415): 要点是维护open_list, closed_list，还有就是F = G+H，一直这么更新下去直到到达终点

### 排序算法

bubble-sort, insertion-sort, ...

quicksort (unstable) nlogn~n<sup>2</sup> : partition

mergesort (stable) nlogn: merge

heapsort: min-heap & max-heap 建立最大/最小堆是O(n)，heapsort是O(nlogn)，但性能是比不上实现地比较好的quicksort的，但是堆本身的性质可以很有用（比如priority_queue的原型就是最大/最小堆）

寻找中位数：近期学过的，记住partition的思想就可以，包括配对bolts&nuts也是这样，确定pivot然后partition就可以

找第i大的：也是random_partition的思想（跟找中位数是一模一样的）

分治可以注意的是找fake coin的那个例子，分成三堆是最文明的，虽然只是从log<sub>2</sub> <sup>n</sup> 优化到了log<sub>3</sub> <sup>n</sup>而已，但蛮有意思

寻找最大/最小：本来要比较2n次，通过先将元素pair然后互相比较（n/2次），再将其中小的那个跟min比较，大的跟max比较（n次），可以减少到3/2n次



#### 线性排序算法

上面很多都是comparison sorts，也就是基于比较输入，这样的算法总要比较nlogn次，所以O(nlogn)，可用决策树证明，最坏情况就是树的高度h, n! <= l <= 2<sup>h</sup> 可以推出h>=lg(n!) = omega(nlgn)

而下面这三种典型的线性排序算法，对输入都有一些特定的要求（毕竟它们并不依赖于比较输入

##### counting sort 计数排序

输入都在0-k之间，如果k=O(n)，那么整个算法就会是theta(n)

因为知道范围，所以可以直接把数字放在应该在的地方

为了处理重复的数，一开始就用辅助数组去统计好0-k每一个数出现了多少次，然后依照这个去开辟结果数组，一个个处理输入数组的数，放在应该放的地方

##### radix sort 基数排序

used by card-sorting machines（非常远古

思想是按位数切割，然后比较每一位。

从个位（也就是最不重要的一位）开始比较并排序，然后是十位、百位......处理完所有的位数之后就完成了

对单独某一位的排序可以使用任意一个排序，但如果用了counting sort的话，需要注意的是内存消耗。如果内存很昂贵，那么不如用in-placement的那种算法，比如quicksort（quicksort能更好的利用cache之类的

##### bucket sort 桶排序

假设input均匀的分布在[0,1)里

n个元素，n个桶

桶中采用插入排序，插入排序的复杂度是常数E[n<sup>2</sup>]=V[n]+E<sup>2</sup>[n] = 1 - 1/n + 1<sup>2</sup> (服从二项分布)



## 网络



## 操作系统



## 图形学和shader相关（？

