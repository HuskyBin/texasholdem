#### 要求和条件
- 给定任意两组牌, 每组5张, 能够输出两组牌的牌面及比较的结果.
- 使用52张扑克, 分为四个花色(将红桃, 方块, 黑桃, 梅花简化为A, B, C, D), 每个花色13张牌, 数字从2到14(将J, Q, K, A简化为11, 12, 13, 14).

#### 规则
1. 都是散牌的话, 比较各自五张牌中数字最大的
    - **例1: "B==11==, A2, A9, D10, A8" < "D4, A8, C5, C6, B==12=="**

2. 对子(两张牌数字相同)大于散牌
    - **例2: "B==14==, A3, A9, D10, A8" < "D4, A==2==, ==C2==, C6, B11"**

3. 都有对子则比较对子之间大小
    - **例3: "B11, ==A9==, D==9==, D5, A8" < "D4, B==10==, C==10==, C6, B12"**

4. 顺子(五张牌数字连续)大于对子
    - **例4: "D==2==, B==2==, C==10==, A==10==, B12" < "D==5==, A==6==, C==7==, C==8==, B==9=="**