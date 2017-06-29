* [496] In one array, find the first element which is larger than the current one:
>creat one stack and store the elements in decreasing order    

```
        for i in range(len(nums)):
            while rec and rec[-1]<nums[i]:
                rela[rec.pop()]=nums[i];
            rec.append(nums[i]);
```


* [232] [225] Switches between queue and stack
>create two lists and pop push elements between them
