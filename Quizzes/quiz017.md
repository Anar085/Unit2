# Quiz 017

## Paper solution
![quiz17s](https://github.com/user-attachments/assets/4d45de18-35f4-42c4-8cd6-491786662711)


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

![image](https://github.com/user-attachments/assets/535c6369-4c51-44db-902f-e531fd373299)

## Truth table and circuit

![quiz17](https://github.com/user-attachments/assets/4b7d2485-8f00-4fae-b73a-ded789503ed9)



