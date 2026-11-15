# 两数相加

> 给你两个 **非空** 的链表，表示两个非负的整数。它们每位数字都是按照 **逆序** 的方式存储的，并且每个节点只能存储 **一位** 数字。
>
> 请你将两个数相加，并以相同形式返回一个表示和的链表。
>
> 你可以假设除了数字 0 之外，这两个数都不会以 0 开头。

我的代码：

```python
# Definition for singly-linked list.
# class ListNode(object):
#     def __init__(self, val=0, next=None):
#         self.val = val
#         self.next = next
class Solution(object):
    def addTwoNumbers(self, l1, l2):
        """
        :type l1: Optional[ListNode]
        :type l2: Optional[ListNode]
        :rtype: Optional[ListNode]
        """
        num1=self.read_listnode(l1)
        num2=self.read_listnode(l2)
        # 调用类方法记得加上self
        return self.set_listnode(num1+num2)
    def read_listnode(self,listnode):
        num_str=''
        while listnode!=None:
            num_str = num_str+str(listnode.val)
            listnode = listnode.next
        ls=list(num_str)
        ls.reverse()
        num_str=''.join(ls)
        # 反转数字
        return int(num_str)
    def set_listnode(self,num):
        ls_str = list(str(num))
        ls_str.reverse()
        cur=ListNode()
        listnode=ListNode()
        listnode.val=int(ls_str[0])
        if len(ls_str)>1:
            listnode.next=cur
        # reverse方法会反转列表本身返回的是none
            for i,_ in enumerate(ls_str[1:]):
                # enumerate可以直接给index和值
                cur.val=int(_)
                if i != len(ls_str[1:])-1:
                # 要判断这个是不是最后一个
                    cur.next=ListNode()
                    cur = cur.next
        return listnode
```

最快代码：

```python
# Definition for singly-linked list.
# class ListNode(object):
#     def __init__(self, val=0, next=None):
#         self.val = val
#         self.next = next
class Solution(object):
    def addTwoNumbers(self, l1, l2):
        """
        :type l1: Optional[ListNode]
        :type l2: Optional[ListNode]
        :rtype: Optional[ListNode]
        """
        dummy = ListNode(0)
        cur = dummy
        carry = 0
        while l1 or l2 or carry:
            x = l1.val if l1 else 0
            y = l2.val if l2 else 0
            total = x+y+carry
            carry = total//10
            digit = total%10
            cur.next = ListNode(digit)
            cur = cur.next
            if l1:
                l1 = l1.next
            if l2:
                l2 = l2.next
        return dummy.next
```

