---
id: 0rkuaamivqueqom5nhzhls6
title: Sort
desc: ''
updated: 1710759099580
created: 1710758955471
---
- Sorts the input *line by line*

```bash
❯ echo -e "2\n1\n0\n3\n5\n6" | sort
0
1
2
3
5
6
```

**Sorting the file:**
```bash
❯ cat newfile.md 
Shyam
Ram
Dev
Shubh
Puneet
Gurmeet

❯ sort newfile.md 
Dev
Gurmeet
Puneet
Ram
Shubh
Shyam
```

> It doesn't make changes to the file, it simply outputs

