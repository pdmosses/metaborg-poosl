---
title: ExprStat.sdf3
hide:
  - toc
---

# `ExprStat.sdf3`

:simple-github: [pdmosses/metaborg-poosl/org.metaborg.lang.poosl/syntax/ExprStat.sdf3]

[pdmosses/metaborg-poosl/org.metaborg.lang.poosl/syntax/ExprStat.sdf3]: https://github.com/pdmosses/metaborg-poosl/blob/master/org.metaborg.lang.poosl/syntax/ExprStat.sdf3 "The source file on GitHub"

<div class="sdf3"><table class="highlighttable"><tbody><tr><td class="linenos"><div class="linenodiv"><pre><span></span>1
2
3
4
5
6
7
8
9
10
11
12
13
14
15
16
17
18
19
20
21
22
23
24
25
26
27
28
29
30
31
32
33
34
35
36
37
38
39
40
41
42
43
44
45
46
47
48
49
50
51
52
53
54
55
56
57
58
59
60
61
62
63
64
65
66
67
68
69
70
71
72
73
74
75
76
77
78
79
80
81
82
83
84
85
86
87
88
89
90
91
92
93
94
95
96
97
98
99
100
101
102
103
104
105
106
107
108
109
110
111
112
113
114
115
116
117
118
119
120
121
122
123
124
125
126
127
128
129
130
131
132
133
134
135
136
137
138
139
140
141
142
143
144
145
146
147
148
149
150
151
152
153
154
155
156
157
158
159
160
161
162
163
164
165
166
167
168
169
170
171
172
173
174
175
176
177
178
179
180
181
182
183
184
185
186
187
188
189
190
191
192
193
194
195
196
197
198
199
200
201
202
203
204
205
206
207
208
209
210
211
212
213
214
215
216
217
218
219
220
221
222
223
224
225
226
227
228
229
230
231
232
233
234
235
236
237
238
239
240
241
242
243
244
245
246
247
248
249
250
251
252
253
254
255
256
257
258
259
260
261
262
263
264
265
266
267
268
269
270
271
272
273
274
275
276
277
278
</pre></div></td>
<td class="code"><pre><code><span class="keyword">module</span> <a href="../Stratego-Poosl.sdf3#ExprStat_166_174" id="ExprStat_7_15" title="Referenced at ../Stratego-Poosl.sdf3 line 11">ExprStat</a>

<span class="keyword">imports</span>
    <a href="../Common.sdf3#Common_7_13" id="Common_29_35" title="Defined at ../Common.sdf3 line 1">Common</a>

<span class="keyword">context-free sorts</span>
    <a href="#Statement_3000_3009" id="Statement_60_69" title="Referenced at line 118; ../Poosl.sdf3 line 153">Statement</a>
    <a href="#SingleStatement_7768_7783" id="SingleStatement_74_89" title="Referenced at line 231">SingleStatement</a>
    <a href="#AndStatement_1223_1235" id="AndStatement_94_106" title="Referenced at line 57">AndStatement</a>
    <a href="#OrStatement_1412_1423" id="OrStatement_111_122" title="Referenced at line 64">OrStatement</a>
    <a href="#ProcessMethodCall_1312_1329" id="ProcessMethodCall_127_144" title="Referenced at line 60; ../Poosl.sdf3 line 144">ProcessMethodCall</a>
    <a href="#CaseStatementList_2303_2320" id="CaseStatementList_149_166" title="Referenced at line 94">CaseStatementList</a>
    <a href="#CaseStatement_2813_2826" id="CaseStatement_171_184" title="Referenced at line 112">CaseStatement</a>
    <a href="#OptDefaultStatement_2335_2354" id="OptDefaultStatement_189_208" title="Referenced at line 95">OptDefaultStatement</a>

    <a href="#Expression_6479_6489" id="Expression_214_224" title="Referenced at line 202; ../Poosl.sdf3 line 198">Expression</a>
    <a href="#SingleExpression_8348_8364" id="SingleExpression_229_245" title="Referenced at line 243">SingleExpression</a>
    <a href="#OnSuperClass_4322_4334" id="OnSuperClass_250_262" title="Referenced at line 145">OnSuperClass</a>
    <a href="#OptExpressionList_4341_4358" id="OptExpressionList_267_284" title="Referenced at line 145">OptExpressionList</a>
    <a href="#OptVariableList_1673_1688" id="OptVariableList_289_304" title="Referenced at line 69">OptVariableList</a>
    <a href="#ExpressionList_2576_2590" id="ExpressionList_309_323" title="Referenced at line 101">ExpressionList</a>
    <a href="#CaseExpressionList_4955_4973" id="CaseExpressionList_328_346" title="Referenced at line 167">CaseExpressionList</a>
    <a href="#CaseExpression_6286_6300" id="CaseExpression_351_365" title="Referenced at line 196">CaseExpression</a>
    <a href="#OptDefaultExpression_4988_5008" id="OptDefaultExpression_370_390" title="Referenced at line 168">OptDefaultExpression</a>
    <a href="#ExpressionConstant_5235_5253" id="ExpressionConstant_395_413" title="Referenced at line 174; ../Poosl.sdf3 line 67">ExpressionConstant</a>
    <a href="#UnaryOperator_7517_7530" id="UnaryOperator_418_431" title="Referenced at line 227; ../Poosl.sdf3 line 101">UnaryOperator</a>
    <a href="#BinaryOperatorLevel2_3927_3947" id="BinaryOperatorLevel2_436_456" title="Referenced at line 141; ../Poosl.sdf3 line 110">BinaryOperatorLevel2</a>
    <a href="#BinaryOperatorLevel3_4050_4070" id="BinaryOperatorLevel3_461_481" title="Referenced at line 142; ../Poosl.sdf3 line 111">BinaryOperatorLevel3</a>
    <a href="#BinaryOperatorLevel4_4173_4193" id="BinaryOperatorLevel4_486_506" title="Referenced at line 143; ../Poosl.sdf3 line 112">BinaryOperatorLevel4</a>
    <a href="#VariableList_2592_2604" id="VariableList_511_523" title="Referenced at line 101">VariableList</a>
    <a href="#OptPostExpression_1715_1732" id="OptPostExpression_528_545" title="Referenced at line 69">OptPostExpression</a>
    <a href="#OptReceptionCondition_1691_1712" id="OptReceptionCondition_550_571" title="Referenced at line 69">OptReceptionCondition</a>

<span class="keyword">context-free syntax</span>

    <span class="layout">// === Statements =======</span>

    <a href="#Statement_3000_3009" id="Statement_629_638" title="Referenced at line 118; ../Poosl.sdf3 line 153">Statement</a>.<span class="cons_Constructor"><span id="StatementSequence_639_656" title="Not referenced locally, nor via imports">StatementSequence</span></span> =                   [[{<a href="#SingleStatement_74_89" id="SingleStatement_680_695" title="Defined at line 8, 40, 46, 47, 48, 54, 60, 61, 67, 68, 69, 70, 75, 82, 87, 92, 98, 99">SingleStatement</a> <span class="cons_Lit">";\n"</span>}+]]

    <a href="#SingleStatement_7768_7783" id="SingleStatement_711_726" title="Referenced at line 231">SingleStatement</a>.<span class="cons_Constructor"><span id="AbortStatement_727_741" title="Not referenced locally, nor via imports">AbortStatement</span></span> = [
        <span class="cons_String">abort</span>
            [<a href="#Statement_60_69" id="Statement_773_782" title="Defined at line 7, 38">Statement</a>]
        <span class="cons_String">with</span>
            [<a href="#SingleStatement_74_89" id="SingleStatement_810_825" title="Defined at line 8, 40, 46, 47, 48, 54, 60, 61, 67, 68, 69, 70, 75, 82, 87, 92, 98, 99">SingleStatement</a>]
        ]
    <a href="#SingleStatement_7768_7783" id="SingleStatement_841_856" title="Referenced at line 231">SingleStatement</a>.<span class="cons_Constructor"><span id="DelayStatement_857_871" title="Not referenced locally, nor via imports">DelayStatement</span></span> =                [<span class="cons_String">delay</span> [<a href="#SingleExpression_229_245" id="SingleExpression_897_913" title="Defined at line 17, 138, 139, 141, 142, 143, 145, 147, 148, 153, 160, 165, 172, 173, 174, 175, 176, 177">SingleExpression</a>]]
    <a href="#SingleStatement_7768_7783" id="SingleStatement_920_935" title="Referenced at line 231">SingleStatement</a>.<span class="cons_Constructor"><span id="GuardedStatement_936_952" title="Not referenced locally, nor via imports">GuardedStatement</span></span> =              &lt;<span class="cons_String">[</span>&lt;<a href="#Expression_214_224" id="Expression_971_981" title="Defined at line 16, 135">Expression</a>&gt;<span class="cons_String">]</span> &lt;<a href="#SingleStatement_74_89" id="SingleStatement_985_1000" title="Defined at line 8, 40, 46, 47, 48, 54, 60, 61, 67, 68, 69, 70, 75, 82, 87, 92, 98, 99">SingleStatement</a>&gt;&gt;
    <a href="#SingleStatement_7768_7783" id="SingleStatement_1007_1022" title="Referenced at line 231">SingleStatement</a>.<span class="cons_Constructor"><span id="InterruptStatement_1023_1041" title="Not referenced locally, nor via imports">InterruptStatement</span></span> = [
        <span class="cons_String">interrupt</span>
            [<a href="#Statement_60_69" id="Statement_1077_1086" title="Defined at line 7, 38">Statement</a>]
        <span class="cons_String">with</span>
            [<a href="#SingleStatement_74_89" id="SingleStatement_1114_1129" title="Defined at line 8, 40, 46, 47, 48, 54, 60, 61, 67, 68, 69, 70, 75, 82, 87, 92, 98, 99">SingleStatement</a>]
        ]
    <a href="#SingleStatement_7768_7783" id="SingleStatement_1145_1160" title="Referenced at line 231">SingleStatement</a>.<span class="cons_Constructor"><span id="ParStatement_1161_1173" title="Not referenced locally, nor via imports">ParStatement</span></span> = [
        <span class="cons_String">par</span>
            [<a href="#Statement_60_69" id="Statement_1203_1212" title="Defined at line 7, 38">Statement</a>]
        [<a href="#AndStatement_94_106" id="AndStatement_1223_1235" title="Defined at line 9, 103">AndStatement</a>+]
        <span class="cons_String">rap</span>
        ]
    <a href="#SingleStatement_7768_7783" id="SingleStatement_1264_1279" title="Referenced at line 231">SingleStatement</a>.<span class="cons_Constructor"><span id="ProcessMethodCallStatement_1280_1306" title="Not referenced locally, nor via imports">ProcessMethodCallStatement</span></span> =    <a href="#ProcessMethodCall_127_144" id="ProcessMethodCall_1312_1329" title="Defined at line 11, 101">ProcessMethodCall</a>
    <a href="#SingleStatement_7768_7783" id="SingleStatement_1334_1349" title="Referenced at line 231">SingleStatement</a>.<span class="cons_Constructor"><span id="SelStatement_1350_1362" title="Not referenced locally, nor via imports">SelStatement</span></span> = [
        <span class="cons_String">sel</span>
            [<a href="#Statement_60_69" id="Statement_1392_1401" title="Defined at line 7, 38">Statement</a>]
        [<a href="#OrStatement_111_122" id="OrStatement_1412_1423" title="Defined at line 10, 107">OrStatement</a>+]
        <span class="cons_String">les</span>
        ]
    <a href="#SingleStatement_7768_7783" id="SingleStatement_1452_1467" title="Referenced at line 231">SingleStatement</a>.<span class="cons_Constructor"><span id="SkipStatement_1468_1481" title="Not referenced locally, nor via imports">SkipStatement</span></span> =                 [<span class="cons_String">skip</span>]
    <a href="#SingleStatement_7768_7783" id="SingleStatement_1511_1526" title="Referenced at line 231">SingleStatement</a>.<span class="cons_Constructor"><span id="SendStatement_1527_1540" title="Not referenced locally, nor via imports">SendStatement</span></span> =                 [[<a href="#ID_8421_8423" id="ID_1561_1563" title="Defined at line 246, 247, 248, 249, 251, 252, 253, 255, 256, 257, 259, 260, 261, 263, 264, 265, 267, 268, 269, 271, 272, 274, 275, 276, 277, 278">ID</a>]<span class="cons_String">!</span>[<a href="#ID_8421_8423" id="ID_1566_1568" title="Defined at line 246, 247, 248, 249, 251, 252, 253, 255, 256, 257, 259, 260, 261, 263, 264, 265, 267, 268, 269, 271, 272, 274, 275, 276, 277, 278">ID</a>][<a href="#OptExpressionList_267_284" id="OptExpressionList_1570_1587" title="Defined at line 19, 191, 192">OptExpressionList</a>] [<a href="#OptPostExpression_528_545" id="OptPostExpression_1590_1607" title="Defined at line 31, 121, 122">OptPostExpression</a>]]
    <a href="#SingleStatement_7768_7783" id="SingleStatement_1614_1629" title="Referenced at line 231">SingleStatement</a>.<span class="cons_Constructor"><span id="ReceiveStatement_1630_1646" title="Not referenced locally, nor via imports">ReceiveStatement</span></span> =              [[<a href="#ID_8421_8423" id="ID_1664_1666" title="Defined at line 246, 247, 248, 249, 251, 252, 253, 255, 256, 257, 259, 260, 261, 263, 264, 265, 267, 268, 269, 271, 272, 274, 275, 276, 277, 278">ID</a>]<span class="cons_String">?</span>[<a href="#ID_8421_8423" id="ID_1669_1671" title="Defined at line 246, 247, 248, 249, 251, 252, 253, 255, 256, 257, 259, 260, 261, 263, 264, 265, 267, 268, 269, 271, 272, 274, 275, 276, 277, 278">ID</a>][<a href="#OptVariableList_289_304" id="OptVariableList_1673_1688" title="Defined at line 20, 127, 128">OptVariableList</a>] [<a href="#OptReceptionCondition_550_571" id="OptReceptionCondition_1691_1712" title="Defined at line 32, 124, 125">OptReceptionCondition</a>] [<a href="#OptPostExpression_528_545" id="OptPostExpression_1715_1732" title="Defined at line 31, 121, 122">OptPostExpression</a>]]
    <a href="#SingleStatement_7768_7783" id="SingleStatement_1739_1754" title="Referenced at line 231">SingleStatement</a>.<span class="cons_Constructor"><span id="IfThenStatement_1755_1770" title="Not referenced locally, nor via imports">IfThenStatement</span></span> = [
        <span class="cons_String">if</span> [<a href="#Expression_214_224" id="Expression_1787_1797" title="Defined at line 16, 135">Expression</a>] <span class="cons_String">then</span> 
            [<a href="#Statement_60_69" id="Statement_1818_1827" title="Defined at line 7, 38">Statement</a>]
        <span class="cons_String">fi</span>
        ]
    <a href="#SingleStatement_7768_7783" id="SingleStatement_1854_1869" title="Referenced at line 231">SingleStatement</a>.<span class="cons_Constructor"><span id="IfThenElseStatement_1870_1889" title="Not referenced locally, nor via imports">IfThenElseStatement</span></span> = [
        <span class="cons_String">if</span> [<a href="#Expression_214_224" id="Expression_1906_1916" title="Defined at line 16, 135">Expression</a>] <span class="cons_String">then</span>
            [<a href="#Statement_60_69" id="Statement_1936_1945" title="Defined at line 7, 38">Statement</a>]
        <span class="cons_String">else</span>
            [<a href="#Statement_60_69" id="Statement_1973_1982" title="Defined at line 7, 38">Statement</a>]
        <span class="cons_String">fi</span>
        ]
    <a href="#SingleStatement_7768_7783" id="SingleStatement_2009_2024" title="Referenced at line 231">SingleStatement</a>.<span class="cons_Constructor"><span id="RoundBracketStatement_2025_2046" title="Not referenced locally, nor via imports">RoundBracketStatement</span></span> = [
        <span class="cons_String">(</span>
            [<a href="#Statement_60_69" id="Statement_2074_2083" title="Defined at line 7, 38">Statement</a>]
        <span class="cons_String">)</span>
        ]
    <a href="#SingleStatement_7768_7783" id="SingleStatement_2109_2124" title="Referenced at line 231">SingleStatement</a>.<span class="cons_Constructor"><span id="WhileStatement_2125_2139" title="Not referenced locally, nor via imports">WhileStatement</span></span> = [
        <span class="cons_String">while</span> [<a href="#Expression_214_224" id="Expression_2159_2169" title="Defined at line 16, 135">Expression</a>] <span class="cons_String">do</span>
            [<a href="#Statement_60_69" id="Statement_2187_2196" title="Defined at line 7, 38">Statement</a>]
        <span class="cons_String">od</span>
        ]
    <a href="#SingleStatement_7768_7783" id="SingleStatement_2223_2238" title="Referenced at line 231">SingleStatement</a>.<span class="cons_Constructor"><span id="SwitchStatement_2239_2254" title="Not referenced locally, nor via imports">SwitchStatement</span></span> = [
        <span class="cons_String">switch</span> [<a href="#Expression_214_224" id="Expression_2275_2285" title="Defined at line 16, 135">Expression</a>] <span class="cons_String">do</span>
            [<a href="#CaseStatementList_149_166" id="CaseStatementList_2303_2320" title="Defined at line 12, 112">CaseStatementList</a>]
            [<a href="#OptDefaultStatement_189_208" id="OptDefaultStatement_2335_2354" title="Defined at line 14, 116, 119">OptDefaultStatement</a>]
        <span class="cons_String">od</span>
        ]
    <a href="#SingleStatement_7768_7783" id="SingleStatement_2381_2396" title="Referenced at line 231">SingleStatement</a>.<span class="cons_Constructor"><a href="#ExpressionStatement_7784_7803" id="ExpressionStatement_2397_2416" title="Referenced at line 231">ExpressionStatement</a></span> =           <a href="#SingleExpression_229_245" id="SingleExpression_2429_2445" title="Defined at line 17, 138, 139, 141, 142, 143, 145, 147, 148, 153, 160, 165, 172, 173, 174, 175, 176, 177">SingleExpression</a>
    <a href="#SingleStatement_7768_7783" id="SingleStatement_2450_2465" title="Referenced at line 231">SingleStatement</a>.<span class="cons_Constructor"><span id="CurlyExpressionStatement_2466_2490" title="Not referenced locally, nor via imports">CurlyExpressionStatement</span></span> =      [<span class="cons_String">{</span> [<a href="#Expression_214_224" id="Expression_2502_2512" title="Defined at line 16, 135">Expression</a>] <span class="cons_String">}</span>]

    <a href="#ProcessMethodCall_1312_1329" id="ProcessMethodCall_2522_2539" title="Referenced at line 60; ../Poosl.sdf3 line 144">ProcessMethodCall</a>.<span class="cons_Constructor"><span id="ProcessMethodCall_2540_2557" title="Not referenced locally, nor via imports">ProcessMethodCall</span></span> =           [[<a href="#ID_8421_8423" id="ID_2572_2574" title="Defined at line 246, 247, 248, 249, 251, 252, 253, 255, 256, 257, 259, 260, 261, 263, 264, 265, 267, 268, 269, 271, 272, 274, 275, 276, 277, 278">ID</a>][<a href="#ExpressionList_309_323" id="ExpressionList_2576_2590" title="Defined at line 21, 194">ExpressionList</a>][<a href="#VariableList_511_523" id="VariableList_2592_2604" title="Defined at line 30, 130">VariableList</a>]]

    <a href="#AndStatement_1223_1235" id="AndStatement_2612_2624" title="Referenced at line 57">AndStatement</a>.<span class="cons_Constructor"><span id="AndStatement_2625_2637" title="Not referenced locally, nor via imports">AndStatement</span></span> = [
        <span class="cons_String">and</span>
            [<a href="#Statement_60_69" id="Statement_2667_2676" title="Defined at line 7, 38">Statement</a>]
    ]
    <a href="#OrStatement_1412_1423" id="OrStatement_2688_2699" title="Referenced at line 64">OrStatement</a>.<span class="cons_Constructor"><span id="OrStatement_2700_2711" title="Not referenced locally, nor via imports">OrStatement</span></span> = [
        <span class="cons_String">or</span>
            [<a href="#Statement_60_69" id="Statement_2740_2749" title="Defined at line 7, 38">Statement</a>]
    ]

    <a href="#CaseStatementList_2303_2320" id="CaseStatementList_2762_2779" title="Referenced at line 94">CaseStatementList</a>.<span class="cons_Constructor"><span id="CaseStatementList_2780_2797" title="Not referenced locally, nor via imports">CaseStatementList</span></span> =           [[{<a href="#CaseStatement_171_184" id="CaseStatement_2813_2826" title="Defined at line 13, 113">CaseStatement</a> <span class="cons_Lit">"\n"</span>}*]]
    <a href="#CaseStatement_2813_2826" id="CaseStatement_2840_2853" title="Referenced at line 112">CaseStatement</a>.<span class="cons_Constructor"><span id="CaseStatement_2854_2867" title="Not referenced locally, nor via imports">CaseStatement</span></span> =
        [<span class="cons_String">case</span> [<a href="#Expression_214_224" id="Expression_2885_2895" title="Defined at line 16, 135">Expression</a>] <span class="cons_String">then</span>
            [<a href="#Statement_60_69" id="Statement_2915_2924" title="Defined at line 7, 38">Statement</a>]]
    <a href="#OptDefaultStatement_2335_2354" id="OptDefaultStatement_2931_2950" title="Referenced at line 95">OptDefaultStatement</a>.<span class="cons_Constructor"><span id="DefaultStatement_2951_2967" title="Not referenced locally, nor via imports">DefaultStatement</span></span> =
        [<span class="cons_String">default</span>
            [<a href="#Statement_60_69" id="Statement_3000_3009" title="Defined at line 7, 38">Statement</a>]]
    <a href="#OptDefaultStatement_2335_2354" id="OptDefaultStatement_3016_3035" title="Referenced at line 95">OptDefaultStatement</a>.<span class="cons_Constructor"><span id="NoDefaultStatement_3036_3054" title="Not referenced locally, nor via imports">NoDefaultStatement</span></span> =        []

    <a href="#OptPostExpression_1715_1732" id="OptPostExpression_3072_3089" title="Referenced at line 69">OptPostExpression</a>.<span class="cons_Constructor"><span id="PostExpression_3090_3104" title="Not referenced locally, nor via imports">PostExpression</span></span> =              [<span class="cons_String">{</span> [<a href="#Expression_214_224" id="Expression_3124_3134" title="Defined at line 16, 135">Expression</a>] <span class="cons_String">}</span>]
    <a href="#OptPostExpression_1715_1732" id="OptPostExpression_3143_3160" title="Referenced at line 69">OptPostExpression</a>.<span class="cons_Constructor"><span id="NoPostExpression_3161_3177" title="Not referenced locally, nor via imports">NoPostExpression</span></span> =            []

    <a href="#OptReceptionCondition_1691_1712" id="OptReceptionCondition_3199_3220" title="Referenced at line 69">OptReceptionCondition</a>.<span class="cons_Constructor"><span id="ReceptionCondition_3221_3239" title="Not referenced locally, nor via imports">ReceptionCondition</span></span> =      [<span class="cons_String">|</span> [<a href="#Expression_214_224" id="Expression_3251_3261" title="Defined at line 16, 135">Expression</a>] <span class="cons_String">|</span>]
    <a href="#OptReceptionCondition_1691_1712" id="OptReceptionCondition_3270_3291" title="Referenced at line 69">OptReceptionCondition</a>.<span class="cons_Constructor"><span id="NoReceptionCondition_3292_3312" title="Not referenced locally, nor via imports">NoReceptionCondition</span></span> =    []

    <a href="#OptVariableList_1673_1688" id="OptVariableList_3326_3341" title="Referenced at line 69">OptVariableList</a>.<span class="cons_Constructor"><span id="Variables_3342_3351" title="Not referenced locally, nor via imports">Variables</span></span> =                     [<span class="cons_String">(</span>[{<a href="#ID_8421_8423" id="ID_3378_3380" title="Defined at line 246, 247, 248, 249, 251, 252, 253, 255, 256, 257, 259, 260, 261, 263, 264, 265, 267, 268, 269, 271, 272, 274, 275, 276, 277, 278">ID</a> <span class="cons_Lit">", "</span>}*]<span class="cons_String">)</span>]
    <a href="#OptVariableList_1673_1688" id="OptVariableList_3395_3410" title="Referenced at line 69">OptVariableList</a>.<span class="cons_Constructor"><span id="NoVariables_3411_3422" title="Not referenced locally, nor via imports">NoVariables</span></span> =                   []

    <a href="#VariableList_2592_2604" id="VariableList_3451_3463" title="Referenced at line 101">VariableList</a>.<span class="cons_Constructor"><span id="VariableList_3464_3476" title="Not referenced locally, nor via imports">VariableList</span></span> =                     [<span class="cons_String">(</span>[{<a href="#ID_8421_8423" id="ID_3503_3505" title="Defined at line 246, 247, 248, 249, 251, 252, 253, 255, 256, 257, 259, 260, 261, 263, 264, 265, 267, 268, 269, 271, 272, 274, 275, 276, 277, 278">ID</a> <span class="cons_Lit">", "</span>}*]<span class="cons_String">)</span>]


    <span class="layout">// === Expressions =======</span>

    <a href="#Expression_6479_6489" id="Expression_3554_3564" title="Referenced at line 202; ../Poosl.sdf3 line 198">Expression</a>.<span class="cons_Constructor"><span id="ExpressionSequence_3565_3583" title="Not referenced locally, nor via imports">ExpressionSequence</span></span> =                 [[{<a href="#SingleExpression_229_245" id="SingleExpression_3605_3621" title="Defined at line 17, 138, 139, 141, 142, 143, 145, 147, 148, 153, 160, 165, 172, 173, 174, 175, 176, 177">SingleExpression</a> <span class="cons_Lit">";\n"</span>}+]]

    <span class="layout">// --- Level 1 -------</span>
    <a href="#SingleExpression_8348_8364" id="SingleExpression_3664_3680" title="Referenced at line 243">SingleExpression</a>.<span class="cons_Constructor"><a href="#AssignmentExpression_8327_8347" id="AssignmentExpression_3681_3701" title="Referenced at line 243">AssignmentExpression</a></span> =         [[<a href="#ID_8421_8423" id="ID_3714_3716" title="Defined at line 246, 247, 248, 249, 251, 252, 253, 255, 256, 257, 259, 260, 261, 263, 264, 265, 267, 268, 269, 271, 272, 274, 275, 276, 277, 278">ID</a>] <span class="cons_String">:=</span> [<a href="#SingleExpression_229_245" id="SingleExpression_3722_3738" title="Defined at line 17, 138, 139, 141, 142, 143, 145, 147, 148, 153, 160, 165, 172, 173, 174, 175, 176, 177">SingleExpression</a>]]
    <a href="#SingleExpression_8348_8364" id="SingleExpression_3745_3761" title="Referenced at line 243">SingleExpression</a>.<span class="cons_Constructor"><a href="#ReturnExpression_8365_8381" id="ReturnExpression_3762_3778" title="Referenced at line 243">ReturnExpression</a></span> =             [<span class="cons_String">return</span> [<a href="#SingleExpression_229_245" id="SingleExpression_3802_3818" title="Defined at line 17, 138, 139, 141, 142, 143, 145, 147, 148, 153, 160, 165, 172, 173, 174, 175, 176, 177">SingleExpression</a>]]
    <span class="layout">// --- Level 2-4  -------   </span>
    <a href="#SingleExpression_8348_8364" id="SingleExpression_3858_3874" title="Referenced at line 243">SingleExpression</a>.<span class="cons_Constructor"><a href="#BinaryOperatorExpression2_8272_8297" id="BinaryOperatorExpression2_3875_3900" title="Referenced at line 242">BinaryOperatorExpression2</a></span> =    [[<a href="#SingleExpression_229_245" id="SingleExpression_3908_3924" title="Defined at line 17, 138, 139, 141, 142, 143, 145, 147, 148, 153, 160, 165, 172, 173, 174, 175, 176, 177">SingleExpression</a>] [<a href="#BinaryOperatorLevel2_436_456" id="BinaryOperatorLevel2_3927_3947" title="Defined at line 27, 209, 210, 211, 212, 213, 214, 215, 216">BinaryOperatorLevel2</a>] [<a href="#SingleExpression_229_245" id="SingleExpression_3950_3966" title="Defined at line 17, 138, 139, 141, 142, 143, 145, 147, 148, 153, 160, 165, 172, 173, 174, 175, 176, 177">SingleExpression</a>]]  {<span class="keyword">left</span>}
    <a href="#SingleExpression_8348_8364" id="SingleExpression_3981_3997" title="Referenced at line 243">SingleExpression</a>.<span class="cons_Constructor"><a href="#BinaryOperatorExpression3_8219_8244" id="BinaryOperatorExpression3_3998_4023" title="Referenced at line 241">BinaryOperatorExpression3</a></span> =    [[<a href="#SingleExpression_229_245" id="SingleExpression_4031_4047" title="Defined at line 17, 138, 139, 141, 142, 143, 145, 147, 148, 153, 160, 165, 172, 173, 174, 175, 176, 177">SingleExpression</a>] [<a href="#BinaryOperatorLevel3_461_481" id="BinaryOperatorLevel3_4050_4070" title="Defined at line 28, 218, 219, 220, 221">BinaryOperatorLevel3</a>] [<a href="#SingleExpression_229_245" id="SingleExpression_4073_4089" title="Defined at line 17, 138, 139, 141, 142, 143, 145, 147, 148, 153, 160, 165, 172, 173, 174, 175, 176, 177">SingleExpression</a>]]  {<span class="keyword">left</span>}
    <a href="#SingleExpression_8348_8364" id="SingleExpression_4104_4120" title="Referenced at line 243">SingleExpression</a>.<span class="cons_Constructor"><a href="#BinaryOperatorExpression4_8166_8191" id="BinaryOperatorExpression4_4121_4146" title="Referenced at line 240">BinaryOperatorExpression4</a></span> =    [[<a href="#SingleExpression_229_245" id="SingleExpression_4154_4170" title="Defined at line 17, 138, 139, 141, 142, 143, 145, 147, 148, 153, 160, 165, 172, 173, 174, 175, 176, 177">SingleExpression</a>] [<a href="#BinaryOperatorLevel4_486_506" id="BinaryOperatorLevel4_4173_4193" title="Defined at line 29, 223, 224">BinaryOperatorLevel4</a>] [<a href="#SingleExpression_229_245" id="SingleExpression_4196_4212" title="Defined at line 17, 138, 139, 141, 142, 143, 145, 147, 148, 153, 160, 165, 172, 173, 174, 175, 176, 177">SingleExpression</a>]]  {<span class="keyword">left</span>}
    <span class="layout">// --- Level 5 -------</span>
    <a href="#SingleExpression_8348_8364" id="SingleExpression_4254_4270" title="Referenced at line 243">SingleExpression</a>.<span class="cons_Constructor"><a href="#DataMethodCallExpression_8114_8138" id="DataMethodCallExpression_4271_4295" title="Referenced at line 239">DataMethodCallExpression</a></span> =     [[<a href="#SingleExpression_229_245" id="SingleExpression_4304_4320" title="Defined at line 17, 138, 139, 141, 142, 143, 145, 147, 148, 153, 160, 165, 172, 173, 174, 175, 176, 177">SingleExpression</a>][<a href="#OnSuperClass_250_262" id="OnSuperClass_4322_4334" title="Defined at line 18, 188, 189">OnSuperClass</a>] [<a href="#ID_8421_8423" id="ID_4337_4339" title="Defined at line 246, 247, 248, 249, 251, 252, 253, 255, 256, 257, 259, 260, 261, 263, 264, 265, 267, 268, 269, 271, 272, 274, 275, 276, 277, 278">ID</a>][<a href="#OptExpressionList_267_284" id="OptExpressionList_4341_4358" title="Defined at line 19, 191, 192">OptExpressionList</a>]]
    <span class="layout">// --- Level 6 -------</span>
    <a href="#SingleExpression_8348_8364" id="SingleExpression_4392_4408" title="Referenced at line 243">SingleExpression</a>.<span class="cons_Constructor"><a href="#UnaryOperatorExpression_8063_8086" id="UnaryOperatorExpression_4409_4432" title="Referenced at line 238">UnaryOperatorExpression</a></span> =      [[<a href="#UnaryOperator_418_431" id="UnaryOperator_4442_4455" title="Defined at line 26, 206, 207">UnaryOperator</a>][<a href="#SingleExpression_229_245" id="SingleExpression_4457_4473" title="Defined at line 17, 138, 139, 141, 142, 143, 145, 147, 148, 153, 160, 165, 172, 173, 174, 175, 176, 177">SingleExpression</a>]]
    <a href="#SingleExpression_8348_8364" id="SingleExpression_4480_4496" title="Referenced at line 243">SingleExpression</a>.<span class="cons_Constructor"><a href="#IfThenExpression_7887_7903" id="IfThenExpression_4497_4513" title="Referenced at line 233">IfThenExpression</a></span> = [
        <span class="cons_String">if</span> [<a href="#Expression_214_224" id="Expression_4530_4540" title="Defined at line 16, 135">Expression</a>] <span class="cons_String">then</span>
            [<a href="#Expression_214_224" id="Expression_4560_4570" title="Defined at line 16, 135">Expression</a>]
        <span class="cons_String">fi</span>
        ]
    <a href="#SingleExpression_8348_8364" id="SingleExpression_4597_4613" title="Referenced at line 243">SingleExpression</a>.<span class="cons_Constructor"><a href="#IfThenElseExpression_7931_7951" id="IfThenElseExpression_4614_4634" title="Referenced at line 234">IfThenElseExpression</a></span> = [
        <span class="cons_String">if</span> [<a href="#Expression_214_224" id="Expression_4651_4661" title="Defined at line 16, 135">Expression</a>] <span class="cons_String">then</span>
            [<a href="#Expression_214_224" id="Expression_4681_4691" title="Defined at line 16, 135">Expression</a>]
        <span class="cons_String">else</span>
            [<a href="#Expression_214_224" id="Expression_4719_4729" title="Defined at line 16, 135">Expression</a>]
        <span class="cons_String">fi</span>
        ]
    <a href="#SingleExpression_8348_8364" id="SingleExpression_4756_4772" title="Referenced at line 243">SingleExpression</a>.<span class="cons_Constructor"><a href="#WhileExpression_7979_7994" id="WhileExpression_4773_4788" title="Referenced at line 235">WhileExpression</a></span> = [
        <span class="cons_String">while</span> [<a href="#Expression_214_224" id="Expression_4808_4818" title="Defined at line 16, 135">Expression</a>] <span class="cons_String">do</span>
            [<a href="#Expression_214_224" id="Expression_4836_4846" title="Defined at line 16, 135">Expression</a>]
        <span class="cons_String">od</span>
        ]
    <a href="#SingleExpression_8348_8364" id="SingleExpression_4873_4889" title="Referenced at line 243">SingleExpression</a>.<span class="cons_Constructor"><a href="#SwitchExpression_8022_8038" id="SwitchExpression_4890_4906" title="Referenced at line 236">SwitchExpression</a></span> = [
        <span class="cons_String">switch</span> [<a href="#Expression_214_224" id="Expression_4927_4937" title="Defined at line 16, 135">Expression</a>] <span class="cons_String">do</span>
            [<a href="#CaseExpressionList_328_346" id="CaseExpressionList_4955_4973" title="Defined at line 22, 196">CaseExpressionList</a>]
            [<a href="#OptDefaultExpression_370_390" id="OptDefaultExpression_4988_5008" title="Defined at line 24, 200, 203">OptDefaultExpression</a>]
        <span class="cons_String">od</span>
        ]
    <span class="layout">// --- Level 7 -------</span>
    <a href="#SingleExpression_8348_8364" id="SingleExpression_5062_5078" title="Referenced at line 243">SingleExpression</a>.<span class="cons_Constructor"><span id="CurrentTimeExpression_5079_5100" title="Not referenced locally, nor via imports">CurrentTimeExpression</span></span> =        [<span class="cons_String">currentTime</span>]
    <a href="#SingleExpression_8348_8364" id="SingleExpression_5128_5144" title="Referenced at line 243">SingleExpression</a>.<span class="cons_Constructor"><span id="SelfExpression_5145_5159" title="Not referenced locally, nor via imports">SelfExpression</span></span> =               [<span class="cons_String">self</span>]
    <a href="#SingleExpression_8348_8364" id="SingleExpression_5187_5203" title="Referenced at line 243">SingleExpression</a>.<span class="cons_Constructor"><span id="ConstantExpression_5204_5222" title="Not referenced locally, nor via imports">ConstantExpression</span></span> =           <a href="#ExpressionConstant_395_413" id="ExpressionConstant_5235_5253" title="Defined at line 25, 179, 180, 181, 182, 183, 184, 185, 186">ExpressionConstant</a>
    <a href="#SingleExpression_8348_8364" id="SingleExpression_5258_5274" title="Referenced at line 243">SingleExpression</a>.<span class="cons_Constructor"><span id="NewExpression_5275_5288" title="Not referenced locally, nor via imports">NewExpression</span></span> =                [<span class="cons_String">new</span> <span class="cons_String">(</span>[<a href="#ID_8421_8423" id="ID_5313_5315" title="Defined at line 246, 247, 248, 249, 251, 252, 253, 255, 256, 257, 259, 260, 261, 263, 264, 265, 267, 268, 269, 271, 272, 274, 275, 276, 277, 278">ID</a>]<span class="cons_String">)</span>]
    <a href="#SingleExpression_8348_8364" id="SingleExpression_5323_5339" title="Referenced at line 243">SingleExpression</a>.<span class="cons_Constructor"><span id="VariableExpression_5340_5358" title="Not referenced locally, nor via imports">VariableExpression</span></span> =           <a href="#ID_8421_8423" id="ID_5371_5373" title="Defined at line 246, 247, 248, 249, 251, 252, 253, 255, 256, 257, 259, 260, 261, 263, 264, 265, 267, 268, 269, 271, 272, 274, 275, 276, 277, 278">ID</a>
    <a href="#SingleExpression_8348_8364" id="SingleExpression_5378_5394" title="Referenced at line 243">SingleExpression</a>.<span class="cons_Constructor"><a href="#RoundBracketExpression_7837_7859" id="RoundBracketExpression_5395_5417" title="Referenced at line 232">RoundBracketExpression</a></span> =       [<span class="cons_String">(</span>[<a href="#Expression_214_224" id="Expression_5429_5439" title="Defined at line 16, 135">Expression</a>]<span class="cons_String">)</span>]

    <a href="#ExpressionConstant_5235_5253" id="ExpressionConstant_5448_5466" title="Referenced at line 174; ../Poosl.sdf3 line 67">ExpressionConstant</a>.<span class="cons_Constructor"><span id="BooleanConstant_5467_5482" title="Not referenced locally, nor via imports">BooleanConstant</span></span> =            <a href="../Common.sdf3#BOOL_224_228" id="BOOL_5496_5500" title="Defined at ../Common.sdf3 line 17, 19, 20">BOOL</a>
    <a href="#ExpressionConstant_5235_5253" id="ExpressionConstant_5505_5523" title="Referenced at line 174; ../Poosl.sdf3 line 67">ExpressionConstant</a>.<span class="cons_Constructor"><span id="CharacterConstant_5524_5541" title="Not referenced locally, nor via imports">CharacterConstant</span></span> =          <a href="../Common.sdf3#CHARACTER_1292_1301" id="CHARACTER_5553_5562" title="Defined at ../Common.sdf3 line 62, 67">CHARACTER</a>
    <a href="#ExpressionConstant_5235_5253" id="ExpressionConstant_5567_5585" title="Referenced at line 174; ../Poosl.sdf3 line 67">ExpressionConstant</a>.<span class="cons_Constructor"><span id="FloatConstant_5586_5599" title="Not referenced locally, nor via imports">FloatConstant</span></span> =              <a href="../Common.sdf3#FLOAT_394_399" id="FLOAT_5615_5620" title="Defined at ../Common.sdf3 line 29, 35">FLOAT</a>
    <a href="#ExpressionConstant_5235_5253" id="ExpressionConstant_5625_5643" title="Referenced at line 174; ../Poosl.sdf3 line 67">ExpressionConstant</a>.<span class="cons_Constructor"><span id="IntegerConstant_5644_5659" title="Not referenced locally, nor via imports">IntegerConstant</span></span> =            <a href="../Common.sdf3#INT_385_388" id="INT_5673_5676" title="Defined at ../Common.sdf3 line 29, 33">INT</a>
    <a href="#ExpressionConstant_5235_5253" id="ExpressionConstant_5681_5699" title="Referenced at line 174; ../Poosl.sdf3 line 67">ExpressionConstant</a>.<span class="cons_Constructor"><span id="NilConstant_5700_5711" title="Not referenced locally, nor via imports">NilConstant</span></span> =                [<span class="cons_String">nil</span>]
    <a href="#ExpressionConstant_5235_5253" id="ExpressionConstant_5739_5757" title="Referenced at line 174; ../Poosl.sdf3 line 67">ExpressionConstant</a>.<span class="cons_Constructor"><span id="RealConstant_5758_5770" title="Not referenced locally, nor via imports">RealConstant</span></span> =               <a href="../Common.sdf3#REAL_389_393" id="REAL_5787_5791" title="Defined at ../Common.sdf3 line 29, 34">REAL</a>
    <a href="#ExpressionConstant_5235_5253" id="ExpressionConstant_5796_5814" title="Referenced at line 174; ../Poosl.sdf3 line 67">ExpressionConstant</a>.<span class="cons_Constructor"><span id="StringConstant_5815_5829" title="Not referenced locally, nor via imports">StringConstant</span></span> =             <a href="../Common.sdf3#STRING_1285_1291" id="STRING_5844_5850" title="Defined at ../Common.sdf3 line 62, 66">STRING</a>
    <a href="#ExpressionConstant_5235_5253" id="ExpressionConstant_5855_5873" title="Referenced at line 174; ../Poosl.sdf3 line 67">ExpressionConstant</a>.<span class="cons_Constructor"><span id="EnvironmentConstant_5874_5893" title="Not referenced locally, nor via imports">EnvironmentConstant</span></span> =        <a href="../Common.sdf3#ENV_53_56" id="ENV_5903_5906" title="Defined at ../Common.sdf3 line 6, 9">ENV</a>

    <a href="#OnSuperClass_4322_4334" id="OnSuperClass_5912_5924" title="Referenced at line 145">OnSuperClass</a>.<span class="cons_Constructor"><span id="OnSuperClass_5925_5937" title="Not referenced locally, nor via imports">OnSuperClass</span></span> =                     [<span class="cons_String">^</span>]
    <a href="#OnSuperClass_4322_4334" id="OnSuperClass_5968_5980" title="Referenced at line 145">OnSuperClass</a>.<span class="cons_Constructor"><span id="NotOnSuperClass_5981_5996" title="Not referenced locally, nor via imports">NotOnSuperClass</span></span> =                  []

    <a href="#OptExpressionList_4341_4358" id="OptExpressionList_6024_6041" title="Referenced at line 145">OptExpressionList</a>.<span class="cons_Constructor"><span id="Expressions_6042_6053" title="Not referenced locally, nor via imports">Expressions</span></span> =                 [<span class="cons_String">(</span>[{<a href="#Expression_214_224" id="Expression_6076_6086" title="Defined at line 16, 135">Expression</a> <span class="cons_Lit">", "</span>}*]<span class="cons_String">)</span>]
    <a href="#OptExpressionList_4341_4358" id="OptExpressionList_6101_6118" title="Referenced at line 145">OptExpressionList</a>.<span class="cons_Constructor"><span id="NoExpressions_6119_6132" title="Not referenced locally, nor via imports">NoExpressions</span></span> =               []

    <a href="#ExpressionList_2576_2590" id="ExpressionList_6157_6171" title="Referenced at line 101">ExpressionList</a>.<span class="cons_Constructor"><span id="ExpressionList_6172_6186" title="Not referenced locally, nor via imports">ExpressionList</span></span> =                 [<span class="cons_String">(</span>[{<a href="#Expression_214_224" id="Expression_6209_6219" title="Defined at line 16, 135">Expression</a> <span class="cons_Lit">", "</span>}*]<span class="cons_String">)</span>]

    <a href="#CaseExpressionList_4955_4973" id="CaseExpressionList_6235_6253" title="Referenced at line 167">CaseExpressionList</a>.<span class="cons_Constructor"><span id="CaseExpressionList_6254_6272" title="Not referenced locally, nor via imports">CaseExpressionList</span></span> =         [[{<a href="#CaseExpression_351_365" id="CaseExpression_6286_6300" title="Defined at line 23, 197">CaseExpression</a> <span class="cons_Lit">"\n"</span>}*]]
    <a href="#CaseExpression_6286_6300" id="CaseExpression_6314_6328" title="Referenced at line 196">CaseExpression</a>.<span class="cons_Constructor"><span id="CaseExpression_6329_6343" title="Not referenced locally, nor via imports">CaseExpression</span></span> =
        [<span class="cons_String">case</span> [<a href="#Expression_214_224" id="Expression_6361_6371" title="Defined at line 16, 135">Expression</a>] <span class="cons_String">then</span>
            [<a href="#Expression_214_224" id="Expression_6391_6401" title="Defined at line 16, 135">Expression</a>]]
    <a href="#OptDefaultExpression_4988_5008" id="OptDefaultExpression_6408_6428" title="Referenced at line 168">OptDefaultExpression</a>.<span class="cons_Constructor"><span id="DefaultExpression_6429_6446" title="Not referenced locally, nor via imports">DefaultExpression</span></span> =
        [<span class="cons_String">default</span>
            [<a href="#Expression_214_224" id="Expression_6479_6489" title="Defined at line 16, 135">Expression</a>]]
    <a href="#OptDefaultExpression_4988_5008" id="OptDefaultExpression_6496_6516" title="Referenced at line 168">OptDefaultExpression</a>.<span class="cons_Constructor"><span id="NoDefaultExpression_6517_6536" title="Not referenced locally, nor via imports">NoDefaultExpression</span></span> =      []

    <span class="layout">// --- Operators -------</span>
    <a href="#UnaryOperator_7517_7530" id="UnaryOperator_6581_6594" title="Referenced at line 227; ../Poosl.sdf3 line 101">UnaryOperator</a>.<span class="cons_Constructor"><span id="Minus_6595_6600" title="Not referenced locally, nor via imports">Minus</span></span> =                           [<span class="cons_String">-</span>]
    <a href="#UnaryOperator_7517_7530" id="UnaryOperator_6637_6650" title="Referenced at line 227; ../Poosl.sdf3 line 101">UnaryOperator</a>.<span class="cons_Constructor"><span id="Not_6651_6654" title="Not referenced locally, nor via imports">Not</span></span> =                             [<span class="cons_String">!</span>]

    <a href="#BinaryOperatorLevel2_3927_3947" id="BinaryOperatorLevel2_6694_6714" title="Referenced at line 141; ../Poosl.sdf3 line 110">BinaryOperatorLevel2</a>.<span class="cons_Constructor"><span id="Equal_6715_6720" title="Not referenced locally, nor via imports">Equal</span></span> =                    [<span class="cons_String">=</span>]
    <a href="#BinaryOperatorLevel2_3927_3947" id="BinaryOperatorLevel2_6750_6770" title="Referenced at line 141; ../Poosl.sdf3 line 110">BinaryOperatorLevel2</a>.<span class="cons_Constructor"><span id="Unequal_6771_6778" title="Not referenced locally, nor via imports">Unequal</span></span> =                  [<span class="cons_String">!=</span>]
    <a href="#BinaryOperatorLevel2_3927_3947" id="BinaryOperatorLevel2_6807_6827" title="Referenced at line 141; ../Poosl.sdf3 line 110">BinaryOperatorLevel2</a>.<span class="cons_Constructor"><span id="Identical_6828_6837" title="Not referenced locally, nor via imports">Identical</span></span> =                [<span class="cons_String">==</span>]
    <a href="#BinaryOperatorLevel2_3927_3947" id="BinaryOperatorLevel2_6864_6884" title="Referenced at line 141; ../Poosl.sdf3 line 110">BinaryOperatorLevel2</a>.<span class="cons_Constructor"><span id="NotIdentical_6885_6897" title="Not referenced locally, nor via imports">NotIdentical</span></span> =             [<span class="cons_String">!==</span>]
    <a href="#BinaryOperatorLevel2_3927_3947" id="BinaryOperatorLevel2_6922_6942" title="Referenced at line 141; ../Poosl.sdf3 line 110">BinaryOperatorLevel2</a>.<span class="cons_Constructor"><span id="LessThan_6943_6951" title="Not referenced locally, nor via imports">LessThan</span></span> =                 [<span class="cons_String">&lt;</span>]
    <a href="#BinaryOperatorLevel2_3927_3947" id="BinaryOperatorLevel2_6978_6998" title="Referenced at line 141; ../Poosl.sdf3 line 110">BinaryOperatorLevel2</a>.<span class="cons_Constructor"><span id="AtMost_6999_7005" title="Not referenced locally, nor via imports">AtMost</span></span> =                   [<span class="cons_String">&lt;=</span>]
    <a href="#BinaryOperatorLevel2_3927_3947" id="BinaryOperatorLevel2_7035_7055" title="Referenced at line 141; ../Poosl.sdf3 line 110">BinaryOperatorLevel2</a>.<span class="cons_Constructor"><span id="GreaterThan_7056_7067" title="Not referenced locally, nor via imports">GreaterThan</span></span> =              [<span class="cons_String">&gt;</span>]
    <a href="#BinaryOperatorLevel2_3927_3947" id="BinaryOperatorLevel2_7091_7111" title="Referenced at line 141; ../Poosl.sdf3 line 110">BinaryOperatorLevel2</a>.<span class="cons_Constructor"><span id="AtLeast_7112_7119" title="Not referenced locally, nor via imports">AtLeast</span></span> =                  [<span class="cons_String">&gt;=</span>]

    <a href="#BinaryOperatorLevel3_4050_4070" id="BinaryOperatorLevel3_7149_7169" title="Referenced at line 142; ../Poosl.sdf3 line 111">BinaryOperatorLevel3</a>.<span class="cons_Constructor"><span id="Add_7170_7173" title="Not referenced locally, nor via imports">Add</span></span> =                      [<span class="cons_String">+</span>]
    <a href="#BinaryOperatorLevel3_4050_4070" id="BinaryOperatorLevel3_7205_7225" title="Referenced at line 142; ../Poosl.sdf3 line 111">BinaryOperatorLevel3</a>.<span class="cons_Constructor"><span id="Subtract_7226_7234" title="Not referenced locally, nor via imports">Subtract</span></span> =                 [<span class="cons_String">-</span>]
    <a href="#BinaryOperatorLevel3_4050_4070" id="BinaryOperatorLevel3_7261_7281" title="Referenced at line 142; ../Poosl.sdf3 line 111">BinaryOperatorLevel3</a>.<span class="cons_Constructor"><span id="And_7282_7285" title="Not referenced locally, nor via imports">And</span></span> =                      [<span class="cons_String">&amp;</span>]
    <a href="#BinaryOperatorLevel3_4050_4070" id="BinaryOperatorLevel3_7317_7337" title="Referenced at line 142; ../Poosl.sdf3 line 111">BinaryOperatorLevel3</a>.<span class="cons_Constructor"><span id="Or_7338_7340" title="Not referenced locally, nor via imports">Or</span></span> =                       [<span class="cons_String">|</span>]
    
    <a href="#BinaryOperatorLevel4_4173_4193" id="BinaryOperatorLevel4_7378_7398" title="Referenced at line 143; ../Poosl.sdf3 line 112">BinaryOperatorLevel4</a>.<span class="cons_Constructor"><span id="Multiply_7399_7407" title="Not referenced locally, nor via imports">Multiply</span></span> =                 [<span class="cons_String">*</span>]
    <a href="#BinaryOperatorLevel4_4173_4193" id="BinaryOperatorLevel4_7434_7454" title="Referenced at line 143; ../Poosl.sdf3 line 112">BinaryOperatorLevel4</a>.<span class="cons_Constructor"><span id="Divide_7455_7461" title="Not referenced locally, nor via imports">Divide</span></span> =                   [<span class="cons_String">/</span>]

<span class="keyword">context-free restrictions</span>
    <a href="#UnaryOperator_418_431" id="UnaryOperator_7517_7530" title="Defined at line 26, 206, 207">UnaryOperator</a> -/- [<span class="cons_Regular">0</span>-<span class="cons_Regular">9</span>]                         <span class="layout">// Parse -42 as Integer instead of UnaryOperation (but 42-0 should be allowed)</span>

<span class="keyword">context-free priorities</span>
    <span class="layout">// If A &gt; B, then all trees are removed that have a B node as a direct child of an A node.</span>
    <a href="#SingleStatement_74_89" id="SingleStatement_7768_7783" title="Defined at line 8, 40, 46, 47, 48, 54, 60, 61, 67, 68, 69, 70, 75, 82, 87, 92, 98, 99">SingleStatement</a>.<span class="cons_Constructor"><a href="#ExpressionStatement_2397_2416" id="ExpressionStatement_7784_7803" title="Defined at line 98">ExpressionStatement</a></span> &lt;0&gt; &gt;
        { <a href="#SingleExpression_229_245" id="SingleExpression_7820_7836" title="Defined at line 17, 138, 139, 141, 142, 143, 145, 147, 148, 153, 160, 165, 172, 173, 174, 175, 176, 177">SingleExpression</a>.<span class="cons_Constructor"><a href="#RoundBracketExpression_5395_5417" id="RoundBracketExpression_7837_7859" title="Defined at line 177">RoundBracketExpression</a></span>
          <a href="#SingleExpression_229_245" id="SingleExpression_7870_7886" title="Defined at line 17, 138, 139, 141, 142, 143, 145, 147, 148, 153, 160, 165, 172, 173, 174, 175, 176, 177">SingleExpression</a>.<span class="cons_Constructor"><a href="#IfThenExpression_4497_4513" id="IfThenExpression_7887_7903" title="Defined at line 148">IfThenExpression</a></span>
          <a href="#SingleExpression_229_245" id="SingleExpression_7914_7930" title="Defined at line 17, 138, 139, 141, 142, 143, 145, 147, 148, 153, 160, 165, 172, 173, 174, 175, 176, 177">SingleExpression</a>.<span class="cons_Constructor"><a href="#IfThenElseExpression_4614_4634" id="IfThenElseExpression_7931_7951" title="Defined at line 153">IfThenElseExpression</a></span>
          <a href="#SingleExpression_229_245" id="SingleExpression_7962_7978" title="Defined at line 17, 138, 139, 141, 142, 143, 145, 147, 148, 153, 160, 165, 172, 173, 174, 175, 176, 177">SingleExpression</a>.<span class="cons_Constructor"><a href="#WhileExpression_4773_4788" id="WhileExpression_7979_7994" title="Defined at line 160">WhileExpression</a></span>
          <a href="#SingleExpression_229_245" id="SingleExpression_8005_8021" title="Defined at line 17, 138, 139, 141, 142, 143, 145, 147, 148, 153, 160, 165, 172, 173, 174, 175, 176, 177">SingleExpression</a>.<span class="cons_Constructor"><a href="#SwitchExpression_4890_4906" id="SwitchExpression_8022_8038" title="Defined at line 165">SwitchExpression</a></span>},

    <a href="#SingleExpression_229_245" id="SingleExpression_8046_8062" title="Defined at line 17, 138, 139, 141, 142, 143, 145, 147, 148, 153, 160, 165, 172, 173, 174, 175, 176, 177">SingleExpression</a>.<span class="cons_Constructor"><a href="#UnaryOperatorExpression_4409_4432" id="UnaryOperatorExpression_8063_8086" title="Defined at line 147">UnaryOperatorExpression</a></span> &gt;
        <a href="#SingleExpression_229_245" id="SingleExpression_8097_8113" title="Defined at line 17, 138, 139, 141, 142, 143, 145, 147, 148, 153, 160, 165, 172, 173, 174, 175, 176, 177">SingleExpression</a>.<span class="cons_Constructor"><a href="#DataMethodCallExpression_4271_4295" id="DataMethodCallExpression_8114_8138" title="Defined at line 145">DataMethodCallExpression</a></span> &gt;
        <a href="#SingleExpression_229_245" id="SingleExpression_8149_8165" title="Defined at line 17, 138, 139, 141, 142, 143, 145, 147, 148, 153, 160, 165, 172, 173, 174, 175, 176, 177">SingleExpression</a>.<span class="cons_Constructor"><a href="#BinaryOperatorExpression4_4121_4146" id="BinaryOperatorExpression4_8166_8191" title="Defined at line 143">BinaryOperatorExpression4</a></span> &gt;
        <a href="#SingleExpression_229_245" id="SingleExpression_8202_8218" title="Defined at line 17, 138, 139, 141, 142, 143, 145, 147, 148, 153, 160, 165, 172, 173, 174, 175, 176, 177">SingleExpression</a>.<span class="cons_Constructor"><a href="#BinaryOperatorExpression3_3998_4023" id="BinaryOperatorExpression3_8219_8244" title="Defined at line 142">BinaryOperatorExpression3</a></span> &gt;
        <a href="#SingleExpression_229_245" id="SingleExpression_8255_8271" title="Defined at line 17, 138, 139, 141, 142, 143, 145, 147, 148, 153, 160, 165, 172, 173, 174, 175, 176, 177">SingleExpression</a>.<span class="cons_Constructor"><a href="#BinaryOperatorExpression2_3875_3900" id="BinaryOperatorExpression2_8272_8297" title="Defined at line 141">BinaryOperatorExpression2</a></span> &gt;
        { <a href="#SingleExpression_229_245" id="SingleExpression_8310_8326" title="Defined at line 17, 138, 139, 141, 142, 143, 145, 147, 148, 153, 160, 165, 172, 173, 174, 175, 176, 177">SingleExpression</a>.<span class="cons_Constructor"><a href="#AssignmentExpression_3681_3701" id="AssignmentExpression_8327_8347" title="Defined at line 138">AssignmentExpression</a></span> <a href="#SingleExpression_229_245" id="SingleExpression_8348_8364" title="Defined at line 17, 138, 139, 141, 142, 143, 145, 147, 148, 153, 160, 165, 172, 173, 174, 175, 176, 177">SingleExpression</a>.<span class="cons_Constructor"><a href="#ReturnExpression_3762_3778" id="ReturnExpression_8365_8381" title="Defined at line 139">ReturnExpression</a></span> }

<span class="keyword">lexical syntax</span>      <span class="layout">// keywords</span>
    <a href="#ID_5371_5373" id="ID_8421_8423" title="Referenced at line 176">ID</a> = <span class="cons_Lit">"if"</span>           {<span class="keyword">reject</span>}
    <a href="#ID_5371_5373" id="ID_8454_8456" title="Referenced at line 176">ID</a> = <span class="cons_Lit">"then"</span>         {<span class="keyword">reject</span>}
    <a href="#ID_5371_5373" id="ID_8487_8489" title="Referenced at line 176">ID</a> = <span class="cons_Lit">"else"</span>         {<span class="keyword">reject</span>}
    <a href="#ID_5371_5373" id="ID_8520_8522" title="Referenced at line 176">ID</a> = <span class="cons_Lit">"fi"</span>           {<span class="keyword">reject</span>}

    <a href="#ID_5371_5373" id="ID_8554_8556" title="Referenced at line 176">ID</a> = <span class="cons_Lit">"while"</span>        {<span class="keyword">reject</span>}
    <a href="#ID_5371_5373" id="ID_8587_8589" title="Referenced at line 176">ID</a> = <span class="cons_Lit">"do"</span>           {<span class="keyword">reject</span>}
    <a href="#ID_5371_5373" id="ID_8620_8622" title="Referenced at line 176">ID</a> = <span class="cons_Lit">"od"</span>           {<span class="keyword">reject</span>}

    <a href="#ID_5371_5373" id="ID_8654_8656" title="Referenced at line 176">ID</a> = <span class="cons_Lit">"switch"</span>       {<span class="keyword">reject</span>}
    <a href="#ID_5371_5373" id="ID_8687_8689" title="Referenced at line 176">ID</a> = <span class="cons_Lit">"case"</span>         {<span class="keyword">reject</span>}
    <a href="#ID_5371_5373" id="ID_8720_8722" title="Referenced at line 176">ID</a> = <span class="cons_Lit">"default"</span>      {<span class="keyword">reject</span>}

    <a href="#ID_5371_5373" id="ID_8754_8756" title="Referenced at line 176">ID</a> = <span class="cons_Lit">"par"</span>          {<span class="keyword">reject</span>}
    <a href="#ID_5371_5373" id="ID_8787_8789" title="Referenced at line 176">ID</a> = <span class="cons_Lit">"and"</span>          {<span class="keyword">reject</span>}
    <a href="#ID_5371_5373" id="ID_8820_8822" title="Referenced at line 176">ID</a> = <span class="cons_Lit">"rap"</span>          {<span class="keyword">reject</span>}

    <a href="#ID_5371_5373" id="ID_8854_8856" title="Referenced at line 176">ID</a> = <span class="cons_Lit">"sel"</span>          {<span class="keyword">reject</span>}
    <a href="#ID_5371_5373" id="ID_8887_8889" title="Referenced at line 176">ID</a> = <span class="cons_Lit">"or"</span>           {<span class="keyword">reject</span>}
    <a href="#ID_5371_5373" id="ID_8920_8922" title="Referenced at line 176">ID</a> = <span class="cons_Lit">"les"</span>          {<span class="keyword">reject</span>}

    <a href="#ID_5371_5373" id="ID_8954_8956" title="Referenced at line 176">ID</a> = <span class="cons_Lit">"abort"</span>        {<span class="keyword">reject</span>}
    <a href="#ID_5371_5373" id="ID_8987_8989" title="Referenced at line 176">ID</a> = <span class="cons_Lit">"interrupt"</span>    {<span class="keyword">reject</span>}
    <a href="#ID_5371_5373" id="ID_9020_9022" title="Referenced at line 176">ID</a> = <span class="cons_Lit">"with"</span>         {<span class="keyword">reject</span>}

    <a href="#ID_5371_5373" id="ID_9054_9056" title="Referenced at line 176">ID</a> = <span class="cons_Lit">"delay"</span>        {<span class="keyword">reject</span>}
    <a href="#ID_5371_5373" id="ID_9087_9089" title="Referenced at line 176">ID</a> = <span class="cons_Lit">"skip"</span>         {<span class="keyword">reject</span>}

    <a href="#ID_5371_5373" id="ID_9121_9123" title="Referenced at line 176">ID</a> = <span class="cons_Lit">"currentTime"</span>  {<span class="keyword">reject</span>}
    <a href="#ID_5371_5373" id="ID_9154_9156" title="Referenced at line 176">ID</a> = <span class="cons_Lit">"new"</span>          {<span class="keyword">reject</span>}
    <a href="#ID_5371_5373" id="ID_9187_9189" title="Referenced at line 176">ID</a> = <span class="cons_Lit">"nil"</span>          {<span class="keyword">reject</span>}
    <a href="#ID_5371_5373" id="ID_9220_9222" title="Referenced at line 176">ID</a> = <span class="cons_Lit">"self"</span>         {<span class="keyword">reject</span>}
    <a href="#ID_5371_5373" id="ID_9253_9255" title="Referenced at line 176">ID</a> = <span class="cons_Lit">"return"</span>       {<span class="keyword">reject</span>}

</code></pre></td></tr></tbody></table></div>