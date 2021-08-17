### flex和fixed冲突的解决办法
在做静态布局的时候，使用flex进行布局，将页面结构搞好了，但一旦加上position: fixed定位后，就会出现图一情况。
尝试处理：给整个需要定位的结构添加一层父容器，在父容器中进行定位，子容器进行flex布局，但还是无法得到想要的效果
最终处理：仍给整个需要定位的结构添加一层父容器，并父容器定位，同时添加left: 0; right: 0;
![image](https://user-images.githubusercontent.com/55281287/129646831-1e3392d1-f197-40f1-93b6-68944daa4aed.png)
![image](https://user-images.githubusercontent.com/55281287/129646875-26aba4ed-0a8e-4fed-b437-394f65778677.png)
