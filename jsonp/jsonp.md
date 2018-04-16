# jsonp原理和实现
>Jsonp(JSON with Padding) 是 json 的一种"使用模式"，可以让网页从别的域名（网站）那获取资料，即跨域读取数据。

发送的并不是 ajax 请求，而是利用动态创建 script 标签，没有同源限制，把src指向服务端地址。



封装promis方法


首先，安装jsonp
```
npm i --save jsonp
```
jsonp的封装
```
import originJSONP from 'jsonp'

//暴露一个方法
export default function jsonp(url,data,option){
  url += (url.indexOf('?')<0 ? '?' : '&') + param(data)
  //如果url没有问号就添加上 否则就是&
  return new Promise((resolve,reject)=>{
    originJSONP(url,option,(err,data)=>{
      if(!err){
        resolve(data)
      }else{
        reject(err)
      }
    })
  })
}

function param(data){
  let url = ''
  for (var i in data) {
    let value = data[i] !== undefined? data[i] : ''
    url += `&${i}=${encodeRIComponent(value)}` //url的拼接
  }
  return url ? url.substring(1) : '' //url有data就去掉第一个&
}
```
