# Quiz 018

## Paper solution
![quiz18](https://github.com/user-attachments/assets/a6f2914e-1ea0-414b-8c30-608e5ad865d8)


## Code
```.py
def get_truth():
    print(f"| A | B | C | AB + not B + not BC |")
    A,B,C=0,0,0
    out=""
    for i in range(8):
        C= not C
        if i %2==0:
            B= not B
        if i %4==0:
            A= not A
        out=f"| {A} | {B} | {C} |          {(((int(A) and int(B)) or (not int(B))) or ((not (int(B))) and int(C)))}          |\n"+out
        out=out.replace("False","0")
        out=out.replace("True","1")
    return out
m=get_truth()
print(m)

```

## Proof of work

![image](https://github.com/user-attachments/assets/7a94e1e6-d9cd-4352-ba5a-1e39e8eedc4d)


## Truth table and circuit for: X = ZW ⨁ (Z ⨁ Y(not W))

![quiz18s](https://github.com/user-attachments/assets/96b10990-77c7-4400-8cf1-d665ec3c31c0)



