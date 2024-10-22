# Quiz 018

## Paper solution


## Code
```.py
def get_truth():
    print(f"| A | B | C |")
    A,B,C=0,0,0
    out=""
    for i in range(8):
        C= not C
        if i %2==0:
            B= not B
        if i %4==0:
            A= not A
        out=f"| {A} | {B} | {C} |\n"+out
        out=out.replace("False","0")
        out=out.replace("True","1")
    return out
m=get_truth()
print(m)

```

## Proof of work







