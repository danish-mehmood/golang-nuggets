# golang-nuggets
### ⭐  a repository containing golang features which are little known but are very useful , all the ***tricks*** 🪄 and ***tips*** and ***syntactic sugar*** i manage to find during my day to day work will be added here ⭐
### 🖱️ this repo is open to contributions 💻 , please feel free to create pull requests 🙏🏻🙏🏻🙏🏻🙏🏻


![alt text](https://github.com/danish-mehmood/golang-nuggets/blob/main/gopher.png)





##### 1 - Make an incomparable type yourself :
```golang
   type incomparable [0]func()
```
- this will only work for `==` operator when this type of variables are compared , a compile time error will be thrown
- it was declared as a zero size array so that no memory footprint is added on 
- [real world use ](https://github.com/golang/go/blob/master/src/net/http/http.go#L22)
- [more info](https://stackoverflow.com/questions/71031243/how-does-type-donotcompare-0func-prevent-comparability-in-golang)

##### 2 - How to think about golang `<<` and `>>` shift operators :
- there is a good mental model to make sense of these operators without doing many calculations in head
- ***n << 1*** would yield n multiplied by 2 (8 << 1 = 16)
- and ***n >> 1*** would yield n divided by 2 (8 >> 1 = 4)
- if we extrapolate , ***n << m*** would yield n multiplied by  2 m times (8 << 2 = 32)
- and ***n >> m*** would yield n divided by 2 m times (8 >> 2 = 2)
