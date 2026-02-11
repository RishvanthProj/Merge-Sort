This method merges two sorted arrays into nums1 in-place.

nums1 has size m + n.
First m elements are valid.
nums2 has n elements.

Instead of merging from the front (which would overwrite data), we merge from the back.

Core idea:

We use three pointers.

p1 → last valid element in nums1
p2 → last element in nums2
i → last index of nums1 (total space)

Now we compare from the end.

If nums1[p1] > nums2[p2]
→ put nums1[p1] at index i
→ move p1 backward

Else
→ put nums2[p2] at index i
→ move p2 backward

After placing, decrease i.

We continue until all elements of nums2 are placed.

Why only check p2 >= 0?

If nums2 finishes first, nums1 elements are already in correct position.
If nums1 finishes first, we still need to copy remaining nums2 elements.

Time Complexity:
O(m + n)

Space Complexity:
O(1) (in-place, no extra array)

In one line for placement:

“This algorithm uses a two-pointer approach from the end to merge two sorted arrays in-place without extra space, achieving O(m+n) time complexity.”

That’s crisp enough to impress and simple enough to remember.

And here’s the deeper pattern:
Whenever a problem says “merge sorted” and “in-place,” think backward traversal. That mental trigger alone wins interviews.
