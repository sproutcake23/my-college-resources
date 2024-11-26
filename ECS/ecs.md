#  And,Or,Not,Xor gates (with their 16 bit ver excluding Xor gate) using Nand gates
## CODE
### And gate using Nand gate 
```Auto
CHIP And {
    IN a, b;
    OUT out;
 
    PARTS:
    Nand(a=a,b=b,out=c);
    Nand(a=c,b=c,out=out);
}
```
### And16 gate using Nand gate 
```
CHIP And16 {
    IN a[16], b[16];
    OUT out[16];
    PARTS:
    Nand(a=a[0],b=b[0],out=out0);
    Nand(a=out0,b=out0,out=out[0]);
    Nand(a=a[1],b=b[1],out=out1);
    Nand(a=out1,b=out1,out=out[1]);
    Nand(a=a[2],b=b[2],out=out2);
    Nand(a=out2,b=out2,out=out[2]);
    Nand(a=a[3],b=b[3],out=out3);
    Nand(a=out3,b=out3,out=out[3]);
    Nand(a=a[4],b=b[4],out=out4);
    Nand(a=out4,b=out4,out=out[4]);
    Nand(a=a[5],b=b[5],out=out5);
    Nand(a=out5,b=out5,out=out[5]);
    Nand(a=a[6],b=b[6],out=out6);
    Nand(a=out6,b=out6,out=out[6]);
    Nand(a=a[7],b=b[7],out=out7);
    Nand(a=out7,b=out7,out=out[7]);
    Nand(a=a[8],b=b[8],out=out8);
    Nand(a=out8,b=out8,out=out[8]);
    Nand(a=a[9],b=b[9],out=out9);
    Nand(a=out9,b=out9,out=out[9]);
    Nand(a=a[10],b=b[10],out=out10);
    Nand(a=out10,b=out10,out=out[10]);
    Nand(a=a[11],b=b[11],out=out11);
    Nand(a=out11,b=out11,out=out[11]);
    Nand(a=a[12],b=b[12],out=out12);
    Nand(a=out12,b=out12,out=out[12]);
    Nand(a=a[13],b=b[13],out=out13);
    Nand(a=out1,b=out13,out=out[13]);
    Nand(a=a[14],b=b[14],out=out14);
    Nand(a=out14,b=out14,out=out[14]);
    Nand(a=a[15],b=b[15],out=out15);
    Nand(a=out15,b=out15,out=out[15]);
```
### Or gate using Nand gate 
```
CHIP Or {
    IN a, b;
    OUT out;

    PARTS:
    Nand(a=a,b=a,out=c);
    Nand(a=b,b=b,out=d);
    Nand(a=c,b=d,out=out);
}
```
### Or16 gate using Nand gate 
```
CHIP Or16 {
    IN a[16], b[16];
    OUT out[16];

    PARTS:
    Nand(a=a[0],b=a[0],out=outq0);
    Nand(a=b[0],b=b[0],out=outp0);
    Nand(a=outq0,b=outp0,out=out[0]);
    Nand(a=a[1],b=a[1],out=outq1);
    Nand(a=b[1],b=b[1],out=outp1);
    Nand(a=outq1,b=outp1,out=out[1]);
    Nand(a=a[2],b=a[2],out=outq2);
    Nand(a=b[2],b=b[2],out=outp2);
    Nand(a=outq2,b=outp2,out=out[2]);
    Nand(a=a[3],b=a[3],out=outq3);
    Nand(a=b[3],b=b[3],out=outp3);
    Nand(a=outq3,b=outp3,out=out[3]);
    Nand(a=a[4],b=a[4],out=outq4);
    Nand(a=b[4],b=b[4],out=outp4);
    Nand(a=outq4,b=outp4,out=out[4]);
    Nand(a=a[5],b=a[5],out=outq5);
    Nand(a=b[5],b=b[5],out=outp5);
    Nand(a=outq5,b=outp5,out=out[5]);
    Nand(a=a[6],b=a[6],out=outq6);
    Nand(a=b[6],b=b[6],out=outp6);
    Nand(a=outq6,b=outp6,out=out[6]);
    Nand(a=a[7],b=a[7],out=outq7);
    Nand(a=b[7],b=b[7],out=outp7);
    Nand(a=outq7,b=outp7,out=out[7]);
    Nand(a=a[8],b=a[8],out=outq8);
    Nand(a=b[8],b=b[8],out=outp8);
    Nand(a=outq8,b=outp8,out=out[8]);
    Nand(a=a[9],b=a[9],out=outq9);
    Nand(a=b[9],b=b[9],out=outp9);
    Nand(a=outq9,b=outp9,out=out[9]);
    Nand(a=a[10],b=a[10],out=outq10);
    Nand(a=b[10],b=b[10],out=outp10);
    Nand(a=outq10,b=outp10,out=out[10]);
    Nand(a=a[11],b=a[11],out=outq11);
    Nand(a=b[11],b=b[11],out=outp11);
    Nand(a=outq11,b=outp11,out=out[11]);
    Nand(a=a[12],b=a[12],out=outq12);
    Nand(a=b[12],b=b[12],out=outp12);
    Nand(a=outq12,b=outp12,out=out[12]);
    Nand(a=a[13],b=a[13],out=outq13);
    Nand(a=b[13],b=b[13],out=outp13);
    Nand(a=outq13,b=outp13,out=out[13]);
    Nand(a=a[14],b=a[14],out=outq14);
    Nand(a=b[14],b=b[14],out=outp14);
    Nand(a=outq14,b=outp14,out=out[14]);
    Nand(a=a[15],b=a[15],out=outq15);
    Nand(a=b[15],b=b[15],out=outp15);
    Nand(a=outq15,b=outp15,out=out[15]);
}
```
### Not gate using Nand gate 
```
CHIP Not {
    IN in;
    OUT out;

    PARTS:
    Nand(a=in,b=in,out=out);
}

```
### Not16 gate using Nand gate
```
CHIP Not16 {
    IN in[16];
    OUT out[16];

    PARTS:
    Nand(a=in[0],b=in[0],out=out[0]);
    Nand(a=in[1],b=in[1],out=out[1]);
    Nand(a=in[2],b=in[2],out=out[2]);
    Nand(a=in[3],b=in[3],out=out[3]);
    Nand(a=in[4],b=in[4],out=out[4]);
    Nand(a=in[5],b=in[5],out=out[5]);
    Nand(a=in[6],b=in[6],out=out[6]);
    Nand(a=in[7],b=in[7],out=out[7]);
    Nand(a=in[8],b=in[8],out=out[8]);
    Nand(a=in[9],b=in[9],out=out[9]);
    Nand(a=in[10],b=in[10],out=out[10]);
    Nand(a=in[11],b=in[11],out=out[11]);
    Nand(a=in[12],b=in[12],out=out[12]);
    Nand(a=in[13],b=in[13],out=out[13]);
    Nand(a=in[14],b=in[14],out=out[14]);
    Nand(a=in[15],b=in[15],out=out[15]);
 
}
```
### Xor gate using Nand gate 
```
CHIP Xor {
    IN a, b;
    OUT out;

    PARTS:
    Nand(a=a,b=b,out=c);
    Nand(a=a,b=c,out=d);
    Nand(a=c,b=b,out=e);
    Nand(a=d,b=e,out=out);
}
```
# Virtual lab (digital electronics) exp -1 , exp - 4 , exp -11
## CODE
### Do these experiments in this website
> 📌
> [https://de-iitr.vlabs.ac.in/](https://de-iitr.vlabs.ac.in/)

# Nand2Tetris project 2 half adder and full adder and add 16
## Half Adder code
```
CHIP HalfAdder {
    IN a, b;    // 1-bit inputs
    OUT sum,    // Right bit of a + b 
        carry;  // Left bit of a + b

    PARTS:
    Xor(a=a,b=b,out=sum);
    And(a=a,b=b,out=carry);
}
```
## Full Adder code
```
CHIP FullAdder {
    IN a, b, c;  // 1-bit inputs
    OUT sum,     // Right bit of a + b + c
        carry;   // Left bit of a + b + c

    PARTS:
    HalfAdder(a=a,b=b,sum=s1,carry=carry1);
    HalfAdder(a=s1,b=c,sum=sum,carry=carry2);
    Or(a=carry1,b=carry2,out=carry);
}
```
# Mux and Demux (with mux 16 bit)
### Mux code
```
CHIP Mux {
    IN a, b, sel;
    OUT out;

    PARTS:
    Not(in=sel,out=notsel);
    And(a=a,b=notsel,out=out1); 
    And(a=b,b=sel,out=out2);
    Or(a=out1,b=out2,out=out); 
}
```
### Mux16 code
```
CHIP Mux16 {
    IN a[16], b[16], sel;
    OUT out[16];

    PARTS:
    Mux(a=a[0],b=b[0],sel=sel,out=out[0]);
    Mux(a=a[1],b=b[1],sel=sel,out=out[1]);
    Mux(a=a[2],b=b[2],sel=sel,out=out[2]);
    Mux(a=a[3],b=b[3],sel=sel,out=out[3]);
    Mux(a=a[4],b=b[4],sel=sel,out=out[4]);
    Mux(a=a[5],b=b[5],sel=sel,out=out[5]);
    Mux(a=a[6],b=b[6],sel=sel,out=out[6]);
    Mux(a=a[7],b=b[7],sel=sel,out=out[7]);
    Mux(a=a[8],b=b[8],sel=sel,out=out[8]);
    Mux(a=a[9],b=b[9],sel=sel,out=out[9]);
    Mux(a=a[10],b=b[10],sel=sel,out=out[10]);
    Mux(a=a[11],b=b[11],sel=sel,out=out[11]);
    Mux(a=a[12],b=b[12],sel=sel,out=out[12]);
    Mux(a=a[13],b=b[13],sel=sel,out=out[13]);
    Mux(a=a[14],b=b[14],sel=sel,out=out[14]);
    Mux(a=a[15],b=b[15],sel=sel,out=out[15]);   
}
```
### Demux code 
```
CHIP DMux {
    IN in, sel;
    OUT a, b;

    PARTS:
    Not(in=sel, out=notsel);
    And(a=in, b=notsel, out=a);
    And(a=sel, b=in, out=b);
}
```
