Locker业务需求：储物柜可以存包、取包

# Tasking 

Given 1个容量为2的储物柜；When 存入1个包；Then 存包成功，返回票据

Given 1个已经装满的储物柜；When 存入1个包；Then 存包失败，提示储物柜已满

Given 1个包已经存入储物柜，获得了票据；When 使用票据取包；Then 取包成功，返回存入的包

Given 1张已经从储物柜取过包的票据；When 使用票据取包；Then 取包失败，提示无效票据

Given 1张伪造票据；When 使用票据取包；Then 取包失败，提示无效票据