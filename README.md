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

