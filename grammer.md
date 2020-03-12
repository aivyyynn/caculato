//过程语句定义
program → block endword
block → {decls stmtis} 
decls → decls decl | ε
stmtis → stmtis stmti |ε
endword → stmt.
decl → int id; | float id;
stmti → stmt;
stmt → id = expr|  write(id)|  block
//表达式计算
expr → expr+term | expr-term | term
term → term*unary | term/unary | unary
//整数和浮点数
unary → num | id
num → intnum | floatnum
floatnum → intnum.(digit)*
intnum → digitz(digit)* | 0
//变量名定义
id → char(char|digit)*	
char → A|B|…|Z|a|b|…|z
digit → 0|1|…|9
digitz → 1|…|9
