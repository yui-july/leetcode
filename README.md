# 链表LinkedList：

class ListNode:     #定义节点类

    def _init_(self,val):
      self.val = val
      self.next = None
    
# 解题方法：
   1.利用快慢指针（有时候需要三个指针）
   
   2.构建虚假链表头：
   prev =ListNode(0) 值为0的虚假链表头
   
     prev = None 将节点初始化为None
     
   先在纸上画出节点之间的关系和修改方法，再编码
   
# Attention：
   1.不论有没有头节点，头指针head都指向链表中的第一个节点
   
   2.操作时，注意考虑：
   
      （1）链表为空
      
      （2）链表仅有一个节点
      
      （3）头节点和尾节点的特殊情况
      
   3.注意考虑node.next和node.next.next是否有意义，即在调用next字段之前，始终检查节点是否为空；
   
   4.仔细定义循环的结束条件
   
   5.链表的公共节点指的是存的内存地址相同，而不是val值相同
   
   6.在快慢指针里，如果慢指针下一个位置是快指针的位置，则一定要先移动慢指针再移动快指针！【错误示范见题目“移除链表元素”】。或者用同时赋值也可以，即 fast, slow = fast.next, fast
