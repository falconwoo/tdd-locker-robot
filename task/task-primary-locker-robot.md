Primary Locker Robot业务需求：作为一个初级储物柜机器人，我能够按储物柜的顺序来存包，也能取包

# Tasking 

Given 机器人管理2个储物柜，柜子剩余空间都是2；
When 通过机器人存入1个包；
Then 存包成功，返回票据，包被存入第1个储物柜

Given 机器人管理2个储物柜，第1个柜子已满，第2个柜子剩余空间为2；
When 通过机器人存入1个包；
Then 存包成功，返回票据，包被存入第2个储物柜

Given 机器人管理2个储物柜，柜子都满了；
When 通过机器人存入1个包；
Then 存包失败，提示储物柜已满

Given 机器人管理2个储物柜，通过机器人把1个包存入第1个储物柜，获得了票据；
When 通过机器人使用票据取包；
Then 取包成功，返回存入的包

Given 机器人管理2个储物柜，通过机器人把1个包存入第2个储物柜，获得了票据；
When 通过机器人使用票据取包；
Then 取包成功，返回存入的包

Given 机器人管理2个储物柜，1张伪造票据；
When 通过机器人使用票据取包；
Then 取包失败，提示无效票据