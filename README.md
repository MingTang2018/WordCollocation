# WordCollocation
Self complemented Word Collocation(词语搭配) using MI method which is tested to be effective..
# 原理  
互信息体现了两个变量之间的相互依赖程度。二元互信息是指两个事件相关性的量，互信息值越高, 表明X和Y相关性越高, 则X和Y 组成短语的可能性越大; 反之, 互信息值越低,X 和Y之间相关性越低, 则X 和Y之间存在短语边界的可能性越大。
# 用途
利用两个词语之间的相互依赖程度，能够求得一个词的常用搭配，可以有以下用途：  
1、为词语搭配知识库建设，可用于输入短语推荐  
2、词语语义刻画与表示提供帮助，若以搭配强度作为词-词矩阵的weight度量，可以用来计算两个词之间的相似度  
3、若给定历史语料库，可以通过历时搭配来监测词汇语义的变迁  
# 提取步骤
step 1/6: build corpus ..........  
step 2/6: compute worddict..........  
step 3/6: build cowords..........  
step 4/6: compute coinfos..........  
step 5/6: compute words mi..........  
step 6/6: save words mi..........  
# 输入与输出
1）输入：  
1、1W个文档，每个文档为一行，保存在'./data/data.txt'中  
2）输出：  
1、格式：(词语 制表符 搭配词1_搭配强度1,搭配词2_搭配强度2)    
2、结果保存，保存在'./data/resut.txt'中  
3）参数：
1、window_size: 默认为5， 左右窗口为5， 作为词共现窗口  
# 效果  
以1W个文档/句子作为训练语料，进行训练，得到结果举例如下：  
word:陷入  
word collocations Top 10:  
不由得@18.05618124455273  
两难@17.83378882321628  
林林总总@17.57075441738249  
不怎么@17.248826322495123  
误区@17.248826322495123  
市面上@17.248826322495123  
失落@16.386329846245058  
困境@15.83378882321628  
母亲@15.511860728328918  
常@15.471218743831571  

word:乐于  
word collocations Top 10:  
吃苦耐劳@19.57075441738249  
奉献@18.57075441738249  
事业心@18.57075441738249  
作风@18.248826322495123  
务实@17.418751323937435  
责任感@17.248826322495123  
Kevin@17.248826322495123  
政治素质@16.248826322495123  
热爱@15.959319705300139  
客户@15.734253149665365  

