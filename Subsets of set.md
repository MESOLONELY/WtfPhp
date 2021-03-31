## Leetcode 78: Subsets

Given an integer array set nums={1,2,3}, return all possible subsets.

「Mathematical induction」- 数学归纳法

Let all subsets of "nums" be "S(nums)"

Then 

- all subsets of "nums[1:]" be "S(nums[1:])"

- S(nums) = S(nums[1:]) + All sets in S(nums[1:]) add nums[0]

```Scheme
(define (subset nums) (if (null? nums) (list nil) (let ((rest (subset (cdr nums)))) (append rest (map (lambda (s) (append (list (car nums)) s)) rest )))))
```

```php
<?php

    function subsets($nums) {
        if (count($nums) == 0)
        {
            return [[]];
        }
        else
        {
            // Assume we are in a class, so use $this
            $rest = $this->subsets(array_slice($nums, 1));
            $copy = $rest;
            for ($key = 0, $maxkey = count($copy) - 1; $key <= $maxkey; ++$key)
            {
                $copy[$key] = array_merge($copy[$key], array($nums[0]));
            }
            
            return array_merge($rest, $copy);
        }
    }

>
```