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
<td class="code"><pre><code><span class="keyword">module</span> <button class="modal-open" id="ExprStat_1_8" title="Multi-file references" data-urls="../Poosl.sdf3/#ExprStat_5_5 ../Stratego-Poosl.sdf3/#ExprStat_12_5">ExprStat</button>

<span class="keyword">imports</span>
    <a href="../Common.sdf3/#Common_0_7" id="Common_4_5" title="Defined at ../Common.sdf3 line 1">Common</a>

<span class="keyword">context-free sorts</span>
    <button class="modal-open" id="Statement_7_5" title="Multi-file references" data-urls="#Statement_42_14 ../Poosl.sdf3/#Statement_153_14">Statement</button>
    <a href="#SingleStatement_37_55" id="SingleStatement_8_5" title="Referenced at line 38, 44, 47, 52, 231">SingleStatement</a>
    <a href="#AndStatement_56_9" id="AndStatement_9_5" title="Referenced at line 57">AndStatement</a>
    <a href="#OrStatement_63_9" id="OrStatement_10_5" title="Referenced at line 64">OrStatement</a>
    <button class="modal-open" id="ProcessMethodCall_11_5" title="Multi-file references" data-urls="#ProcessMethodCall_60_53 ../Poosl.sdf3/#ProcessMethodCall_144_14">ProcessMethodCall</button>
    <a href="#CaseStatementList_93_13" id="CaseStatementList_12_5" title="Referenced at line 94">CaseStatementList</a>
    <a href="#CaseStatement_111_55" id="CaseStatement_13_5" title="Referenced at line 112">CaseStatement</a>
    <a href="#OptDefaultStatement_94_13" id="OptDefaultStatement_14_5" title="Referenced at line 95">OptDefaultStatement</a>

    <button class="modal-open" id="Expression_16_5" title="Multi-file references" data-urls="#Expression_47_56 ../Poosl.sdf3/#Expression_85_14">Expression</button>
    <a href="#SingleExpression_45_60" id="SingleExpression_17_5" title="Referenced at line 46, 98, 135, 138, 139, 141, 142, 143, 145, 147, 232, 233, 234, 235, 236, 238, 239, 240, 241, 242, 243">SingleExpression</a>
    <a href="#OnSuperClass_144_72" id="OnSuperClass_18_5" title="Referenced at line 145">OnSuperClass</a>
    <a href="#OptExpressionList_67_63" id="OptExpressionList_19_5" title="Referenced at line 68, 145">OptExpressionList</a>
    <a href="#OptVariableList_68_63" id="OptVariableList_20_5" title="Referenced at line 69">OptVariableList</a>
    <a href="#ExpressionList_100_58" id="ExpressionList_21_5" title="Referenced at line 101">ExpressionList</a>
    <a href="#CaseExpressionList_166_13" id="CaseExpressionList_22_5" title="Referenced at line 167">CaseExpressionList</a>
    <a href="#CaseExpression_195_55" id="CaseExpression_23_5" title="Referenced at line 196">CaseExpression</a>
    <a href="#OptDefaultExpression_167_13" id="OptDefaultExpression_24_5" title="Referenced at line 168">OptDefaultExpression</a>
    <button class="modal-open" id="ExpressionConstant_25_5" title="Multi-file references" data-urls="#ExpressionConstant_174_53 ../Poosl.sdf3/#ExpressionConstant_67_61">ExpressionConstant</button>
    <button class="modal-open" id="UnaryOperator_26_5" title="Multi-file references" data-urls="#UnaryOperator_147_55 ../Poosl.sdf3/#UnaryOperator_89_10">UnaryOperator</button>
    <button class="modal-open" id="BinaryOperatorLevel2_27_5" title="Multi-file references" data-urls="#BinaryOperatorLevel2_141_74 ../Poosl.sdf3/#BinaryOperatorLevel2_110_57">BinaryOperatorLevel2</button>
    <button class="modal-open" id="BinaryOperatorLevel3_28_5" title="Multi-file references" data-urls="#BinaryOperatorLevel3_142_74 ../Poosl.sdf3/#BinaryOperatorLevel3_111_57">BinaryOperatorLevel3</button>
    <button class="modal-open" id="BinaryOperatorLevel4_29_5" title="Multi-file references" data-urls="#BinaryOperatorLevel4_143_74 ../Poosl.sdf3/#BinaryOperatorLevel4_112_57">BinaryOperatorLevel4</button>
    <a href="#VariableList_100_74" id="VariableList_30_5" title="Referenced at line 101">VariableList</a>
    <a href="#OptPostExpression_67_83" id="OptPostExpression_31_5" title="Referenced at line 68, 69">OptPostExpression</a>
    <a href="#OptReceptionCondition_68_81" id="OptReceptionCondition_32_5" title="Referenced at line 69">OptReceptionCondition</a>

<span class="keyword">context-free syntax</span>

    <span class="layout">// === Statements =======</span>

    <button class="modal-open" id="Statement_38_5" title="Multi-file references" data-urls="#Statement_42_14 ../Poosl.sdf3/#Statement_153_14">Statement</button>.<span class="cons_Constructor"><span id="StatementSequence_38_15" title="Not referenced locally, nor via imports">StatementSequence</span></span> =                   [[{<a href="#SingleStatement_7_4" id="SingleStatement_38_56" title="Defined at line 8, 40, 46, 47, 48, 54, 60, 61, 67, 68, 69, 70, 75, 82, 87, 92, 98, 99">SingleStatement</a> <span class="cons_Lit">";\n"</span>}+]]

    <a href="#SingleStatement_37_55" id="SingleStatement_40_5" title="Referenced at line 38, 44, 47, 52, 231">SingleStatement</a>.<span class="cons_Constructor"><span id="AbortStatement_40_21" title="Not referenced locally, nor via imports">AbortStatement</span></span> = [
        <span class="cons_String">abort</span>
            [<a href="#Statement_6_4" id="Statement_42_14" title="Defined at line 7, 38">Statement</a>]
        <span class="cons_String">with</span>
            [<a href="#SingleStatement_7_4" id="SingleStatement_44_14" title="Defined at line 8, 40, 46, 47, 48, 54, 60, 61, 67, 68, 69, 70, 75, 82, 87, 92, 98, 99">SingleStatement</a>]
        ]
    <a href="#SingleStatement_37_55" id="SingleStatement_46_5" title="Referenced at line 38, 44, 47, 52, 231">SingleStatement</a>.<span class="cons_Constructor"><span id="DelayStatement_46_21" title="Not referenced locally, nor via imports">DelayStatement</span></span> =                [<span class="cons_String">delay</span> [<a href="#SingleExpression_16_4" id="SingleExpression_46_61" title="Defined at line 17, 138, 139, 141, 142, 143, 145, 147, 148, 153, 160, 165, 172, 173, 174, 175, 176, 177">SingleExpression</a>]]
    <a href="#SingleStatement_37_55" id="SingleStatement_47_5" title="Referenced at line 38, 44, 47, 52, 231">SingleStatement</a>.<span class="cons_Constructor"><span id="GuardedStatement_47_21" title="Not referenced locally, nor via imports">GuardedStatement</span></span> =              &lt;<span class="cons_String">[</span>&lt;<a href="#Expression_15_4" id="Expression_47_56" title="Defined at line 16, 135">Expression</a>&gt;<span class="cons_String">]</span> &lt;<a href="#SingleStatement_7_4" id="SingleStatement_47_70" title="Defined at line 8, 40, 46, 47, 48, 54, 60, 61, 67, 68, 69, 70, 75, 82, 87, 92, 98, 99">SingleStatement</a>&gt;&gt;
    <a href="#SingleStatement_37_55" id="SingleStatement_48_5" title="Referenced at line 38, 44, 47, 52, 231">SingleStatement</a>.<span class="cons_Constructor"><span id="InterruptStatement_48_21" title="Not referenced locally, nor via imports">InterruptStatement</span></span> = [
        <span class="cons_String">interrupt</span>
            [<a href="#Statement_6_4" id="Statement_50_14" title="Defined at line 7, 38">Statement</a>]
        <span class="cons_String">with</span>
            [<a href="#SingleStatement_7_4" id="SingleStatement_52_14" title="Defined at line 8, 40, 46, 47, 48, 54, 60, 61, 67, 68, 69, 70, 75, 82, 87, 92, 98, 99">SingleStatement</a>]
        ]
    <a href="#SingleStatement_37_55" id="SingleStatement_54_5" title="Referenced at line 38, 44, 47, 52, 231">SingleStatement</a>.<span class="cons_Constructor"><span id="ParStatement_54_21" title="Not referenced locally, nor via imports">ParStatement</span></span> = [
        <span class="cons_String">par</span>
            [<a href="#Statement_6_4" id="Statement_56_14" title="Defined at line 7, 38">Statement</a>]
        [<a href="#AndStatement_8_4" id="AndStatement_57_10" title="Defined at line 9, 103">AndStatement</a>+]
        <span class="cons_String">rap</span>
        ]
    <a href="#SingleStatement_37_55" id="SingleStatement_60_5" title="Referenced at line 38, 44, 47, 52, 231">SingleStatement</a>.<span class="cons_Constructor"><span id="ProcessMethodCallStatement_60_21" title="Not referenced locally, nor via imports">ProcessMethodCallStatement</span></span> =    <a href="#ProcessMethodCall_10_4" id="ProcessMethodCall_60_53" title="Defined at line 11, 101">ProcessMethodCall</a>
    <a href="#SingleStatement_37_55" id="SingleStatement_61_5" title="Referenced at line 38, 44, 47, 52, 231">SingleStatement</a>.<span class="cons_Constructor"><span id="SelStatement_61_21" title="Not referenced locally, nor via imports">SelStatement</span></span> = [
        <span class="cons_String">sel</span>
            [<a href="#Statement_6_4" id="Statement_63_14" title="Defined at line 7, 38">Statement</a>]
        [<a href="#OrStatement_9_4" id="OrStatement_64_10" title="Defined at line 10, 107">OrStatement</a>+]
        <span class="cons_String">les</span>
        ]
    <a href="#SingleStatement_37_55" id="SingleStatement_67_5" title="Referenced at line 38, 44, 47, 52, 231">SingleStatement</a>.<span class="cons_Constructor"><span id="SkipStatement_67_21" title="Not referenced locally, nor via imports">SkipStatement</span></span> =                 [<span class="cons_String">skip</span>]
    <a href="#SingleStatement_37_55" id="SingleStatement_68_5" title="Referenced at line 38, 44, 47, 52, 231">SingleStatement</a>.<span class="cons_Constructor"><span id="SendStatement_68_21" title="Not referenced locally, nor via imports">SendStatement</span></span> =                 [[<a href="#ID_245_4" id="ID_68_55" title="Defined at line 246, 247, 248, 249, 251, 252, 253, 255, 256, 257, 259, 260, 261, 263, 264, 265, 267, 268, 269, 271, 272, 274, 275, 276, 277, 278">ID</a>]<span class="cons_String">!</span>[<a href="#ID_245_4" id="ID_68_60" title="Defined at line 246, 247, 248, 249, 251, 252, 253, 255, 256, 257, 259, 260, 261, 263, 264, 265, 267, 268, 269, 271, 272, 274, 275, 276, 277, 278">ID</a>][<a href="#OptExpressionList_18_4" id="OptExpressionList_68_64" title="Defined at line 19, 191, 192">OptExpressionList</a>] [<a href="#OptPostExpression_30_4" id="OptPostExpression_68_84" title="Defined at line 31, 121, 122">OptPostExpression</a>]]
    <a href="#SingleStatement_37_55" id="SingleStatement_69_5" title="Referenced at line 38, 44, 47, 52, 231">SingleStatement</a>.<span class="cons_Constructor"><span id="ReceiveStatement_69_21" title="Not referenced locally, nor via imports">ReceiveStatement</span></span> =              [[<a href="#ID_245_4" id="ID_69_55" title="Defined at line 246, 247, 248, 249, 251, 252, 253, 255, 256, 257, 259, 260, 261, 263, 264, 265, 267, 268, 269, 271, 272, 274, 275, 276, 277, 278">ID</a>]<span class="cons_String">?</span>[<a href="#ID_245_4" id="ID_69_60" title="Defined at line 246, 247, 248, 249, 251, 252, 253, 255, 256, 257, 259, 260, 261, 263, 264, 265, 267, 268, 269, 271, 272, 274, 275, 276, 277, 278">ID</a>][<a href="#OptVariableList_19_4" id="OptVariableList_69_64" title="Defined at line 20, 127, 128">OptVariableList</a>] [<a href="#OptReceptionCondition_31_4" id="OptReceptionCondition_69_82" title="Defined at line 32, 124, 125">OptReceptionCondition</a>] [<a href="#OptPostExpression_30_4" id="OptPostExpression_69_106" title="Defined at line 31, 121, 122">OptPostExpression</a>]]
    <a href="#SingleStatement_37_55" id="SingleStatement_70_5" title="Referenced at line 38, 44, 47, 52, 231">SingleStatement</a>.<span class="cons_Constructor"><span id="IfThenStatement_70_21" title="Not referenced locally, nor via imports">IfThenStatement</span></span> = [
        <span class="cons_String">if</span> [<a href="#Expression_15_4" id="Expression_71_13" title="Defined at line 16, 135">Expression</a>] <span class="cons_String">then</span> 
            [<a href="#Statement_6_4" id="Statement_72_14" title="Defined at line 7, 38">Statement</a>]
        <span class="cons_String">fi</span>
        ]
    <a href="#SingleStatement_37_55" id="SingleStatement_75_5" title="Referenced at line 38, 44, 47, 52, 231">SingleStatement</a>.<span class="cons_Constructor"><span id="IfThenElseStatement_75_21" title="Not referenced locally, nor via imports">IfThenElseStatement</span></span> = [
        <span class="cons_String">if</span> [<a href="#Expression_15_4" id="Expression_76_13" title="Defined at line 16, 135">Expression</a>] <span class="cons_String">then</span>
            [<a href="#Statement_6_4" id="Statement_77_14" title="Defined at line 7, 38">Statement</a>]
        <span class="cons_String">else</span>
            [<a href="#Statement_6_4" id="Statement_79_14" title="Defined at line 7, 38">Statement</a>]
        <span class="cons_String">fi</span>
        ]
    <a href="#SingleStatement_37_55" id="SingleStatement_82_5" title="Referenced at line 38, 44, 47, 52, 231">SingleStatement</a>.<span class="cons_Constructor"><span id="RoundBracketStatement_82_21" title="Not referenced locally, nor via imports">RoundBracketStatement</span></span> = [
        <span class="cons_String">(</span>
            [<a href="#Statement_6_4" id="Statement_84_14" title="Defined at line 7, 38">Statement</a>]
        <span class="cons_String">)</span>
        ]
    <a href="#SingleStatement_37_55" id="SingleStatement_87_5" title="Referenced at line 38, 44, 47, 52, 231">SingleStatement</a>.<span class="cons_Constructor"><span id="WhileStatement_87_21" title="Not referenced locally, nor via imports">WhileStatement</span></span> = [
        <span class="cons_String">while</span> [<a href="#Expression_15_4" id="Expression_88_16" title="Defined at line 16, 135">Expression</a>] <span class="cons_String">do</span>
            [<a href="#Statement_6_4" id="Statement_89_14" title="Defined at line 7, 38">Statement</a>]
        <span class="cons_String">od</span>
        ]
    <a href="#SingleStatement_37_55" id="SingleStatement_92_5" title="Referenced at line 38, 44, 47, 52, 231">SingleStatement</a>.<span class="cons_Constructor"><span id="SwitchStatement_92_21" title="Not referenced locally, nor via imports">SwitchStatement</span></span> = [
        <span class="cons_String">switch</span> [<a href="#Expression_15_4" id="Expression_93_17" title="Defined at line 16, 135">Expression</a>] <span class="cons_String">do</span>
            [<a href="#CaseStatementList_11_4" id="CaseStatementList_94_14" title="Defined at line 12, 112">CaseStatementList</a>]
            [<a href="#OptDefaultStatement_13_4" id="OptDefaultStatement_95_14" title="Defined at line 14, 116, 119">OptDefaultStatement</a>]
        <span class="cons_String">od</span>
        ]
    <a href="#SingleStatement_37_55" id="SingleStatement_98_5" title="Referenced at line 38, 44, 47, 52, 231">SingleStatement</a>.<span class="cons_Constructor"><a href="#ExpressionStatement_230_20" id="ExpressionStatement_98_21" title="Referenced at line 231">ExpressionStatement</a></span> =           <a href="#SingleExpression_16_4" id="SingleExpression_98_53" title="Defined at line 17, 138, 139, 141, 142, 143, 145, 147, 148, 153, 160, 165, 172, 173, 174, 175, 176, 177">SingleExpression</a>
    <a href="#SingleStatement_37_55" id="SingleStatement_99_5" title="Referenced at line 38, 44, 47, 52, 231">SingleStatement</a>.<span class="cons_Constructor"><span id="CurlyExpressionStatement_99_21" title="Not referenced locally, nor via imports">CurlyExpressionStatement</span></span> =      [<span class="cons_String">{</span> [<a href="#Expression_15_4" id="Expression_99_57" title="Defined at line 16, 135">Expression</a>] <span class="cons_String">}</span>]

    <button class="modal-open" id="ProcessMethodCall_101_5" title="Multi-file references" data-urls="#ProcessMethodCall_60_53 ../Poosl.sdf3/#ProcessMethodCall_144_14">ProcessMethodCall</button>.<span class="cons_Constructor"><span id="ProcessMethodCall_101_23" title="Not referenced locally, nor via imports">ProcessMethodCall</span></span> =           [[<a href="#ID_245_4" id="ID_101_55" title="Defined at line 246, 247, 248, 249, 251, 252, 253, 255, 256, 257, 259, 260, 261, 263, 264, 265, 267, 268, 269, 271, 272, 274, 275, 276, 277, 278">ID</a>][<a href="#ExpressionList_20_4" id="ExpressionList_101_59" title="Defined at line 21, 194">ExpressionList</a>][<a href="#VariableList_29_4" id="VariableList_101_75" title="Defined at line 30, 130">VariableList</a>]]

    <a href="#AndStatement_56_9" id="AndStatement_103_5" title="Referenced at line 57">AndStatement</a>.<span class="cons_Constructor"><span id="AndStatement_103_18" title="Not referenced locally, nor via imports">AndStatement</span></span> = [
        <span class="cons_String">and</span>
            [<a href="#Statement_6_4" id="Statement_105_14" title="Defined at line 7, 38">Statement</a>]
    ]
    <a href="#OrStatement_63_9" id="OrStatement_107_5" title="Referenced at line 64">OrStatement</a>.<span class="cons_Constructor"><span id="OrStatement_107_17" title="Not referenced locally, nor via imports">OrStatement</span></span> = [
        <span class="cons_String">or</span>
            [<a href="#Statement_6_4" id="Statement_109_14" title="Defined at line 7, 38">Statement</a>]
    ]

    <a href="#CaseStatementList_93_13" id="CaseStatementList_112_5" title="Referenced at line 94">CaseStatementList</a>.<span class="cons_Constructor"><span id="CaseStatementList_112_23" title="Not referenced locally, nor via imports">CaseStatementList</span></span> =           [[{<a href="#CaseStatement_12_4" id="CaseStatement_112_56" title="Defined at line 13, 113">CaseStatement</a> <span class="cons_Lit">"\n"</span>}*]]
    <a href="#CaseStatement_111_55" id="CaseStatement_113_5" title="Referenced at line 112">CaseStatement</a>.<span class="cons_Constructor"><span id="CaseStatement_113_19" title="Not referenced locally, nor via imports">CaseStatement</span></span> =
        [<span class="cons_String">case</span> [<a href="#Expression_15_4" id="Expression_114_16" title="Defined at line 16, 135">Expression</a>] <span class="cons_String">then</span>
            [<a href="#Statement_6_4" id="Statement_115_14" title="Defined at line 7, 38">Statement</a>]]
    <a href="#OptDefaultStatement_94_13" id="OptDefaultStatement_116_5" title="Referenced at line 95">OptDefaultStatement</a>.<span class="cons_Constructor"><span id="DefaultStatement_116_25" title="Not referenced locally, nor via imports">DefaultStatement</span></span> =
        [<span class="cons_String">default</span>
            [<a href="#Statement_6_4" id="Statement_118_14" title="Defined at line 7, 38">Statement</a>]]
    <a href="#OptDefaultStatement_94_13" id="OptDefaultStatement_119_5" title="Referenced at line 95">OptDefaultStatement</a>.<span class="cons_Constructor"><span id="NoDefaultStatement_119_25" title="Not referenced locally, nor via imports">NoDefaultStatement</span></span> =        []

    <a href="#OptPostExpression_67_83" id="OptPostExpression_121_5" title="Referenced at line 68, 69">OptPostExpression</a>.<span class="cons_Constructor"><span id="PostExpression_121_23" title="Not referenced locally, nor via imports">PostExpression</span></span> =              [<span class="cons_String">{</span> [<a href="#Expression_15_4" id="Expression_121_57" title="Defined at line 16, 135">Expression</a>] <span class="cons_String">}</span>]
    <a href="#OptPostExpression_67_83" id="OptPostExpression_122_5" title="Referenced at line 68, 69">OptPostExpression</a>.<span class="cons_Constructor"><span id="NoPostExpression_122_23" title="Not referenced locally, nor via imports">NoPostExpression</span></span> =            []

    <a href="#OptReceptionCondition_68_81" id="OptReceptionCondition_124_5" title="Referenced at line 69">OptReceptionCondition</a>.<span class="cons_Constructor"><span id="ReceptionCondition_124_27" title="Not referenced locally, nor via imports">ReceptionCondition</span></span> =      [<span class="cons_String">|</span> [<a href="#Expression_15_4" id="Expression_124_57" title="Defined at line 16, 135">Expression</a>] <span class="cons_String">|</span>]
    <a href="#OptReceptionCondition_68_81" id="OptReceptionCondition_125_5" title="Referenced at line 69">OptReceptionCondition</a>.<span class="cons_Constructor"><span id="NoReceptionCondition_125_27" title="Not referenced locally, nor via imports">NoReceptionCondition</span></span> =    []

    <a href="#OptVariableList_68_63" id="OptVariableList_127_5" title="Referenced at line 69">OptVariableList</a>.<span class="cons_Constructor"><span id="Variables_127_21" title="Not referenced locally, nor via imports">Variables</span></span> =                     [<span class="cons_String">(</span>[{<a href="#ID_245_4" id="ID_127_57" title="Defined at line 246, 247, 248, 249, 251, 252, 253, 255, 256, 257, 259, 260, 261, 263, 264, 265, 267, 268, 269, 271, 272, 274, 275, 276, 277, 278">ID</a> <span class="cons_Lit">", "</span>}*]<span class="cons_String">)</span>]
    <a href="#OptVariableList_68_63" id="OptVariableList_128_5" title="Referenced at line 69">OptVariableList</a>.<span class="cons_Constructor"><span id="NoVariables_128_21" title="Not referenced locally, nor via imports">NoVariables</span></span> =                   []

    <a href="#VariableList_100_74" id="VariableList_130_5" title="Referenced at line 101">VariableList</a>.<span class="cons_Constructor"><span id="VariableList_130_18" title="Not referenced locally, nor via imports">VariableList</span></span> =                     [<span class="cons_String">(</span>[{<a href="#ID_245_4" id="ID_130_57" title="Defined at line 246, 247, 248, 249, 251, 252, 253, 255, 256, 257, 259, 260, 261, 263, 264, 265, 267, 268, 269, 271, 272, 274, 275, 276, 277, 278">ID</a> <span class="cons_Lit">", "</span>}*]<span class="cons_String">)</span>]


    <span class="layout">// === Expressions =======</span>

    <button class="modal-open" id="Expression_135_5" title="Multi-file references" data-urls="#Expression_47_56 ../Poosl.sdf3/#Expression_85_14">Expression</button>.<span class="cons_Constructor"><span id="ExpressionSequence_135_16" title="Not referenced locally, nor via imports">ExpressionSequence</span></span> =                 [[{<a href="#SingleExpression_16_4" id="SingleExpression_135_56" title="Defined at line 17, 138, 139, 141, 142, 143, 145, 147, 148, 153, 160, 165, 172, 173, 174, 175, 176, 177">SingleExpression</a> <span class="cons_Lit">";\n"</span>}+]]

    <span class="layout">// --- Level 1 -------</span>
    <a href="#SingleExpression_45_60" id="SingleExpression_138_5" title="Referenced at line 46, 98, 135, 138, 139, 141, 142, 143, 145, 147, 232, 233, 234, 235, 236, 238, 239, 240, 241, 242, 243">SingleExpression</a>.<span class="cons_Constructor"><a href="#AssignmentExpression_242_27" id="AssignmentExpression_138_22" title="Referenced at line 243">AssignmentExpression</a></span> =         [[<a href="#ID_245_4" id="ID_138_55" title="Defined at line 246, 247, 248, 249, 251, 252, 253, 255, 256, 257, 259, 260, 261, 263, 264, 265, 267, 268, 269, 271, 272, 274, 275, 276, 277, 278">ID</a>] <span class="cons_String">:=</span> [<a href="#SingleExpression_16_4" id="SingleExpression_138_63" title="Defined at line 17, 138, 139, 141, 142, 143, 145, 147, 148, 153, 160, 165, 172, 173, 174, 175, 176, 177">SingleExpression</a>]]
    <a href="#SingleExpression_45_60" id="SingleExpression_139_5" title="Referenced at line 46, 98, 135, 138, 139, 141, 142, 143, 145, 147, 232, 233, 234, 235, 236, 238, 239, 240, 241, 242, 243">SingleExpression</a>.<span class="cons_Constructor"><a href="#ReturnExpression_242_65" id="ReturnExpression_139_22" title="Referenced at line 243">ReturnExpression</a></span> =             [<span class="cons_String">return</span> [<a href="#SingleExpression_16_4" id="SingleExpression_139_62" title="Defined at line 17, 138, 139, 141, 142, 143, 145, 147, 148, 153, 160, 165, 172, 173, 174, 175, 176, 177">SingleExpression</a>]]
    <span class="layout">// --- Level 2-4  -------   </span>
    <a href="#SingleExpression_45_60" id="SingleExpression_141_5" title="Referenced at line 46, 98, 135, 138, 139, 141, 142, 143, 145, 147, 232, 233, 234, 235, 236, 238, 239, 240, 241, 242, 243">SingleExpression</a>.<span class="cons_Constructor"><a href="#BinaryOperatorExpression2_241_25" id="BinaryOperatorExpression2_141_22" title="Referenced at line 242">BinaryOperatorExpression2</a></span> =    [[<a href="#SingleExpression_16_4" id="SingleExpression_141_55" title="Defined at line 17, 138, 139, 141, 142, 143, 145, 147, 148, 153, 160, 165, 172, 173, 174, 175, 176, 177">SingleExpression</a>] [<a href="#BinaryOperatorLevel2_26_4" id="BinaryOperatorLevel2_141_74" title="Defined at line 27, 209, 210, 211, 212, 213, 214, 215, 216">BinaryOperatorLevel2</a>] [<a href="#SingleExpression_16_4" id="SingleExpression_141_97" title="Defined at line 17, 138, 139, 141, 142, 143, 145, 147, 148, 153, 160, 165, 172, 173, 174, 175, 176, 177">SingleExpression</a>]]  {<span class="keyword">left</span>}
    <a href="#SingleExpression_45_60" id="SingleExpression_142_5" title="Referenced at line 46, 98, 135, 138, 139, 141, 142, 143, 145, 147, 232, 233, 234, 235, 236, 238, 239, 240, 241, 242, 243">SingleExpression</a>.<span class="cons_Constructor"><a href="#BinaryOperatorExpression3_240_25" id="BinaryOperatorExpression3_142_22" title="Referenced at line 241">BinaryOperatorExpression3</a></span> =    [[<a href="#SingleExpression_16_4" id="SingleExpression_142_55" title="Defined at line 17, 138, 139, 141, 142, 143, 145, 147, 148, 153, 160, 165, 172, 173, 174, 175, 176, 177">SingleExpression</a>] [<a href="#BinaryOperatorLevel3_27_4" id="BinaryOperatorLevel3_142_74" title="Defined at line 28, 218, 219, 220, 221">BinaryOperatorLevel3</a>] [<a href="#SingleExpression_16_4" id="SingleExpression_142_97" title="Defined at line 17, 138, 139, 141, 142, 143, 145, 147, 148, 153, 160, 165, 172, 173, 174, 175, 176, 177">SingleExpression</a>]]  {<span class="keyword">left</span>}
    <a href="#SingleExpression_45_60" id="SingleExpression_143_5" title="Referenced at line 46, 98, 135, 138, 139, 141, 142, 143, 145, 147, 232, 233, 234, 235, 236, 238, 239, 240, 241, 242, 243">SingleExpression</a>.<span class="cons_Constructor"><a href="#BinaryOperatorExpression4_239_25" id="BinaryOperatorExpression4_143_22" title="Referenced at line 240">BinaryOperatorExpression4</a></span> =    [[<a href="#SingleExpression_16_4" id="SingleExpression_143_55" title="Defined at line 17, 138, 139, 141, 142, 143, 145, 147, 148, 153, 160, 165, 172, 173, 174, 175, 176, 177">SingleExpression</a>] [<a href="#BinaryOperatorLevel4_28_4" id="BinaryOperatorLevel4_143_74" title="Defined at line 29, 223, 224">BinaryOperatorLevel4</a>] [<a href="#SingleExpression_16_4" id="SingleExpression_143_97" title="Defined at line 17, 138, 139, 141, 142, 143, 145, 147, 148, 153, 160, 165, 172, 173, 174, 175, 176, 177">SingleExpression</a>]]  {<span class="keyword">left</span>}
    <span class="layout">// --- Level 5 -------</span>
    <a href="#SingleExpression_45_60" id="SingleExpression_145_5" title="Referenced at line 46, 98, 135, 138, 139, 141, 142, 143, 145, 147, 232, 233, 234, 235, 236, 238, 239, 240, 241, 242, 243">SingleExpression</a>.<span class="cons_Constructor"><a href="#DataMethodCallExpression_238_25" id="DataMethodCallExpression_145_22" title="Referenced at line 239">DataMethodCallExpression</a></span> =     [[<a href="#SingleExpression_16_4" id="SingleExpression_145_55" title="Defined at line 17, 138, 139, 141, 142, 143, 145, 147, 148, 153, 160, 165, 172, 173, 174, 175, 176, 177">SingleExpression</a>][<a href="#OnSuperClass_17_4" id="OnSuperClass_145_73" title="Defined at line 18, 188, 189">OnSuperClass</a>] [<a href="#ID_245_4" id="ID_145_88" title="Defined at line 246, 247, 248, 249, 251, 252, 253, 255, 256, 257, 259, 260, 261, 263, 264, 265, 267, 268, 269, 271, 272, 274, 275, 276, 277, 278">ID</a>][<a href="#OptExpressionList_18_4" id="OptExpressionList_145_92" title="Defined at line 19, 191, 192">OptExpressionList</a>]]
    <span class="layout">// --- Level 6 -------</span>
    <a href="#SingleExpression_45_60" id="SingleExpression_147_5" title="Referenced at line 46, 98, 135, 138, 139, 141, 142, 143, 145, 147, 232, 233, 234, 235, 236, 238, 239, 240, 241, 242, 243">SingleExpression</a>.<span class="cons_Constructor"><a href="#UnaryOperatorExpression_237_21" id="UnaryOperatorExpression_147_22" title="Referenced at line 238">UnaryOperatorExpression</a></span> =      [[<a href="#UnaryOperator_25_4" id="UnaryOperator_147_55" title="Defined at line 26, 206, 207">UnaryOperator</a>][<a href="#SingleExpression_16_4" id="SingleExpression_147_70" title="Defined at line 17, 138, 139, 141, 142, 143, 145, 147, 148, 153, 160, 165, 172, 173, 174, 175, 176, 177">SingleExpression</a>]]
    <a href="#SingleExpression_45_60" id="SingleExpression_148_5" title="Referenced at line 46, 98, 135, 138, 139, 141, 142, 143, 145, 147, 232, 233, 234, 235, 236, 238, 239, 240, 241, 242, 243">SingleExpression</a>.<span class="cons_Constructor"><a href="#IfThenExpression_232_27" id="IfThenExpression_148_22" title="Referenced at line 233">IfThenExpression</a></span> = [
        <span class="cons_String">if</span> [<a href="#Expression_15_4" id="Expression_149_13" title="Defined at line 16, 135">Expression</a>] <span class="cons_String">then</span>
            [<a href="#Expression_15_4" id="Expression_150_14" title="Defined at line 16, 135">Expression</a>]
        <span class="cons_String">fi</span>
        ]
    <a href="#SingleExpression_45_60" id="SingleExpression_153_5" title="Referenced at line 46, 98, 135, 138, 139, 141, 142, 143, 145, 147, 232, 233, 234, 235, 236, 238, 239, 240, 241, 242, 243">SingleExpression</a>.<span class="cons_Constructor"><a href="#IfThenElseExpression_233_27" id="IfThenElseExpression_153_22" title="Referenced at line 234">IfThenElseExpression</a></span> = [
        <span class="cons_String">if</span> [<a href="#Expression_15_4" id="Expression_154_13" title="Defined at line 16, 135">Expression</a>] <span class="cons_String">then</span>
            [<a href="#Expression_15_4" id="Expression_155_14" title="Defined at line 16, 135">Expression</a>]
        <span class="cons_String">else</span>
            [<a href="#Expression_15_4" id="Expression_157_14" title="Defined at line 16, 135">Expression</a>]
        <span class="cons_String">fi</span>
        ]
    <a href="#SingleExpression_45_60" id="SingleExpression_160_5" title="Referenced at line 46, 98, 135, 138, 139, 141, 142, 143, 145, 147, 232, 233, 234, 235, 236, 238, 239, 240, 241, 242, 243">SingleExpression</a>.<span class="cons_Constructor"><a href="#WhileExpression_234_27" id="WhileExpression_160_22" title="Referenced at line 235">WhileExpression</a></span> = [
        <span class="cons_String">while</span> [<a href="#Expression_15_4" id="Expression_161_16" title="Defined at line 16, 135">Expression</a>] <span class="cons_String">do</span>
            [<a href="#Expression_15_4" id="Expression_162_14" title="Defined at line 16, 135">Expression</a>]
        <span class="cons_String">od</span>
        ]
    <a href="#SingleExpression_45_60" id="SingleExpression_165_5" title="Referenced at line 46, 98, 135, 138, 139, 141, 142, 143, 145, 147, 232, 233, 234, 235, 236, 238, 239, 240, 241, 242, 243">SingleExpression</a>.<span class="cons_Constructor"><a href="#SwitchExpression_235_27" id="SwitchExpression_165_22" title="Referenced at line 236">SwitchExpression</a></span> = [
        <span class="cons_String">switch</span> [<a href="#Expression_15_4" id="Expression_166_17" title="Defined at line 16, 135">Expression</a>] <span class="cons_String">do</span>
            [<a href="#CaseExpressionList_21_4" id="CaseExpressionList_167_14" title="Defined at line 22, 196">CaseExpressionList</a>]
            [<a href="#OptDefaultExpression_23_4" id="OptDefaultExpression_168_14" title="Defined at line 24, 200, 203">OptDefaultExpression</a>]
        <span class="cons_String">od</span>
        ]
    <span class="layout">// --- Level 7 -------</span>
    <a href="#SingleExpression_45_60" id="SingleExpression_172_5" title="Referenced at line 46, 98, 135, 138, 139, 141, 142, 143, 145, 147, 232, 233, 234, 235, 236, 238, 239, 240, 241, 242, 243">SingleExpression</a>.<span class="cons_Constructor"><span id="CurrentTimeExpression_172_22" title="Not referenced locally, nor via imports">CurrentTimeExpression</span></span> =        [<span class="cons_String">currentTime</span>]
    <a href="#SingleExpression_45_60" id="SingleExpression_173_5" title="Referenced at line 46, 98, 135, 138, 139, 141, 142, 143, 145, 147, 232, 233, 234, 235, 236, 238, 239, 240, 241, 242, 243">SingleExpression</a>.<span class="cons_Constructor"><span id="SelfExpression_173_22" title="Not referenced locally, nor via imports">SelfExpression</span></span> =               [<span class="cons_String">self</span>]
    <a href="#SingleExpression_45_60" id="SingleExpression_174_5" title="Referenced at line 46, 98, 135, 138, 139, 141, 142, 143, 145, 147, 232, 233, 234, 235, 236, 238, 239, 240, 241, 242, 243">SingleExpression</a>.<span class="cons_Constructor"><span id="ConstantExpression_174_22" title="Not referenced locally, nor via imports">ConstantExpression</span></span> =           <a href="#ExpressionConstant_24_4" id="ExpressionConstant_174_53" title="Defined at line 25, 179, 180, 181, 182, 183, 184, 185, 186">ExpressionConstant</a>
    <a href="#SingleExpression_45_60" id="SingleExpression_175_5" title="Referenced at line 46, 98, 135, 138, 139, 141, 142, 143, 145, 147, 232, 233, 234, 235, 236, 238, 239, 240, 241, 242, 243">SingleExpression</a>.<span class="cons_Constructor"><span id="NewExpression_175_22" title="Not referenced locally, nor via imports">NewExpression</span></span> =                [<span class="cons_String">new</span> <span class="cons_String">(</span>[<a href="#ID_245_4" id="ID_175_60" title="Defined at line 246, 247, 248, 249, 251, 252, 253, 255, 256, 257, 259, 260, 261, 263, 264, 265, 267, 268, 269, 271, 272, 274, 275, 276, 277, 278">ID</a>]<span class="cons_String">)</span>]
    <a href="#SingleExpression_45_60" id="SingleExpression_176_5" title="Referenced at line 46, 98, 135, 138, 139, 141, 142, 143, 145, 147, 232, 233, 234, 235, 236, 238, 239, 240, 241, 242, 243">SingleExpression</a>.<span class="cons_Constructor"><span id="VariableExpression_176_22" title="Not referenced locally, nor via imports">VariableExpression</span></span> =           <a href="#ID_245_4" id="ID_176_53" title="Defined at line 246, 247, 248, 249, 251, 252, 253, 255, 256, 257, 259, 260, 261, 263, 264, 265, 267, 268, 269, 271, 272, 274, 275, 276, 277, 278">ID</a>
    <a href="#SingleExpression_45_60" id="SingleExpression_177_5" title="Referenced at line 46, 98, 135, 138, 139, 141, 142, 143, 145, 147, 232, 233, 234, 235, 236, 238, 239, 240, 241, 242, 243">SingleExpression</a>.<span class="cons_Constructor"><a href="#RoundBracketExpression_231_27" id="RoundBracketExpression_177_22" title="Referenced at line 232">RoundBracketExpression</a></span> =       [<span class="cons_String">(</span>[<a href="#Expression_15_4" id="Expression_177_56" title="Defined at line 16, 135">Expression</a>]<span class="cons_String">)</span>]

    <button class="modal-open" id="ExpressionConstant_179_5" title="Multi-file references" data-urls="#ExpressionConstant_174_53 ../Poosl.sdf3/#ExpressionConstant_67_61">ExpressionConstant</button>.<span class="cons_Constructor"><span id="BooleanConstant_179_24" title="Not referenced locally, nor via imports">BooleanConstant</span></span> =            <a href="../Common.sdf3/#BOOL_16_2" id="BOOL_179_53" title="Defined at ../Common.sdf3 line 17, 19, 20">BOOL</a>
    <button class="modal-open" id="ExpressionConstant_180_5" title="Multi-file references" data-urls="#ExpressionConstant_174_53 ../Poosl.sdf3/#ExpressionConstant_67_61">ExpressionConstant</button>.<span class="cons_Constructor"><span id="CharacterConstant_180_24" title="Not referenced locally, nor via imports">CharacterConstant</span></span> =          <a href="../Common.sdf3/#CHARACTER_61_9" id="CHARACTER_180_53" title="Defined at ../Common.sdf3 line 62, 67">CHARACTER</a>
    <button class="modal-open" id="ExpressionConstant_181_5" title="Multi-file references" data-urls="#ExpressionConstant_174_53 ../Poosl.sdf3/#ExpressionConstant_67_61">ExpressionConstant</button>.<span class="cons_Constructor"><span id="FloatConstant_181_24" title="Not referenced locally, nor via imports">FloatConstant</span></span> =              <a href="../Common.sdf3/#FLOAT_28_11" id="FLOAT_181_53" title="Defined at ../Common.sdf3 line 29, 35">FLOAT</a>
    <button class="modal-open" id="ExpressionConstant_182_5" title="Multi-file references" data-urls="#ExpressionConstant_174_53 ../Poosl.sdf3/#ExpressionConstant_67_61">ExpressionConstant</button>.<span class="cons_Constructor"><span id="IntegerConstant_182_24" title="Not referenced locally, nor via imports">IntegerConstant</span></span> =            <a href="../Common.sdf3/#INT_28_2" id="INT_182_53" title="Defined at ../Common.sdf3 line 29, 33">INT</a>
    <button class="modal-open" id="ExpressionConstant_183_5" title="Multi-file references" data-urls="#ExpressionConstant_174_53 ../Poosl.sdf3/#ExpressionConstant_67_61">ExpressionConstant</button>.<span class="cons_Constructor"><span id="NilConstant_183_24" title="Not referenced locally, nor via imports">NilConstant</span></span> =                [<span class="cons_String">nil</span>]
    <button class="modal-open" id="ExpressionConstant_184_5" title="Multi-file references" data-urls="#ExpressionConstant_174_53 ../Poosl.sdf3/#ExpressionConstant_67_61">ExpressionConstant</button>.<span class="cons_Constructor"><span id="RealConstant_184_24" title="Not referenced locally, nor via imports">RealConstant</span></span> =               <a href="../Common.sdf3/#REAL_28_6" id="REAL_184_53" title="Defined at ../Common.sdf3 line 29, 34">REAL</a>
    <button class="modal-open" id="ExpressionConstant_185_5" title="Multi-file references" data-urls="#ExpressionConstant_174_53 ../Poosl.sdf3/#ExpressionConstant_67_61">ExpressionConstant</button>.<span class="cons_Constructor"><span id="StringConstant_185_24" title="Not referenced locally, nor via imports">StringConstant</span></span> =             <a href="../Common.sdf3/#STRING_61_2" id="STRING_185_53" title="Defined at ../Common.sdf3 line 62, 66">STRING</a>
    <button class="modal-open" id="ExpressionConstant_186_5" title="Multi-file references" data-urls="#ExpressionConstant_174_53 ../Poosl.sdf3/#ExpressionConstant_67_61">ExpressionConstant</button>.<span class="cons_Constructor"><span id="EnvironmentConstant_186_24" title="Not referenced locally, nor via imports">EnvironmentConstant</span></span> =        <a href="../Common.sdf3/#ENV_5_5" id="ENV_186_53" title="Defined at ../Common.sdf3 line 6, 9">ENV</a>

    <a href="#OnSuperClass_144_72" id="OnSuperClass_188_5" title="Referenced at line 145">OnSuperClass</a>.<span class="cons_Constructor"><span id="OnSuperClass_188_18" title="Not referenced locally, nor via imports">OnSuperClass</span></span> =                     [<span class="cons_String">^</span>]
    <a href="#OnSuperClass_144_72" id="OnSuperClass_189_5" title="Referenced at line 145">OnSuperClass</a>.<span class="cons_Constructor"><span id="NotOnSuperClass_189_18" title="Not referenced locally, nor via imports">NotOnSuperClass</span></span> =                  []

    <a href="#OptExpressionList_67_63" id="OptExpressionList_191_5" title="Referenced at line 68, 145">OptExpressionList</a>.<span class="cons_Constructor"><span id="Expressions_191_23" title="Not referenced locally, nor via imports">Expressions</span></span> =                 [<span class="cons_String">(</span>[{<a href="#Expression_15_4" id="Expression_191_57" title="Defined at line 16, 135">Expression</a> <span class="cons_Lit">", "</span>}*]<span class="cons_String">)</span>]
    <a href="#OptExpressionList_67_63" id="OptExpressionList_192_5" title="Referenced at line 68, 145">OptExpressionList</a>.<span class="cons_Constructor"><span id="NoExpressions_192_23" title="Not referenced locally, nor via imports">NoExpressions</span></span> =               []

    <a href="#ExpressionList_100_58" id="ExpressionList_194_5" title="Referenced at line 101">ExpressionList</a>.<span class="cons_Constructor"><span id="ExpressionList_194_20" title="Not referenced locally, nor via imports">ExpressionList</span></span> =                 [<span class="cons_String">(</span>[{<a href="#Expression_15_4" id="Expression_194_57" title="Defined at line 16, 135">Expression</a> <span class="cons_Lit">", "</span>}*]<span class="cons_String">)</span>]

    <a href="#CaseExpressionList_166_13" id="CaseExpressionList_196_5" title="Referenced at line 167">CaseExpressionList</a>.<span class="cons_Constructor"><span id="CaseExpressionList_196_24" title="Not referenced locally, nor via imports">CaseExpressionList</span></span> =         [[{<a href="#CaseExpression_22_4" id="CaseExpression_196_56" title="Defined at line 23, 197">CaseExpression</a> <span class="cons_Lit">"\n"</span>}*]]
    <a href="#CaseExpression_195_55" id="CaseExpression_197_5" title="Referenced at line 196">CaseExpression</a>.<span class="cons_Constructor"><span id="CaseExpression_197_20" title="Not referenced locally, nor via imports">CaseExpression</span></span> =
        [<span class="cons_String">case</span> [<a href="#Expression_15_4" id="Expression_198_16" title="Defined at line 16, 135">Expression</a>] <span class="cons_String">then</span>
            [<a href="#Expression_15_4" id="Expression_199_14" title="Defined at line 16, 135">Expression</a>]]
    <a href="#OptDefaultExpression_167_13" id="OptDefaultExpression_200_5" title="Referenced at line 168">OptDefaultExpression</a>.<span class="cons_Constructor"><span id="DefaultExpression_200_26" title="Not referenced locally, nor via imports">DefaultExpression</span></span> =
        [<span class="cons_String">default</span>
            [<a href="#Expression_15_4" id="Expression_202_14" title="Defined at line 16, 135">Expression</a>]]
    <a href="#OptDefaultExpression_167_13" id="OptDefaultExpression_203_5" title="Referenced at line 168">OptDefaultExpression</a>.<span class="cons_Constructor"><span id="NoDefaultExpression_203_26" title="Not referenced locally, nor via imports">NoDefaultExpression</span></span> =      []

    <span class="layout">// --- Operators -------</span>
    <button class="modal-open" id="UnaryOperator_206_5" title="Multi-file references" data-urls="#UnaryOperator_147_55 ../Poosl.sdf3/#UnaryOperator_89_10">UnaryOperator</button>.<span class="cons_Constructor"><span id="Minus_206_19" title="Not referenced locally, nor via imports">Minus</span></span> =                           [<span class="cons_String">-</span>]
    <button class="modal-open" id="UnaryOperator_207_5" title="Multi-file references" data-urls="#UnaryOperator_147_55 ../Poosl.sdf3/#UnaryOperator_89_10">UnaryOperator</button>.<span class="cons_Constructor"><span id="Not_207_19" title="Not referenced locally, nor via imports">Not</span></span> =                             [<span class="cons_String">!</span>]

    <button class="modal-open" id="BinaryOperatorLevel2_209_5" title="Multi-file references" data-urls="#BinaryOperatorLevel2_141_74 ../Poosl.sdf3/#BinaryOperatorLevel2_110_57">BinaryOperatorLevel2</button>.<span class="cons_Constructor"><span id="Equal_209_26" title="Not referenced locally, nor via imports">Equal</span></span> =                    [<span class="cons_String">=</span>]
    <button class="modal-open" id="BinaryOperatorLevel2_210_5" title="Multi-file references" data-urls="#BinaryOperatorLevel2_141_74 ../Poosl.sdf3/#BinaryOperatorLevel2_110_57">BinaryOperatorLevel2</button>.<span class="cons_Constructor"><span id="Unequal_210_26" title="Not referenced locally, nor via imports">Unequal</span></span> =                  [<span class="cons_String">!=</span>]
    <button class="modal-open" id="BinaryOperatorLevel2_211_5" title="Multi-file references" data-urls="#BinaryOperatorLevel2_141_74 ../Poosl.sdf3/#BinaryOperatorLevel2_110_57">BinaryOperatorLevel2</button>.<span class="cons_Constructor"><span id="Identical_211_26" title="Not referenced locally, nor via imports">Identical</span></span> =                [<span class="cons_String">==</span>]
    <button class="modal-open" id="BinaryOperatorLevel2_212_5" title="Multi-file references" data-urls="#BinaryOperatorLevel2_141_74 ../Poosl.sdf3/#BinaryOperatorLevel2_110_57">BinaryOperatorLevel2</button>.<span class="cons_Constructor"><span id="NotIdentical_212_26" title="Not referenced locally, nor via imports">NotIdentical</span></span> =             [<span class="cons_String">!==</span>]
    <button class="modal-open" id="BinaryOperatorLevel2_213_5" title="Multi-file references" data-urls="#BinaryOperatorLevel2_141_74 ../Poosl.sdf3/#BinaryOperatorLevel2_110_57">BinaryOperatorLevel2</button>.<span class="cons_Constructor"><span id="LessThan_213_26" title="Not referenced locally, nor via imports">LessThan</span></span> =                 [<span class="cons_String">&lt;</span>]
    <button class="modal-open" id="BinaryOperatorLevel2_214_5" title="Multi-file references" data-urls="#BinaryOperatorLevel2_141_74 ../Poosl.sdf3/#BinaryOperatorLevel2_110_57">BinaryOperatorLevel2</button>.<span class="cons_Constructor"><span id="AtMost_214_26" title="Not referenced locally, nor via imports">AtMost</span></span> =                   [<span class="cons_String">&lt;=</span>]
    <button class="modal-open" id="BinaryOperatorLevel2_215_5" title="Multi-file references" data-urls="#BinaryOperatorLevel2_141_74 ../Poosl.sdf3/#BinaryOperatorLevel2_110_57">BinaryOperatorLevel2</button>.<span class="cons_Constructor"><span id="GreaterThan_215_26" title="Not referenced locally, nor via imports">GreaterThan</span></span> =              [<span class="cons_String">&gt;</span>]
    <button class="modal-open" id="BinaryOperatorLevel2_216_5" title="Multi-file references" data-urls="#BinaryOperatorLevel2_141_74 ../Poosl.sdf3/#BinaryOperatorLevel2_110_57">BinaryOperatorLevel2</button>.<span class="cons_Constructor"><span id="AtLeast_216_26" title="Not referenced locally, nor via imports">AtLeast</span></span> =                  [<span class="cons_String">&gt;=</span>]

    <button class="modal-open" id="BinaryOperatorLevel3_218_5" title="Multi-file references" data-urls="#BinaryOperatorLevel3_142_74 ../Poosl.sdf3/#BinaryOperatorLevel3_111_57">BinaryOperatorLevel3</button>.<span class="cons_Constructor"><span id="Add_218_26" title="Not referenced locally, nor via imports">Add</span></span> =                      [<span class="cons_String">+</span>]
    <button class="modal-open" id="BinaryOperatorLevel3_219_5" title="Multi-file references" data-urls="#BinaryOperatorLevel3_142_74 ../Poosl.sdf3/#BinaryOperatorLevel3_111_57">BinaryOperatorLevel3</button>.<span class="cons_Constructor"><span id="Subtract_219_26" title="Not referenced locally, nor via imports">Subtract</span></span> =                 [<span class="cons_String">-</span>]
    <button class="modal-open" id="BinaryOperatorLevel3_220_5" title="Multi-file references" data-urls="#BinaryOperatorLevel3_142_74 ../Poosl.sdf3/#BinaryOperatorLevel3_111_57">BinaryOperatorLevel3</button>.<span class="cons_Constructor"><span id="And_220_26" title="Not referenced locally, nor via imports">And</span></span> =                      [<span class="cons_String">&amp;</span>]
    <button class="modal-open" id="BinaryOperatorLevel3_221_5" title="Multi-file references" data-urls="#BinaryOperatorLevel3_142_74 ../Poosl.sdf3/#BinaryOperatorLevel3_111_57">BinaryOperatorLevel3</button>.<span class="cons_Constructor"><span id="Or_221_26" title="Not referenced locally, nor via imports">Or</span></span> =                       [<span class="cons_String">|</span>]
    
    <button class="modal-open" id="BinaryOperatorLevel4_223_5" title="Multi-file references" data-urls="#BinaryOperatorLevel4_143_74 ../Poosl.sdf3/#BinaryOperatorLevel4_112_57">BinaryOperatorLevel4</button>.<span class="cons_Constructor"><span id="Multiply_223_26" title="Not referenced locally, nor via imports">Multiply</span></span> =                 [<span class="cons_String">*</span>]
    <button class="modal-open" id="BinaryOperatorLevel4_224_5" title="Multi-file references" data-urls="#BinaryOperatorLevel4_143_74 ../Poosl.sdf3/#BinaryOperatorLevel4_112_57">BinaryOperatorLevel4</button>.<span class="cons_Constructor"><span id="Divide_224_26" title="Not referenced locally, nor via imports">Divide</span></span> =                   [<span class="cons_String">/</span>]

<span class="keyword">context-free restrictions</span>
    <a href="#UnaryOperator_25_4" id="UnaryOperator_227_5" title="Defined at line 26, 206, 207">UnaryOperator</a> -/- [<span class="cons_Regular">0</span>-<span class="cons_Regular">9</span>]                         <span class="layout">// Parse -42 as Integer instead of UnaryOperation (but 42-0 should be allowed)</span>

<span class="keyword">context-free priorities</span>
    <span class="layout">// If A &gt; B, then all trees are removed that have a B node as a direct child of an A node.</span>
    <a href="#SingleStatement_7_4" id="SingleStatement_231_5" title="Defined at line 8, 40, 46, 47, 48, 54, 60, 61, 67, 68, 69, 70, 75, 82, 87, 92, 98, 99">SingleStatement</a>.<span class="cons_Constructor"><a href="#ExpressionStatement_97_20" id="ExpressionStatement_231_21" title="Defined at line 98">ExpressionStatement</a></span> &lt;0&gt; &gt;
        { <a href="#SingleExpression_16_4" id="SingleExpression_232_11" title="Defined at line 17, 138, 139, 141, 142, 143, 145, 147, 148, 153, 160, 165, 172, 173, 174, 175, 176, 177">SingleExpression</a>.<span class="cons_Constructor"><a href="#RoundBracketExpression_176_21" id="RoundBracketExpression_232_28" title="Defined at line 177">RoundBracketExpression</a></span>
          <a href="#SingleExpression_16_4" id="SingleExpression_233_11" title="Defined at line 17, 138, 139, 141, 142, 143, 145, 147, 148, 153, 160, 165, 172, 173, 174, 175, 176, 177">SingleExpression</a>.<span class="cons_Constructor"><a href="#IfThenExpression_147_21" id="IfThenExpression_233_28" title="Defined at line 148">IfThenExpression</a></span>
          <a href="#SingleExpression_16_4" id="SingleExpression_234_11" title="Defined at line 17, 138, 139, 141, 142, 143, 145, 147, 148, 153, 160, 165, 172, 173, 174, 175, 176, 177">SingleExpression</a>.<span class="cons_Constructor"><a href="#IfThenElseExpression_152_21" id="IfThenElseExpression_234_28" title="Defined at line 153">IfThenElseExpression</a></span>
          <a href="#SingleExpression_16_4" id="SingleExpression_235_11" title="Defined at line 17, 138, 139, 141, 142, 143, 145, 147, 148, 153, 160, 165, 172, 173, 174, 175, 176, 177">SingleExpression</a>.<span class="cons_Constructor"><a href="#WhileExpression_159_21" id="WhileExpression_235_28" title="Defined at line 160">WhileExpression</a></span>
          <a href="#SingleExpression_16_4" id="SingleExpression_236_11" title="Defined at line 17, 138, 139, 141, 142, 143, 145, 147, 148, 153, 160, 165, 172, 173, 174, 175, 176, 177">SingleExpression</a>.<span class="cons_Constructor"><a href="#SwitchExpression_164_21" id="SwitchExpression_236_28" title="Defined at line 165">SwitchExpression</a></span>},

    <a href="#SingleExpression_16_4" id="SingleExpression_238_5" title="Defined at line 17, 138, 139, 141, 142, 143, 145, 147, 148, 153, 160, 165, 172, 173, 174, 175, 176, 177">SingleExpression</a>.<span class="cons_Constructor"><a href="#UnaryOperatorExpression_146_21" id="UnaryOperatorExpression_238_22" title="Defined at line 147">UnaryOperatorExpression</a></span> &gt;
        <a href="#SingleExpression_16_4" id="SingleExpression_239_9" title="Defined at line 17, 138, 139, 141, 142, 143, 145, 147, 148, 153, 160, 165, 172, 173, 174, 175, 176, 177">SingleExpression</a>.<span class="cons_Constructor"><a href="#DataMethodCallExpression_144_21" id="DataMethodCallExpression_239_26" title="Defined at line 145">DataMethodCallExpression</a></span> &gt;
        <a href="#SingleExpression_16_4" id="SingleExpression_240_9" title="Defined at line 17, 138, 139, 141, 142, 143, 145, 147, 148, 153, 160, 165, 172, 173, 174, 175, 176, 177">SingleExpression</a>.<span class="cons_Constructor"><a href="#BinaryOperatorExpression4_142_21" id="BinaryOperatorExpression4_240_26" title="Defined at line 143">BinaryOperatorExpression4</a></span> &gt;
        <a href="#SingleExpression_16_4" id="SingleExpression_241_9" title="Defined at line 17, 138, 139, 141, 142, 143, 145, 147, 148, 153, 160, 165, 172, 173, 174, 175, 176, 177">SingleExpression</a>.<span class="cons_Constructor"><a href="#BinaryOperatorExpression3_141_21" id="BinaryOperatorExpression3_241_26" title="Defined at line 142">BinaryOperatorExpression3</a></span> &gt;
        <a href="#SingleExpression_16_4" id="SingleExpression_242_9" title="Defined at line 17, 138, 139, 141, 142, 143, 145, 147, 148, 153, 160, 165, 172, 173, 174, 175, 176, 177">SingleExpression</a>.<span class="cons_Constructor"><a href="#BinaryOperatorExpression2_140_21" id="BinaryOperatorExpression2_242_26" title="Defined at line 141">BinaryOperatorExpression2</a></span> &gt;
        { <a href="#SingleExpression_16_4" id="SingleExpression_243_11" title="Defined at line 17, 138, 139, 141, 142, 143, 145, 147, 148, 153, 160, 165, 172, 173, 174, 175, 176, 177">SingleExpression</a>.<span class="cons_Constructor"><a href="#AssignmentExpression_137_21" id="AssignmentExpression_243_28" title="Defined at line 138">AssignmentExpression</a></span> <a href="#SingleExpression_16_4" id="SingleExpression_243_49" title="Defined at line 17, 138, 139, 141, 142, 143, 145, 147, 148, 153, 160, 165, 172, 173, 174, 175, 176, 177">SingleExpression</a>.<span class="cons_Constructor"><a href="#ReturnExpression_138_21" id="ReturnExpression_243_66" title="Defined at line 139">ReturnExpression</a></span> }

<span class="keyword">lexical syntax</span>      <span class="layout">// keywords</span>
    <a href="#ID_67_54" id="ID_246_5" title="Referenced at line 68, 69, 101, 127, 130, 138, 145, 175, 176">ID</a> = <span class="cons_Lit">"if"</span>           {<span class="keyword">reject</span>}
    <a href="#ID_67_54" id="ID_247_5" title="Referenced at line 68, 69, 101, 127, 130, 138, 145, 175, 176">ID</a> = <span class="cons_Lit">"then"</span>         {<span class="keyword">reject</span>}
    <a href="#ID_67_54" id="ID_248_5" title="Referenced at line 68, 69, 101, 127, 130, 138, 145, 175, 176">ID</a> = <span class="cons_Lit">"else"</span>         {<span class="keyword">reject</span>}
    <a href="#ID_67_54" id="ID_249_5" title="Referenced at line 68, 69, 101, 127, 130, 138, 145, 175, 176">ID</a> = <span class="cons_Lit">"fi"</span>           {<span class="keyword">reject</span>}

    <a href="#ID_67_54" id="ID_251_5" title="Referenced at line 68, 69, 101, 127, 130, 138, 145, 175, 176">ID</a> = <span class="cons_Lit">"while"</span>        {<span class="keyword">reject</span>}
    <a href="#ID_67_54" id="ID_252_5" title="Referenced at line 68, 69, 101, 127, 130, 138, 145, 175, 176">ID</a> = <span class="cons_Lit">"do"</span>           {<span class="keyword">reject</span>}
    <a href="#ID_67_54" id="ID_253_5" title="Referenced at line 68, 69, 101, 127, 130, 138, 145, 175, 176">ID</a> = <span class="cons_Lit">"od"</span>           {<span class="keyword">reject</span>}

    <a href="#ID_67_54" id="ID_255_5" title="Referenced at line 68, 69, 101, 127, 130, 138, 145, 175, 176">ID</a> = <span class="cons_Lit">"switch"</span>       {<span class="keyword">reject</span>}
    <a href="#ID_67_54" id="ID_256_5" title="Referenced at line 68, 69, 101, 127, 130, 138, 145, 175, 176">ID</a> = <span class="cons_Lit">"case"</span>         {<span class="keyword">reject</span>}
    <a href="#ID_67_54" id="ID_257_5" title="Referenced at line 68, 69, 101, 127, 130, 138, 145, 175, 176">ID</a> = <span class="cons_Lit">"default"</span>      {<span class="keyword">reject</span>}

    <a href="#ID_67_54" id="ID_259_5" title="Referenced at line 68, 69, 101, 127, 130, 138, 145, 175, 176">ID</a> = <span class="cons_Lit">"par"</span>          {<span class="keyword">reject</span>}
    <a href="#ID_67_54" id="ID_260_5" title="Referenced at line 68, 69, 101, 127, 130, 138, 145, 175, 176">ID</a> = <span class="cons_Lit">"and"</span>          {<span class="keyword">reject</span>}
    <a href="#ID_67_54" id="ID_261_5" title="Referenced at line 68, 69, 101, 127, 130, 138, 145, 175, 176">ID</a> = <span class="cons_Lit">"rap"</span>          {<span class="keyword">reject</span>}

    <a href="#ID_67_54" id="ID_263_5" title="Referenced at line 68, 69, 101, 127, 130, 138, 145, 175, 176">ID</a> = <span class="cons_Lit">"sel"</span>          {<span class="keyword">reject</span>}
    <a href="#ID_67_54" id="ID_264_5" title="Referenced at line 68, 69, 101, 127, 130, 138, 145, 175, 176">ID</a> = <span class="cons_Lit">"or"</span>           {<span class="keyword">reject</span>}
    <a href="#ID_67_54" id="ID_265_5" title="Referenced at line 68, 69, 101, 127, 130, 138, 145, 175, 176">ID</a> = <span class="cons_Lit">"les"</span>          {<span class="keyword">reject</span>}

    <a href="#ID_67_54" id="ID_267_5" title="Referenced at line 68, 69, 101, 127, 130, 138, 145, 175, 176">ID</a> = <span class="cons_Lit">"abort"</span>        {<span class="keyword">reject</span>}
    <a href="#ID_67_54" id="ID_268_5" title="Referenced at line 68, 69, 101, 127, 130, 138, 145, 175, 176">ID</a> = <span class="cons_Lit">"interrupt"</span>    {<span class="keyword">reject</span>}
    <a href="#ID_67_54" id="ID_269_5" title="Referenced at line 68, 69, 101, 127, 130, 138, 145, 175, 176">ID</a> = <span class="cons_Lit">"with"</span>         {<span class="keyword">reject</span>}

    <a href="#ID_67_54" id="ID_271_5" title="Referenced at line 68, 69, 101, 127, 130, 138, 145, 175, 176">ID</a> = <span class="cons_Lit">"delay"</span>        {<span class="keyword">reject</span>}
    <a href="#ID_67_54" id="ID_272_5" title="Referenced at line 68, 69, 101, 127, 130, 138, 145, 175, 176">ID</a> = <span class="cons_Lit">"skip"</span>         {<span class="keyword">reject</span>}

    <a href="#ID_67_54" id="ID_274_5" title="Referenced at line 68, 69, 101, 127, 130, 138, 145, 175, 176">ID</a> = <span class="cons_Lit">"currentTime"</span>  {<span class="keyword">reject</span>}
    <a href="#ID_67_54" id="ID_275_5" title="Referenced at line 68, 69, 101, 127, 130, 138, 145, 175, 176">ID</a> = <span class="cons_Lit">"new"</span>          {<span class="keyword">reject</span>}
    <a href="#ID_67_54" id="ID_276_5" title="Referenced at line 68, 69, 101, 127, 130, 138, 145, 175, 176">ID</a> = <span class="cons_Lit">"nil"</span>          {<span class="keyword">reject</span>}
    <a href="#ID_67_54" id="ID_277_5" title="Referenced at line 68, 69, 101, 127, 130, 138, 145, 175, 176">ID</a> = <span class="cons_Lit">"self"</span>         {<span class="keyword">reject</span>}
    <a href="#ID_67_54" id="ID_278_5" title="Referenced at line 68, 69, 101, 127, 130, 138, 145, 175, 176">ID</a> = <span class="cons_Lit">"return"</span>       {<span class="keyword">reject</span>}

</code></pre></td></tr></tbody></table></div>

<div id="modal">
  <div id="modal-content">
    <span id="modal-close">&times;</span>
    <h2 id="modal-h2"></h2>
    <p  id="modal-p"></p>
    <ul id="modal-ul"></ul>
  </div>
</div>
