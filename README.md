# verilog-code-for-fulladder
#using halfadder module instantiation on xilinx vivado software
module fulladderusinghalfadder(a,b,c,sum,carry );
    input a,b,c;
    output sum,carry;
    wire w1,w2,w3;
    halfadder h1(.a(a),.b(b),.sum(w1),.carry(w2));
    halfadder h2(.a(w1),.b(c),.sum(sum),.carry(w3));
    assign carry=w3|w2;
    
endmodule
