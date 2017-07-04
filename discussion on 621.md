>my code;

the key is  
```
max((n+1)*(maxi-1)+count_maxi , len(tasks))
```
maxi is the maximum time of repeat, count_maxi is the number of elements repeat maxi times


```
class Solution(object):
    def leastInterval(self, tasks, n):
        """
        :type tasks: List[str]
        :type n: int
        :rtype: int
        """
        if len(tasks)==0:
            return 0;
        rec={};
        for ta in tasks:
            if rec.has_key(ta):
                rec[ta]+=1;
            else:
                rec[ta]=1;
        maxi=max(rec.values());
        count_maxi=0;
        for i in rec.values():
            if i ==maxi:
                count_maxi+=1;
        return max((n+1)*(maxi-1)+count_maxi , len(tasks))
```
