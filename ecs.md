- Nand2Tetris project 2 half adder and full adder and add 16
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
	```- Mux and Demux (with mux 16 bit)
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















**YOU**** ARE**** PROHIBITED**** FROM**** ****I****N****F**** ****G**** ****T****H****I****S**** ****M****ATO THE **
