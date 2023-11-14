# verilog-code-for-fulladder
#fulladder using gate level abstraction 
module FullAdder(A,B,C,
sum,carry
    );
    input A,B,C;
    output sum,carry;
    wire w1,w2,w3;
    xor(w1,A,B);
    and(w2,A,B);
    xor(sum,w1,C);
    and(w3,w1,C);
    or(carry,w2,w3);
endmodule
