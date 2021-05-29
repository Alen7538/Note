cin>>s：不能读取空格，遇到多个空格会分割导致后续字符串丢失

getline(cin,s)：能读取含有空格的字符串

结构体排序sort(stu，stu+n，compare) ：从stu第一个开始到stu+n结束，compare位自己定义的排序方法，返回类型位bool

数组初始化：memset(array，初值，sizeof(array))，需要引入头文件cstring

保留小数点后n位：头文件#include<iomanip>

​								 one---cout<<setiosflags(ios::fixed)<<setprecision(2);

​								 two---cout.setf(ios::fixed);

​											cout<<setprecision(2);

​								 three---cout<<fixed<<setprecision(2);

删除字符串第一个字符：ans.erase(ans.begin());

STL二分查找：查找的是arr[i+1]~arr[n-1]中的数，当前位于arr[i]；

​						  upper_bound  找到第一个大于该数的下标  使用:int index = upper_bound(arr+i+1,arr+n,'对比的数')-arr;

​						  lower_bound  找到第一个小于该数的下标  使用:int index = lower_bound(arr+i+1,arr+n,'对比的数')-arr;

```c++
//stl转换字符串的大小写
transform(su.begin(), su.end(), su.begin(), ::toupper);
```

isalpha：判断一个字符是否为字母，如果是字符则返回非零，否则返回零。

isalnum：判断一个字符是否为数字或者字母，也就是说判断一个字符是否属于a~z||A~Z||0~9

islower：判断一个字符是否为小写字母，也就是是否属于a~z。

isupper：判断一个字符是否为大写字母。

tolower()函数是把字符串都转化为小写字母

```c++
string str= "THIS IS A STRING";
for (int i=0; i <str.size(); i++)
   str[i] = tolower(str[i]);
```

toupper()函数是把字符串都转化为小写字母

```c++
string str= "hahahahaha";
for (int i=0; i <str.size(); i++)
   str[i] = toupper(str[i]);
```

map遍历，second表示取map中的value，first表示取map的key

```c++
        for(auto& a:mp){
            ans=max(ans,a.second);
        }
```

取二进制末位的值

```c++
1、(n>>1)&1：右移一位与1相与
2、(n&1)：直接与1相与
```

