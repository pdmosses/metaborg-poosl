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
<td class="code"><pre><code><span class="keyword">module</span> <button class="modal-open" id="ExprStat_1_8" title="a definition with multiple references" data-urls="../Poosl.sdf3/#ExprStat line 5_5; ../Stratego-Poosl.sdf3/#ExprStat line 12_5">ExprStat</button>

<span class="keyword">imports</span>
    <a href="../Common.sdf3/#Common_1_8" id="Common_4_5" title="a reference to a single-file definition">Common</a>

<span class="keyword">context-free sorts</span>
    <button class="modal-open" id="Statement_7_5" title="a definition with multiple references" data-urls="#Statement line 42_14, 50_14, 56_14, 63_14, 72_14, 77_14, 79_14, 84_14, 89_14, 105_14, 109_14, 115_14, 118_14; ../Poosl.sdf3/#Statement line 153_14">Statement</button>
    <button class="modal-open" id="SingleStatement_8_5" title="a definition with multiple references" data-urls="#SingleStatement line 38_56, 44_14, 47_70, 52_14, 231_5">SingleStatement</button>
    <a href="#AndStatement_57_10" id="AndStatement_9_5" title="a definition with a single reference">AndStatement</a>
    <a href="#OrStatement_64_10" id="OrStatement_10_5" title="a definition with a single reference">OrStatement</a>
    <button class="modal-open" id="ProcessMethodCall_11_5" title="a definition with multiple references" data-urls="#ProcessMethodCall line 60_53; ../Poosl.sdf3/#ProcessMethodCall line 144_14">ProcessMethodCall</button>
    <a href="#CaseStatementList_94_14" id="CaseStatementList_12_5" title="a definition with a single reference">CaseStatementList</a>
    <a href="#CaseStatement_112_56" id="CaseStatement_13_5" title="a definition with a single reference">CaseStatement</a>
    <a href="#OptDefaultStatement_95_14" id="OptDefaultStatement_14_5" title="a definition with a single reference">OptDefaultStatement</a>

    <button class="modal-open" id="Expression_16_5" title="a definition with multiple references" data-urls="#Expression line 47_56, 71_13, 76_13, 88_16, 93_17, 99_57, 114_16, 121_57, 124_57, 149_13, 150_14, 154_13, 155_14, 157_14, 161_16, 162_14, 166_17, 177_56, 191_57, 194_57, 198_16, 199_14, 202_14; ../Poosl.sdf3/#Expression line 85_14, 90_14, 95_14, 198_67">Expression</button>
    <button class="modal-open" id="SingleExpression_17_5" title="a definition with multiple references" data-urls="#SingleExpression line 46_61, 98_53, 135_56, 138_63, 139_62, 141_55, 141_97, 142_55, 142_97, 143_55, 143_97, 145_55, 147_70, 232_11, 233_11, 234_11, 235_11, 236_11, 238_5, 239_9, 240_9, 241_9, 242_9, 243_11, 243_49">SingleExpression</button>
    <a href="#OnSuperClass_145_73" id="OnSuperClass_18_5" title="a definition with a single reference">OnSuperClass</a>
    <button class="modal-open" id="OptExpressionList_19_5" title="a definition with multiple references" data-urls="#OptExpressionList line 68_64, 145_92">OptExpressionList</button>
    <a href="#OptVariableList_69_64" id="OptVariableList_20_5" title="a definition with a single reference">OptVariableList</a>
    <a href="#ExpressionList_101_59" id="ExpressionList_21_5" title="a definition with a single reference">ExpressionList</a>
    <a href="#CaseExpressionList_167_14" id="CaseExpressionList_22_5" title="a definition with a single reference">CaseExpressionList</a>
    <a href="#CaseExpression_196_56" id="CaseExpression_23_5" title="a definition with a single reference">CaseExpression</a>
    <a href="#OptDefaultExpression_168_14" id="OptDefaultExpression_24_5" title="a definition with a single reference">OptDefaultExpression</a>
    <button class="modal-open" id="ExpressionConstant_25_5" title="a definition with multiple references" data-urls="#ExpressionConstant line 174_53; ../Poosl.sdf3/#ExpressionConstant line 67_61">ExpressionConstant</button>
    <button class="modal-open" id="UnaryOperator_26_5" title="a definition with multiple references" data-urls="#UnaryOperator line 147_55, 227_5; ../Poosl.sdf3/#UnaryOperator line 89_10, 101_17">UnaryOperator</button>
    <button class="modal-open" id="BinaryOperatorLevel2_27_5" title="a definition with multiple references" data-urls="#BinaryOperatorLevel2 line 141_74; ../Poosl.sdf3/#BinaryOperatorLevel2 line 110_57">BinaryOperatorLevel2</button>
    <button class="modal-open" id="BinaryOperatorLevel3_28_5" title="a definition with multiple references" data-urls="#BinaryOperatorLevel3 line 142_74; ../Poosl.sdf3/#BinaryOperatorLevel3 line 111_57">BinaryOperatorLevel3</button>
    <button class="modal-open" id="BinaryOperatorLevel4_29_5" title="a definition with multiple references" data-urls="#BinaryOperatorLevel4 line 143_74; ../Poosl.sdf3/#BinaryOperatorLevel4 line 112_57">BinaryOperatorLevel4</button>
    <a href="#VariableList_101_75" id="VariableList_30_5" title="a definition with a single reference">VariableList</a>
    <button class="modal-open" id="OptPostExpression_31_5" title="a definition with multiple references" data-urls="#OptPostExpression line 68_84, 69_106">OptPostExpression</button>
    <a href="#OptReceptionCondition_69_82" id="OptReceptionCondition_32_5" title="a definition with a single reference">OptReceptionCondition</a>

<span class="keyword">context-free syntax</span>

    <span class="layout">// === Statements =======</span>

    <button class="modal-open" id="Statement_38_5" title="a definition with multiple references" data-urls="#Statement line 42_14, 50_14, 56_14, 63_14, 72_14, 77_14, 79_14, 84_14, 89_14, 105_14, 109_14, 115_14, 118_14; ../Poosl.sdf3/#Statement line 153_14">Statement</button>.<span class="cons_Constructor"><span id="StatementSequence_38_15" title="a definition with no references">StatementSequence</span></span> =                   [[{<a href="#SingleStatement_8_5" id="SingleStatement_38_56" title="a reference to a single-file definition">SingleStatement</a> <span class="cons_Lit">";\n"</span>}+]]

    <button class="modal-open" id="SingleStatement_40_5" title="a definition with multiple references" data-urls="#SingleStatement line 38_56, 44_14, 47_70, 52_14, 231_5">SingleStatement</button>.<span class="cons_Constructor"><span id="AbortStatement_40_21" title="a definition with no references">AbortStatement</span></span> = [
        <span class="cons_String">abort</span>
            [<a href="#Statement_7_5" id="Statement_42_14" title="a reference to a single-file definition">Statement</a>]
        <span class="cons_String">with</span>
            [<a href="#SingleStatement_8_5" id="SingleStatement_44_14" title="a reference to a single-file definition">SingleStatement</a>]
        ]
    <button class="modal-open" id="SingleStatement_46_5" title="a definition with multiple references" data-urls="#SingleStatement line 38_56, 44_14, 47_70, 52_14, 231_5">SingleStatement</button>.<span class="cons_Constructor"><span id="DelayStatement_46_21" title="a definition with no references">DelayStatement</span></span> =                [<span class="cons_String">delay</span> [<a href="#SingleExpression_17_5" id="SingleExpression_46_61" title="a reference to a single-file definition">SingleExpression</a>]]
    <button class="modal-open" id="SingleStatement_47_5" title="a definition with multiple references" data-urls="#SingleStatement line 38_56, 44_14, 47_70, 52_14, 231_5">SingleStatement</button>.<span class="cons_Constructor"><span id="GuardedStatement_47_21" title="a definition with no references">GuardedStatement</span></span> =              &lt;<span class="cons_String">[</span>&lt;<a href="#Expression_16_5" id="Expression_47_56" title="a reference to a single-file definition">Expression</a>&gt;<span class="cons_String">]</span> &lt;<a href="#SingleStatement_8_5" id="SingleStatement_47_70" title="a reference to a single-file definition">SingleStatement</a>&gt;&gt;
    <button class="modal-open" id="SingleStatement_48_5" title="a definition with multiple references" data-urls="#SingleStatement line 38_56, 44_14, 47_70, 52_14, 231_5">SingleStatement</button>.<span class="cons_Constructor"><span id="InterruptStatement_48_21" title="a definition with no references">InterruptStatement</span></span> = [
        <span class="cons_String">interrupt</span>
            [<a href="#Statement_7_5" id="Statement_50_14" title="a reference to a single-file definition">Statement</a>]
        <span class="cons_String">with</span>
            [<a href="#SingleStatement_8_5" id="SingleStatement_52_14" title="a reference to a single-file definition">SingleStatement</a>]
        ]
    <button class="modal-open" id="SingleStatement_54_5" title="a definition with multiple references" data-urls="#SingleStatement line 38_56, 44_14, 47_70, 52_14, 231_5">SingleStatement</button>.<span class="cons_Constructor"><span id="ParStatement_54_21" title="a definition with no references">ParStatement</span></span> = [
        <span class="cons_String">par</span>
            [<a href="#Statement_7_5" id="Statement_56_14" title="a reference to a single-file definition">Statement</a>]
        [<a href="#AndStatement_9_5" id="AndStatement_57_10" title="a reference to a single-file definition">AndStatement</a>+]
        <span class="cons_String">rap</span>
        ]
    <button class="modal-open" id="SingleStatement_60_5" title="a definition with multiple references" data-urls="#SingleStatement line 38_56, 44_14, 47_70, 52_14, 231_5">SingleStatement</button>.<span class="cons_Constructor"><span id="ProcessMethodCallStatement_60_21" title="a definition with no references">ProcessMethodCallStatement</span></span> =    <a href="#ProcessMethodCall_11_5" id="ProcessMethodCall_60_53" title="a reference to a single-file definition">ProcessMethodCall</a>
    <button class="modal-open" id="SingleStatement_61_5" title="a definition with multiple references" data-urls="#SingleStatement line 38_56, 44_14, 47_70, 52_14, 231_5">SingleStatement</button>.<span class="cons_Constructor"><span id="SelStatement_61_21" title="a definition with no references">SelStatement</span></span> = [
        <span class="cons_String">sel</span>
            [<a href="#Statement_7_5" id="Statement_63_14" title="a reference to a single-file definition">Statement</a>]
        [<a href="#OrStatement_10_5" id="OrStatement_64_10" title="a reference to a single-file definition">OrStatement</a>+]
        <span class="cons_String">les</span>
        ]
    <button class="modal-open" id="SingleStatement_67_5" title="a definition with multiple references" data-urls="#SingleStatement line 38_56, 44_14, 47_70, 52_14, 231_5">SingleStatement</button>.<span class="cons_Constructor"><span id="SkipStatement_67_21" title="a definition with no references">SkipStatement</span></span> =                 [<span class="cons_String">skip</span>]
    <button class="modal-open" id="SingleStatement_68_5" title="a definition with multiple references" data-urls="#SingleStatement line 38_56, 44_14, 47_70, 52_14, 231_5">SingleStatement</button>.<span class="cons_Constructor"><span id="SendStatement_68_21" title="a definition with no references">SendStatement</span></span> =                 [[<a href="#ID_246_5" id="ID_68_55" title="a reference to a single-file definition">ID</a>]<span class="cons_String">!</span>[<a href="#ID_246_5" id="ID_68_60" title="a reference to a single-file definition">ID</a>][<a href="#OptExpressionList_19_5" id="OptExpressionList_68_64" title="a reference to a single-file definition">OptExpressionList</a>] [<a href="#OptPostExpression_31_5" id="OptPostExpression_68_84" title="a reference to a single-file definition">OptPostExpression</a>]]
    <button class="modal-open" id="SingleStatement_69_5" title="a definition with multiple references" data-urls="#SingleStatement line 38_56, 44_14, 47_70, 52_14, 231_5">SingleStatement</button>.<span class="cons_Constructor"><span id="ReceiveStatement_69_21" title="a definition with no references">ReceiveStatement</span></span> =              [[<a href="#ID_246_5" id="ID_69_55" title="a reference to a single-file definition">ID</a>]<span class="cons_String">?</span>[<a href="#ID_246_5" id="ID_69_60" title="a reference to a single-file definition">ID</a>][<a href="#OptVariableList_20_5" id="OptVariableList_69_64" title="a reference to a single-file definition">OptVariableList</a>] [<a href="#OptReceptionCondition_32_5" id="OptReceptionCondition_69_82" title="a reference to a single-file definition">OptReceptionCondition</a>] [<a href="#OptPostExpression_31_5" id="OptPostExpression_69_106" title="a reference to a single-file definition">OptPostExpression</a>]]
    <button class="modal-open" id="SingleStatement_70_5" title="a definition with multiple references" data-urls="#SingleStatement line 38_56, 44_14, 47_70, 52_14, 231_5">SingleStatement</button>.<span class="cons_Constructor"><span id="IfThenStatement_70_21" title="a definition with no references">IfThenStatement</span></span> = [
        <span class="cons_String">if</span> [<a href="#Expression_16_5" id="Expression_71_13" title="a reference to a single-file definition">Expression</a>] <span class="cons_String">then</span> 
            [<a href="#Statement_7_5" id="Statement_72_14" title="a reference to a single-file definition">Statement</a>]
        <span class="cons_String">fi</span>
        ]
    <button class="modal-open" id="SingleStatement_75_5" title="a definition with multiple references" data-urls="#SingleStatement line 38_56, 44_14, 47_70, 52_14, 231_5">SingleStatement</button>.<span class="cons_Constructor"><span id="IfThenElseStatement_75_21" title="a definition with no references">IfThenElseStatement</span></span> = [
        <span class="cons_String">if</span> [<a href="#Expression_16_5" id="Expression_76_13" title="a reference to a single-file definition">Expression</a>] <span class="cons_String">then</span>
            [<a href="#Statement_7_5" id="Statement_77_14" title="a reference to a single-file definition">Statement</a>]
        <span class="cons_String">else</span>
            [<a href="#Statement_7_5" id="Statement_79_14" title="a reference to a single-file definition">Statement</a>]
        <span class="cons_String">fi</span>
        ]
    <button class="modal-open" id="SingleStatement_82_5" title="a definition with multiple references" data-urls="#SingleStatement line 38_56, 44_14, 47_70, 52_14, 231_5">SingleStatement</button>.<span class="cons_Constructor"><span id="RoundBracketStatement_82_21" title="a definition with no references">RoundBracketStatement</span></span> = [
        <span class="cons_String">(</span>
            [<a href="#Statement_7_5" id="Statement_84_14" title="a reference to a single-file definition">Statement</a>]
        <span class="cons_String">)</span>
        ]
    <button class="modal-open" id="SingleStatement_87_5" title="a definition with multiple references" data-urls="#SingleStatement line 38_56, 44_14, 47_70, 52_14, 231_5">SingleStatement</button>.<span class="cons_Constructor"><span id="WhileStatement_87_21" title="a definition with no references">WhileStatement</span></span> = [
        <span class="cons_String">while</span> [<a href="#Expression_16_5" id="Expression_88_16" title="a reference to a single-file definition">Expression</a>] <span class="cons_String">do</span>
            [<a href="#Statement_7_5" id="Statement_89_14" title="a reference to a single-file definition">Statement</a>]
        <span class="cons_String">od</span>
        ]
    <button class="modal-open" id="SingleStatement_92_5" title="a definition with multiple references" data-urls="#SingleStatement line 38_56, 44_14, 47_70, 52_14, 231_5">SingleStatement</button>.<span class="cons_Constructor"><span id="SwitchStatement_92_21" title="a definition with no references">SwitchStatement</span></span> = [
        <span class="cons_String">switch</span> [<a href="#Expression_16_5" id="Expression_93_17" title="a reference to a single-file definition">Expression</a>] <span class="cons_String">do</span>
            [<a href="#CaseStatementList_12_5" id="CaseStatementList_94_14" title="a reference to a single-file definition">CaseStatementList</a>]
            [<a href="#OptDefaultStatement_14_5" id="OptDefaultStatement_95_14" title="a reference to a single-file definition">OptDefaultStatement</a>]
        <span class="cons_String">od</span>
        ]
    <button class="modal-open" id="SingleStatement_98_5" title="a definition with multiple references" data-urls="#SingleStatement line 38_56, 44_14, 47_70, 52_14, 231_5">SingleStatement</button>.<span class="cons_Constructor"><a href="#ExpressionStatement_231_21" id="ExpressionStatement_98_21" title="a definition with a single reference">ExpressionStatement</a></span> =           <a href="#SingleExpression_17_5" id="SingleExpression_98_53" title="a reference to a single-file definition">SingleExpression</a>
    <button class="modal-open" id="SingleStatement_99_5" title="a definition with multiple references" data-urls="#SingleStatement line 38_56, 44_14, 47_70, 52_14, 231_5">SingleStatement</button>.<span class="cons_Constructor"><span id="CurlyExpressionStatement_99_21" title="a definition with no references">CurlyExpressionStatement</span></span> =      [<span class="cons_String">{</span> [<a href="#Expression_16_5" id="Expression_99_57" title="a reference to a single-file definition">Expression</a>] <span class="cons_String">}</span>]

    <button class="modal-open" id="ProcessMethodCall_101_5" title="a definition with multiple references" data-urls="#ProcessMethodCall line 60_53; ../Poosl.sdf3/#ProcessMethodCall line 144_14">ProcessMethodCall</button>.<span class="cons_Constructor"><span id="ProcessMethodCall_101_23" title="a definition with no references">ProcessMethodCall</span></span> =           [[<a href="#ID_246_5" id="ID_101_55" title="a reference to a single-file definition">ID</a>][<a href="#ExpressionList_21_5" id="ExpressionList_101_59" title="a reference to a single-file definition">ExpressionList</a>][<a href="#VariableList_30_5" id="VariableList_101_75" title="a reference to a single-file definition">VariableList</a>]]

    <a href="#AndStatement_57_10" id="AndStatement_103_5" title="a definition with a single reference">AndStatement</a>.<span class="cons_Constructor"><span id="AndStatement_103_18" title="a definition with no references">AndStatement</span></span> = [
        <span class="cons_String">and</span>
            [<a href="#Statement_7_5" id="Statement_105_14" title="a reference to a single-file definition">Statement</a>]
    ]
    <a href="#OrStatement_64_10" id="OrStatement_107_5" title="a definition with a single reference">OrStatement</a>.<span class="cons_Constructor"><span id="OrStatement_107_17" title="a definition with no references">OrStatement</span></span> = [
        <span class="cons_String">or</span>
            [<a href="#Statement_7_5" id="Statement_109_14" title="a reference to a single-file definition">Statement</a>]
    ]

    <a href="#CaseStatementList_94_14" id="CaseStatementList_112_5" title="a definition with a single reference">CaseStatementList</a>.<span class="cons_Constructor"><span id="CaseStatementList_112_23" title="a definition with no references">CaseStatementList</span></span> =           [[{<a href="#CaseStatement_13_5" id="CaseStatement_112_56" title="a reference to a single-file definition">CaseStatement</a> <span class="cons_Lit">"\n"</span>}*]]
    <a href="#CaseStatement_112_56" id="CaseStatement_113_5" title="a definition with a single reference">CaseStatement</a>.<span class="cons_Constructor"><span id="CaseStatement_113_19" title="a definition with no references">CaseStatement</span></span> =
        [<span class="cons_String">case</span> [<a href="#Expression_16_5" id="Expression_114_16" title="a reference to a single-file definition">Expression</a>] <span class="cons_String">then</span>
            [<a href="#Statement_7_5" id="Statement_115_14" title="a reference to a single-file definition">Statement</a>]]
    <a href="#OptDefaultStatement_95_14" id="OptDefaultStatement_116_5" title="a definition with a single reference">OptDefaultStatement</a>.<span class="cons_Constructor"><span id="DefaultStatement_116_25" title="a definition with no references">DefaultStatement</span></span> =
        [<span class="cons_String">default</span>
            [<a href="#Statement_7_5" id="Statement_118_14" title="a reference to a single-file definition">Statement</a>]]
    <a href="#OptDefaultStatement_95_14" id="OptDefaultStatement_119_5" title="a definition with a single reference">OptDefaultStatement</a>.<span class="cons_Constructor"><span id="NoDefaultStatement_119_25" title="a definition with no references">NoDefaultStatement</span></span> =        []

    <button class="modal-open" id="OptPostExpression_121_5" title="a definition with multiple references" data-urls="#OptPostExpression line 68_84, 69_106">OptPostExpression</button>.<span class="cons_Constructor"><span id="PostExpression_121_23" title="a definition with no references">PostExpression</span></span> =              [<span class="cons_String">{</span> [<a href="#Expression_16_5" id="Expression_121_57" title="a reference to a single-file definition">Expression</a>] <span class="cons_String">}</span>]
    <button class="modal-open" id="OptPostExpression_122_5" title="a definition with multiple references" data-urls="#OptPostExpression line 68_84, 69_106">OptPostExpression</button>.<span class="cons_Constructor"><span id="NoPostExpression_122_23" title="a definition with no references">NoPostExpression</span></span> =            []

    <a href="#OptReceptionCondition_69_82" id="OptReceptionCondition_124_5" title="a definition with a single reference">OptReceptionCondition</a>.<span class="cons_Constructor"><span id="ReceptionCondition_124_27" title="a definition with no references">ReceptionCondition</span></span> =      [<span class="cons_String">|</span> [<a href="#Expression_16_5" id="Expression_124_57" title="a reference to a single-file definition">Expression</a>] <span class="cons_String">|</span>]
    <a href="#OptReceptionCondition_69_82" id="OptReceptionCondition_125_5" title="a definition with a single reference">OptReceptionCondition</a>.<span class="cons_Constructor"><span id="NoReceptionCondition_125_27" title="a definition with no references">NoReceptionCondition</span></span> =    []

    <a href="#OptVariableList_69_64" id="OptVariableList_127_5" title="a definition with a single reference">OptVariableList</a>.<span class="cons_Constructor"><span id="Variables_127_21" title="a definition with no references">Variables</span></span> =                     [<span class="cons_String">(</span>[{<a href="#ID_246_5" id="ID_127_57" title="a reference to a single-file definition">ID</a> <span class="cons_Lit">", "</span>}*]<span class="cons_String">)</span>]
    <a href="#OptVariableList_69_64" id="OptVariableList_128_5" title="a definition with a single reference">OptVariableList</a>.<span class="cons_Constructor"><span id="NoVariables_128_21" title="a definition with no references">NoVariables</span></span> =                   []

    <a href="#VariableList_101_75" id="VariableList_130_5" title="a definition with a single reference">VariableList</a>.<span class="cons_Constructor"><span id="VariableList_130_18" title="a definition with no references">VariableList</span></span> =                     [<span class="cons_String">(</span>[{<a href="#ID_246_5" id="ID_130_57" title="a reference to a single-file definition">ID</a> <span class="cons_Lit">", "</span>}*]<span class="cons_String">)</span>]


    <span class="layout">// === Expressions =======</span>

    <button class="modal-open" id="Expression_135_5" title="a definition with multiple references" data-urls="#Expression line 47_56, 71_13, 76_13, 88_16, 93_17, 99_57, 114_16, 121_57, 124_57, 149_13, 150_14, 154_13, 155_14, 157_14, 161_16, 162_14, 166_17, 177_56, 191_57, 194_57, 198_16, 199_14, 202_14; ../Poosl.sdf3/#Expression line 85_14, 90_14, 95_14, 198_67">Expression</button>.<span class="cons_Constructor"><span id="ExpressionSequence_135_16" title="a definition with no references">ExpressionSequence</span></span> =                 [[{<a href="#SingleExpression_17_5" id="SingleExpression_135_56" title="a reference to a single-file definition">SingleExpression</a> <span class="cons_Lit">";\n"</span>}+]]

    <span class="layout">// --- Level 1 -------</span>
    <button class="modal-open" id="SingleExpression_138_5" title="a definition with multiple references" data-urls="#SingleExpression line 46_61, 98_53, 135_56, 138_63, 139_62, 141_55, 141_97, 142_55, 142_97, 143_55, 143_97, 145_55, 147_70, 232_11, 233_11, 234_11, 235_11, 236_11, 238_5, 239_9, 240_9, 241_9, 242_9, 243_11, 243_49">SingleExpression</button>.<span class="cons_Constructor"><a href="#AssignmentExpression_243_28" id="AssignmentExpression_138_22" title="a definition with a single reference">AssignmentExpression</a></span> =         [[<a href="#ID_246_5" id="ID_138_55" title="a reference to a single-file definition">ID</a>] <span class="cons_String">:=</span> [<a href="#SingleExpression_17_5" id="SingleExpression_138_63" title="a reference to a single-file definition">SingleExpression</a>]]
    <button class="modal-open" id="SingleExpression_139_5" title="a definition with multiple references" data-urls="#SingleExpression line 46_61, 98_53, 135_56, 138_63, 139_62, 141_55, 141_97, 142_55, 142_97, 143_55, 143_97, 145_55, 147_70, 232_11, 233_11, 234_11, 235_11, 236_11, 238_5, 239_9, 240_9, 241_9, 242_9, 243_11, 243_49">SingleExpression</button>.<span class="cons_Constructor"><a href="#ReturnExpression_243_66" id="ReturnExpression_139_22" title="a definition with a single reference">ReturnExpression</a></span> =             [<span class="cons_String">return</span> [<a href="#SingleExpression_17_5" id="SingleExpression_139_62" title="a reference to a single-file definition">SingleExpression</a>]]
    <span class="layout">// --- Level 2-4  -------   </span>
    <button class="modal-open" id="SingleExpression_141_5" title="a definition with multiple references" data-urls="#SingleExpression line 46_61, 98_53, 135_56, 138_63, 139_62, 141_55, 141_97, 142_55, 142_97, 143_55, 143_97, 145_55, 147_70, 232_11, 233_11, 234_11, 235_11, 236_11, 238_5, 239_9, 240_9, 241_9, 242_9, 243_11, 243_49">SingleExpression</button>.<span class="cons_Constructor"><a href="#BinaryOperatorExpression2_242_26" id="BinaryOperatorExpression2_141_22" title="a definition with a single reference">BinaryOperatorExpression2</a></span> =    [[<a href="#SingleExpression_17_5" id="SingleExpression_141_55" title="a reference to a single-file definition">SingleExpression</a>] [<a href="#BinaryOperatorLevel2_27_5" id="BinaryOperatorLevel2_141_74" title="a reference to a single-file definition">BinaryOperatorLevel2</a>] [<a href="#SingleExpression_17_5" id="SingleExpression_141_97" title="a reference to a single-file definition">SingleExpression</a>]]  {<span class="keyword">left</span>}
    <button class="modal-open" id="SingleExpression_142_5" title="a definition with multiple references" data-urls="#SingleExpression line 46_61, 98_53, 135_56, 138_63, 139_62, 141_55, 141_97, 142_55, 142_97, 143_55, 143_97, 145_55, 147_70, 232_11, 233_11, 234_11, 235_11, 236_11, 238_5, 239_9, 240_9, 241_9, 242_9, 243_11, 243_49">SingleExpression</button>.<span class="cons_Constructor"><a href="#BinaryOperatorExpression3_241_26" id="BinaryOperatorExpression3_142_22" title="a definition with a single reference">BinaryOperatorExpression3</a></span> =    [[<a href="#SingleExpression_17_5" id="SingleExpression_142_55" title="a reference to a single-file definition">SingleExpression</a>] [<a href="#BinaryOperatorLevel3_28_5" id="BinaryOperatorLevel3_142_74" title="a reference to a single-file definition">BinaryOperatorLevel3</a>] [<a href="#SingleExpression_17_5" id="SingleExpression_142_97" title="a reference to a single-file definition">SingleExpression</a>]]  {<span class="keyword">left</span>}
    <button class="modal-open" id="SingleExpression_143_5" title="a definition with multiple references" data-urls="#SingleExpression line 46_61, 98_53, 135_56, 138_63, 139_62, 141_55, 141_97, 142_55, 142_97, 143_55, 143_97, 145_55, 147_70, 232_11, 233_11, 234_11, 235_11, 236_11, 238_5, 239_9, 240_9, 241_9, 242_9, 243_11, 243_49">SingleExpression</button>.<span class="cons_Constructor"><a href="#BinaryOperatorExpression4_240_26" id="BinaryOperatorExpression4_143_22" title="a definition with a single reference">BinaryOperatorExpression4</a></span> =    [[<a href="#SingleExpression_17_5" id="SingleExpression_143_55" title="a reference to a single-file definition">SingleExpression</a>] [<a href="#BinaryOperatorLevel4_29_5" id="BinaryOperatorLevel4_143_74" title="a reference to a single-file definition">BinaryOperatorLevel4</a>] [<a href="#SingleExpression_17_5" id="SingleExpression_143_97" title="a reference to a single-file definition">SingleExpression</a>]]  {<span class="keyword">left</span>}
    <span class="layout">// --- Level 5 -------</span>
    <button class="modal-open" id="SingleExpression_145_5" title="a definition with multiple references" data-urls="#SingleExpression line 46_61, 98_53, 135_56, 138_63, 139_62, 141_55, 141_97, 142_55, 142_97, 143_55, 143_97, 145_55, 147_70, 232_11, 233_11, 234_11, 235_11, 236_11, 238_5, 239_9, 240_9, 241_9, 242_9, 243_11, 243_49">SingleExpression</button>.<span class="cons_Constructor"><a href="#DataMethodCallExpression_239_26" id="DataMethodCallExpression_145_22" title="a definition with a single reference">DataMethodCallExpression</a></span> =     [[<a href="#SingleExpression_17_5" id="SingleExpression_145_55" title="a reference to a single-file definition">SingleExpression</a>][<a href="#OnSuperClass_18_5" id="OnSuperClass_145_73" title="a reference to a single-file definition">OnSuperClass</a>] [<a href="#ID_246_5" id="ID_145_88" title="a reference to a single-file definition">ID</a>][<a href="#OptExpressionList_19_5" id="OptExpressionList_145_92" title="a reference to a single-file definition">OptExpressionList</a>]]
    <span class="layout">// --- Level 6 -------</span>
    <button class="modal-open" id="SingleExpression_147_5" title="a definition with multiple references" data-urls="#SingleExpression line 46_61, 98_53, 135_56, 138_63, 139_62, 141_55, 141_97, 142_55, 142_97, 143_55, 143_97, 145_55, 147_70, 232_11, 233_11, 234_11, 235_11, 236_11, 238_5, 239_9, 240_9, 241_9, 242_9, 243_11, 243_49">SingleExpression</button>.<span class="cons_Constructor"><a href="#UnaryOperatorExpression_238_22" id="UnaryOperatorExpression_147_22" title="a definition with a single reference">UnaryOperatorExpression</a></span> =      [[<a href="#UnaryOperator_26_5" id="UnaryOperator_147_55" title="a reference to a single-file definition">UnaryOperator</a>][<a href="#SingleExpression_17_5" id="SingleExpression_147_70" title="a reference to a single-file definition">SingleExpression</a>]]
    <button class="modal-open" id="SingleExpression_148_5" title="a definition with multiple references" data-urls="#SingleExpression line 46_61, 98_53, 135_56, 138_63, 139_62, 141_55, 141_97, 142_55, 142_97, 143_55, 143_97, 145_55, 147_70, 232_11, 233_11, 234_11, 235_11, 236_11, 238_5, 239_9, 240_9, 241_9, 242_9, 243_11, 243_49">SingleExpression</button>.<span class="cons_Constructor"><a href="#IfThenExpression_233_28" id="IfThenExpression_148_22" title="a definition with a single reference">IfThenExpression</a></span> = [
        <span class="cons_String">if</span> [<a href="#Expression_16_5" id="Expression_149_13" title="a reference to a single-file definition">Expression</a>] <span class="cons_String">then</span>
            [<a href="#Expression_16_5" id="Expression_150_14" title="a reference to a single-file definition">Expression</a>]
        <span class="cons_String">fi</span>
        ]
    <button class="modal-open" id="SingleExpression_153_5" title="a definition with multiple references" data-urls="#SingleExpression line 46_61, 98_53, 135_56, 138_63, 139_62, 141_55, 141_97, 142_55, 142_97, 143_55, 143_97, 145_55, 147_70, 232_11, 233_11, 234_11, 235_11, 236_11, 238_5, 239_9, 240_9, 241_9, 242_9, 243_11, 243_49">SingleExpression</button>.<span class="cons_Constructor"><a href="#IfThenElseExpression_234_28" id="IfThenElseExpression_153_22" title="a definition with a single reference">IfThenElseExpression</a></span> = [
        <span class="cons_String">if</span> [<a href="#Expression_16_5" id="Expression_154_13" title="a reference to a single-file definition">Expression</a>] <span class="cons_String">then</span>
            [<a href="#Expression_16_5" id="Expression_155_14" title="a reference to a single-file definition">Expression</a>]
        <span class="cons_String">else</span>
            [<a href="#Expression_16_5" id="Expression_157_14" title="a reference to a single-file definition">Expression</a>]
        <span class="cons_String">fi</span>
        ]
    <button class="modal-open" id="SingleExpression_160_5" title="a definition with multiple references" data-urls="#SingleExpression line 46_61, 98_53, 135_56, 138_63, 139_62, 141_55, 141_97, 142_55, 142_97, 143_55, 143_97, 145_55, 147_70, 232_11, 233_11, 234_11, 235_11, 236_11, 238_5, 239_9, 240_9, 241_9, 242_9, 243_11, 243_49">SingleExpression</button>.<span class="cons_Constructor"><a href="#WhileExpression_235_28" id="WhileExpression_160_22" title="a definition with a single reference">WhileExpression</a></span> = [
        <span class="cons_String">while</span> [<a href="#Expression_16_5" id="Expression_161_16" title="a reference to a single-file definition">Expression</a>] <span class="cons_String">do</span>
            [<a href="#Expression_16_5" id="Expression_162_14" title="a reference to a single-file definition">Expression</a>]
        <span class="cons_String">od</span>
        ]
    <button class="modal-open" id="SingleExpression_165_5" title="a definition with multiple references" data-urls="#SingleExpression line 46_61, 98_53, 135_56, 138_63, 139_62, 141_55, 141_97, 142_55, 142_97, 143_55, 143_97, 145_55, 147_70, 232_11, 233_11, 234_11, 235_11, 236_11, 238_5, 239_9, 240_9, 241_9, 242_9, 243_11, 243_49">SingleExpression</button>.<span class="cons_Constructor"><a href="#SwitchExpression_236_28" id="SwitchExpression_165_22" title="a definition with a single reference">SwitchExpression</a></span> = [
        <span class="cons_String">switch</span> [<a href="#Expression_16_5" id="Expression_166_17" title="a reference to a single-file definition">Expression</a>] <span class="cons_String">do</span>
            [<a href="#CaseExpressionList_22_5" id="CaseExpressionList_167_14" title="a reference to a single-file definition">CaseExpressionList</a>]
            [<a href="#OptDefaultExpression_24_5" id="OptDefaultExpression_168_14" title="a reference to a single-file definition">OptDefaultExpression</a>]
        <span class="cons_String">od</span>
        ]
    <span class="layout">// --- Level 7 -------</span>
    <button class="modal-open" id="SingleExpression_172_5" title="a definition with multiple references" data-urls="#SingleExpression line 46_61, 98_53, 135_56, 138_63, 139_62, 141_55, 141_97, 142_55, 142_97, 143_55, 143_97, 145_55, 147_70, 232_11, 233_11, 234_11, 235_11, 236_11, 238_5, 239_9, 240_9, 241_9, 242_9, 243_11, 243_49">SingleExpression</button>.<span class="cons_Constructor"><span id="CurrentTimeExpression_172_22" title="a definition with no references">CurrentTimeExpression</span></span> =        [<span class="cons_String">currentTime</span>]
    <button class="modal-open" id="SingleExpression_173_5" title="a definition with multiple references" data-urls="#SingleExpression line 46_61, 98_53, 135_56, 138_63, 139_62, 141_55, 141_97, 142_55, 142_97, 143_55, 143_97, 145_55, 147_70, 232_11, 233_11, 234_11, 235_11, 236_11, 238_5, 239_9, 240_9, 241_9, 242_9, 243_11, 243_49">SingleExpression</button>.<span class="cons_Constructor"><span id="SelfExpression_173_22" title="a definition with no references">SelfExpression</span></span> =               [<span class="cons_String">self</span>]
    <button class="modal-open" id="SingleExpression_174_5" title="a definition with multiple references" data-urls="#SingleExpression line 46_61, 98_53, 135_56, 138_63, 139_62, 141_55, 141_97, 142_55, 142_97, 143_55, 143_97, 145_55, 147_70, 232_11, 233_11, 234_11, 235_11, 236_11, 238_5, 239_9, 240_9, 241_9, 242_9, 243_11, 243_49">SingleExpression</button>.<span class="cons_Constructor"><span id="ConstantExpression_174_22" title="a definition with no references">ConstantExpression</span></span> =           <a href="#ExpressionConstant_25_5" id="ExpressionConstant_174_53" title="a reference to a single-file definition">ExpressionConstant</a>
    <button class="modal-open" id="SingleExpression_175_5" title="a definition with multiple references" data-urls="#SingleExpression line 46_61, 98_53, 135_56, 138_63, 139_62, 141_55, 141_97, 142_55, 142_97, 143_55, 143_97, 145_55, 147_70, 232_11, 233_11, 234_11, 235_11, 236_11, 238_5, 239_9, 240_9, 241_9, 242_9, 243_11, 243_49">SingleExpression</button>.<span class="cons_Constructor"><span id="NewExpression_175_22" title="a definition with no references">NewExpression</span></span> =                [<span class="cons_String">new</span> <span class="cons_String">(</span>[<a href="#ID_246_5" id="ID_175_60" title="a reference to a single-file definition">ID</a>]<span class="cons_String">)</span>]
    <button class="modal-open" id="SingleExpression_176_5" title="a definition with multiple references" data-urls="#SingleExpression line 46_61, 98_53, 135_56, 138_63, 139_62, 141_55, 141_97, 142_55, 142_97, 143_55, 143_97, 145_55, 147_70, 232_11, 233_11, 234_11, 235_11, 236_11, 238_5, 239_9, 240_9, 241_9, 242_9, 243_11, 243_49">SingleExpression</button>.<span class="cons_Constructor"><span id="VariableExpression_176_22" title="a definition with no references">VariableExpression</span></span> =           <a href="#ID_246_5" id="ID_176_53" title="a reference to a single-file definition">ID</a>
    <button class="modal-open" id="SingleExpression_177_5" title="a definition with multiple references" data-urls="#SingleExpression line 46_61, 98_53, 135_56, 138_63, 139_62, 141_55, 141_97, 142_55, 142_97, 143_55, 143_97, 145_55, 147_70, 232_11, 233_11, 234_11, 235_11, 236_11, 238_5, 239_9, 240_9, 241_9, 242_9, 243_11, 243_49">SingleExpression</button>.<span class="cons_Constructor"><a href="#RoundBracketExpression_232_28" id="RoundBracketExpression_177_22" title="a definition with a single reference">RoundBracketExpression</a></span> =       [<span class="cons_String">(</span>[<a href="#Expression_16_5" id="Expression_177_56" title="a reference to a single-file definition">Expression</a>]<span class="cons_String">)</span>]

    <button class="modal-open" id="ExpressionConstant_179_5" title="a definition with multiple references" data-urls="#ExpressionConstant line 174_53; ../Poosl.sdf3/#ExpressionConstant line 67_61">ExpressionConstant</button>.<span class="cons_Constructor"><span id="BooleanConstant_179_24" title="a definition with no references">BooleanConstant</span></span> =            <a href="../Common.sdf3/#BOOL_17_3" id="BOOL_179_53" title="a reference to a single-file definition">BOOL</a>
    <button class="modal-open" id="ExpressionConstant_180_5" title="a definition with multiple references" data-urls="#ExpressionConstant line 174_53; ../Poosl.sdf3/#ExpressionConstant line 67_61">ExpressionConstant</button>.<span class="cons_Constructor"><span id="CharacterConstant_180_24" title="a definition with no references">CharacterConstant</span></span> =          <a href="../Common.sdf3/#CHARACTER_62_10" id="CHARACTER_180_53" title="a reference to a single-file definition">CHARACTER</a>
    <button class="modal-open" id="ExpressionConstant_181_5" title="a definition with multiple references" data-urls="#ExpressionConstant line 174_53; ../Poosl.sdf3/#ExpressionConstant line 67_61">ExpressionConstant</button>.<span class="cons_Constructor"><span id="FloatConstant_181_24" title="a definition with no references">FloatConstant</span></span> =              <a href="../Common.sdf3/#FLOAT_29_12" id="FLOAT_181_53" title="a reference to a single-file definition">FLOAT</a>
    <button class="modal-open" id="ExpressionConstant_182_5" title="a definition with multiple references" data-urls="#ExpressionConstant line 174_53; ../Poosl.sdf3/#ExpressionConstant line 67_61">ExpressionConstant</button>.<span class="cons_Constructor"><span id="IntegerConstant_182_24" title="a definition with no references">IntegerConstant</span></span> =            <a href="../Common.sdf3/#INT_29_3" id="INT_182_53" title="a reference to a single-file definition">INT</a>
    <button class="modal-open" id="ExpressionConstant_183_5" title="a definition with multiple references" data-urls="#ExpressionConstant line 174_53; ../Poosl.sdf3/#ExpressionConstant line 67_61">ExpressionConstant</button>.<span class="cons_Constructor"><span id="NilConstant_183_24" title="a definition with no references">NilConstant</span></span> =                [<span class="cons_String">nil</span>]
    <button class="modal-open" id="ExpressionConstant_184_5" title="a definition with multiple references" data-urls="#ExpressionConstant line 174_53; ../Poosl.sdf3/#ExpressionConstant line 67_61">ExpressionConstant</button>.<span class="cons_Constructor"><span id="RealConstant_184_24" title="a definition with no references">RealConstant</span></span> =               <a href="../Common.sdf3/#REAL_29_7" id="REAL_184_53" title="a reference to a single-file definition">REAL</a>
    <button class="modal-open" id="ExpressionConstant_185_5" title="a definition with multiple references" data-urls="#ExpressionConstant line 174_53; ../Poosl.sdf3/#ExpressionConstant line 67_61">ExpressionConstant</button>.<span class="cons_Constructor"><span id="StringConstant_185_24" title="a definition with no references">StringConstant</span></span> =             <a href="../Common.sdf3/#STRING_62_3" id="STRING_185_53" title="a reference to a single-file definition">STRING</a>
    <button class="modal-open" id="ExpressionConstant_186_5" title="a definition with multiple references" data-urls="#ExpressionConstant line 174_53; ../Poosl.sdf3/#ExpressionConstant line 67_61">ExpressionConstant</button>.<span class="cons_Constructor"><span id="EnvironmentConstant_186_24" title="a definition with no references">EnvironmentConstant</span></span> =        <a href="../Common.sdf3/#ENV_6_6" id="ENV_186_53" title="a reference to a single-file definition">ENV</a>

    <a href="#OnSuperClass_145_73" id="OnSuperClass_188_5" title="a definition with a single reference">OnSuperClass</a>.<span class="cons_Constructor"><span id="OnSuperClass_188_18" title="a definition with no references">OnSuperClass</span></span> =                     [<span class="cons_String">^</span>]
    <a href="#OnSuperClass_145_73" id="OnSuperClass_189_5" title="a definition with a single reference">OnSuperClass</a>.<span class="cons_Constructor"><span id="NotOnSuperClass_189_18" title="a definition with no references">NotOnSuperClass</span></span> =                  []

    <button class="modal-open" id="OptExpressionList_191_5" title="a definition with multiple references" data-urls="#OptExpressionList line 68_64, 145_92">OptExpressionList</button>.<span class="cons_Constructor"><span id="Expressions_191_23" title="a definition with no references">Expressions</span></span> =                 [<span class="cons_String">(</span>[{<a href="#Expression_16_5" id="Expression_191_57" title="a reference to a single-file definition">Expression</a> <span class="cons_Lit">", "</span>}*]<span class="cons_String">)</span>]
    <button class="modal-open" id="OptExpressionList_192_5" title="a definition with multiple references" data-urls="#OptExpressionList line 68_64, 145_92">OptExpressionList</button>.<span class="cons_Constructor"><span id="NoExpressions_192_23" title="a definition with no references">NoExpressions</span></span> =               []

    <a href="#ExpressionList_101_59" id="ExpressionList_194_5" title="a definition with a single reference">ExpressionList</a>.<span class="cons_Constructor"><span id="ExpressionList_194_20" title="a definition with no references">ExpressionList</span></span> =                 [<span class="cons_String">(</span>[{<a href="#Expression_16_5" id="Expression_194_57" title="a reference to a single-file definition">Expression</a> <span class="cons_Lit">", "</span>}*]<span class="cons_String">)</span>]

    <a href="#CaseExpressionList_167_14" id="CaseExpressionList_196_5" title="a definition with a single reference">CaseExpressionList</a>.<span class="cons_Constructor"><span id="CaseExpressionList_196_24" title="a definition with no references">CaseExpressionList</span></span> =         [[{<a href="#CaseExpression_23_5" id="CaseExpression_196_56" title="a reference to a single-file definition">CaseExpression</a> <span class="cons_Lit">"\n"</span>}*]]
    <a href="#CaseExpression_196_56" id="CaseExpression_197_5" title="a definition with a single reference">CaseExpression</a>.<span class="cons_Constructor"><span id="CaseExpression_197_20" title="a definition with no references">CaseExpression</span></span> =
        [<span class="cons_String">case</span> [<a href="#Expression_16_5" id="Expression_198_16" title="a reference to a single-file definition">Expression</a>] <span class="cons_String">then</span>
            [<a href="#Expression_16_5" id="Expression_199_14" title="a reference to a single-file definition">Expression</a>]]
    <a href="#OptDefaultExpression_168_14" id="OptDefaultExpression_200_5" title="a definition with a single reference">OptDefaultExpression</a>.<span class="cons_Constructor"><span id="DefaultExpression_200_26" title="a definition with no references">DefaultExpression</span></span> =
        [<span class="cons_String">default</span>
            [<a href="#Expression_16_5" id="Expression_202_14" title="a reference to a single-file definition">Expression</a>]]
    <a href="#OptDefaultExpression_168_14" id="OptDefaultExpression_203_5" title="a definition with a single reference">OptDefaultExpression</a>.<span class="cons_Constructor"><span id="NoDefaultExpression_203_26" title="a definition with no references">NoDefaultExpression</span></span> =      []

    <span class="layout">// --- Operators -------</span>
    <button class="modal-open" id="UnaryOperator_206_5" title="a definition with multiple references" data-urls="#UnaryOperator line 147_55, 227_5; ../Poosl.sdf3/#UnaryOperator line 89_10, 101_17">UnaryOperator</button>.<span class="cons_Constructor"><span id="Minus_206_19" title="a definition with no references">Minus</span></span> =                           [<span class="cons_String">-</span>]
    <button class="modal-open" id="UnaryOperator_207_5" title="a definition with multiple references" data-urls="#UnaryOperator line 147_55, 227_5; ../Poosl.sdf3/#UnaryOperator line 89_10, 101_17">UnaryOperator</button>.<span class="cons_Constructor"><span id="Not_207_19" title="a definition with no references">Not</span></span> =                             [<span class="cons_String">!</span>]

    <button class="modal-open" id="BinaryOperatorLevel2_209_5" title="a definition with multiple references" data-urls="#BinaryOperatorLevel2 line 141_74; ../Poosl.sdf3/#BinaryOperatorLevel2 line 110_57">BinaryOperatorLevel2</button>.<span class="cons_Constructor"><span id="Equal_209_26" title="a definition with no references">Equal</span></span> =                    [<span class="cons_String">=</span>]
    <button class="modal-open" id="BinaryOperatorLevel2_210_5" title="a definition with multiple references" data-urls="#BinaryOperatorLevel2 line 141_74; ../Poosl.sdf3/#BinaryOperatorLevel2 line 110_57">BinaryOperatorLevel2</button>.<span class="cons_Constructor"><span id="Unequal_210_26" title="a definition with no references">Unequal</span></span> =                  [<span class="cons_String">!=</span>]
    <button class="modal-open" id="BinaryOperatorLevel2_211_5" title="a definition with multiple references" data-urls="#BinaryOperatorLevel2 line 141_74; ../Poosl.sdf3/#BinaryOperatorLevel2 line 110_57">BinaryOperatorLevel2</button>.<span class="cons_Constructor"><span id="Identical_211_26" title="a definition with no references">Identical</span></span> =                [<span class="cons_String">==</span>]
    <button class="modal-open" id="BinaryOperatorLevel2_212_5" title="a definition with multiple references" data-urls="#BinaryOperatorLevel2 line 141_74; ../Poosl.sdf3/#BinaryOperatorLevel2 line 110_57">BinaryOperatorLevel2</button>.<span class="cons_Constructor"><span id="NotIdentical_212_26" title="a definition with no references">NotIdentical</span></span> =             [<span class="cons_String">!==</span>]
    <button class="modal-open" id="BinaryOperatorLevel2_213_5" title="a definition with multiple references" data-urls="#BinaryOperatorLevel2 line 141_74; ../Poosl.sdf3/#BinaryOperatorLevel2 line 110_57">BinaryOperatorLevel2</button>.<span class="cons_Constructor"><span id="LessThan_213_26" title="a definition with no references">LessThan</span></span> =                 [<span class="cons_String">&lt;</span>]
    <button class="modal-open" id="BinaryOperatorLevel2_214_5" title="a definition with multiple references" data-urls="#BinaryOperatorLevel2 line 141_74; ../Poosl.sdf3/#BinaryOperatorLevel2 line 110_57">BinaryOperatorLevel2</button>.<span class="cons_Constructor"><span id="AtMost_214_26" title="a definition with no references">AtMost</span></span> =                   [<span class="cons_String">&lt;=</span>]
    <button class="modal-open" id="BinaryOperatorLevel2_215_5" title="a definition with multiple references" data-urls="#BinaryOperatorLevel2 line 141_74; ../Poosl.sdf3/#BinaryOperatorLevel2 line 110_57">BinaryOperatorLevel2</button>.<span class="cons_Constructor"><span id="GreaterThan_215_26" title="a definition with no references">GreaterThan</span></span> =              [<span class="cons_String">&gt;</span>]
    <button class="modal-open" id="BinaryOperatorLevel2_216_5" title="a definition with multiple references" data-urls="#BinaryOperatorLevel2 line 141_74; ../Poosl.sdf3/#BinaryOperatorLevel2 line 110_57">BinaryOperatorLevel2</button>.<span class="cons_Constructor"><span id="AtLeast_216_26" title="a definition with no references">AtLeast</span></span> =                  [<span class="cons_String">&gt;=</span>]

    <button class="modal-open" id="BinaryOperatorLevel3_218_5" title="a definition with multiple references" data-urls="#BinaryOperatorLevel3 line 142_74; ../Poosl.sdf3/#BinaryOperatorLevel3 line 111_57">BinaryOperatorLevel3</button>.<span class="cons_Constructor"><span id="Add_218_26" title="a definition with no references">Add</span></span> =                      [<span class="cons_String">+</span>]
    <button class="modal-open" id="BinaryOperatorLevel3_219_5" title="a definition with multiple references" data-urls="#BinaryOperatorLevel3 line 142_74; ../Poosl.sdf3/#BinaryOperatorLevel3 line 111_57">BinaryOperatorLevel3</button>.<span class="cons_Constructor"><span id="Subtract_219_26" title="a definition with no references">Subtract</span></span> =                 [<span class="cons_String">-</span>]
    <button class="modal-open" id="BinaryOperatorLevel3_220_5" title="a definition with multiple references" data-urls="#BinaryOperatorLevel3 line 142_74; ../Poosl.sdf3/#BinaryOperatorLevel3 line 111_57">BinaryOperatorLevel3</button>.<span class="cons_Constructor"><span id="And_220_26" title="a definition with no references">And</span></span> =                      [<span class="cons_String">&amp;</span>]
    <button class="modal-open" id="BinaryOperatorLevel3_221_5" title="a definition with multiple references" data-urls="#BinaryOperatorLevel3 line 142_74; ../Poosl.sdf3/#BinaryOperatorLevel3 line 111_57">BinaryOperatorLevel3</button>.<span class="cons_Constructor"><span id="Or_221_26" title="a definition with no references">Or</span></span> =                       [<span class="cons_String">|</span>]
    
    <button class="modal-open" id="BinaryOperatorLevel4_223_5" title="a definition with multiple references" data-urls="#BinaryOperatorLevel4 line 143_74; ../Poosl.sdf3/#BinaryOperatorLevel4 line 112_57">BinaryOperatorLevel4</button>.<span class="cons_Constructor"><span id="Multiply_223_26" title="a definition with no references">Multiply</span></span> =                 [<span class="cons_String">*</span>]
    <button class="modal-open" id="BinaryOperatorLevel4_224_5" title="a definition with multiple references" data-urls="#BinaryOperatorLevel4 line 143_74; ../Poosl.sdf3/#BinaryOperatorLevel4 line 112_57">BinaryOperatorLevel4</button>.<span class="cons_Constructor"><span id="Divide_224_26" title="a definition with no references">Divide</span></span> =                   [<span class="cons_String">/</span>]

<span class="keyword">context-free restrictions</span>
    <a href="#UnaryOperator_26_5" id="UnaryOperator_227_5" title="a reference to a single-file definition">UnaryOperator</a> -/- [<span class="cons_Regular">0</span>-<span class="cons_Regular">9</span>]                         <span class="layout">// Parse -42 as Integer instead of UnaryOperation (but 42-0 should be allowed)</span>

<span class="keyword">context-free priorities</span>
    <span class="layout">// If A &gt; B, then all trees are removed that have a B node as a direct child of an A node.</span>
    <a href="#SingleStatement_8_5" id="SingleStatement_231_5" title="a reference to a single-file definition">SingleStatement</a>.<span class="cons_Constructor"><a href="#ExpressionStatement_98_21" id="ExpressionStatement_231_21" title="a reference to a single-file definition">ExpressionStatement</a></span> &lt;0&gt; &gt;
        { <a href="#SingleExpression_17_5" id="SingleExpression_232_11" title="a reference to a single-file definition">SingleExpression</a>.<span class="cons_Constructor"><a href="#RoundBracketExpression_177_22" id="RoundBracketExpression_232_28" title="a reference to a single-file definition">RoundBracketExpression</a></span>
          <a href="#SingleExpression_17_5" id="SingleExpression_233_11" title="a reference to a single-file definition">SingleExpression</a>.<span class="cons_Constructor"><a href="#IfThenExpression_148_22" id="IfThenExpression_233_28" title="a reference to a single-file definition">IfThenExpression</a></span>
          <a href="#SingleExpression_17_5" id="SingleExpression_234_11" title="a reference to a single-file definition">SingleExpression</a>.<span class="cons_Constructor"><a href="#IfThenElseExpression_153_22" id="IfThenElseExpression_234_28" title="a reference to a single-file definition">IfThenElseExpression</a></span>
          <a href="#SingleExpression_17_5" id="SingleExpression_235_11" title="a reference to a single-file definition">SingleExpression</a>.<span class="cons_Constructor"><a href="#WhileExpression_160_22" id="WhileExpression_235_28" title="a reference to a single-file definition">WhileExpression</a></span>
          <a href="#SingleExpression_17_5" id="SingleExpression_236_11" title="a reference to a single-file definition">SingleExpression</a>.<span class="cons_Constructor"><a href="#SwitchExpression_165_22" id="SwitchExpression_236_28" title="a reference to a single-file definition">SwitchExpression</a></span>},

    <a href="#SingleExpression_17_5" id="SingleExpression_238_5" title="a reference to a single-file definition">SingleExpression</a>.<span class="cons_Constructor"><a href="#UnaryOperatorExpression_147_22" id="UnaryOperatorExpression_238_22" title="a reference to a single-file definition">UnaryOperatorExpression</a></span> &gt;
        <a href="#SingleExpression_17_5" id="SingleExpression_239_9" title="a reference to a single-file definition">SingleExpression</a>.<span class="cons_Constructor"><a href="#DataMethodCallExpression_145_22" id="DataMethodCallExpression_239_26" title="a reference to a single-file definition">DataMethodCallExpression</a></span> &gt;
        <a href="#SingleExpression_17_5" id="SingleExpression_240_9" title="a reference to a single-file definition">SingleExpression</a>.<span class="cons_Constructor"><a href="#BinaryOperatorExpression4_143_22" id="BinaryOperatorExpression4_240_26" title="a reference to a single-file definition">BinaryOperatorExpression4</a></span> &gt;
        <a href="#SingleExpression_17_5" id="SingleExpression_241_9" title="a reference to a single-file definition">SingleExpression</a>.<span class="cons_Constructor"><a href="#BinaryOperatorExpression3_142_22" id="BinaryOperatorExpression3_241_26" title="a reference to a single-file definition">BinaryOperatorExpression3</a></span> &gt;
        <a href="#SingleExpression_17_5" id="SingleExpression_242_9" title="a reference to a single-file definition">SingleExpression</a>.<span class="cons_Constructor"><a href="#BinaryOperatorExpression2_141_22" id="BinaryOperatorExpression2_242_26" title="a reference to a single-file definition">BinaryOperatorExpression2</a></span> &gt;
        { <a href="#SingleExpression_17_5" id="SingleExpression_243_11" title="a reference to a single-file definition">SingleExpression</a>.<span class="cons_Constructor"><a href="#AssignmentExpression_138_22" id="AssignmentExpression_243_28" title="a reference to a single-file definition">AssignmentExpression</a></span> <a href="#SingleExpression_17_5" id="SingleExpression_243_49" title="a reference to a single-file definition">SingleExpression</a>.<span class="cons_Constructor"><a href="#ReturnExpression_139_22" id="ReturnExpression_243_66" title="a reference to a single-file definition">ReturnExpression</a></span> }

<span class="keyword">lexical syntax</span>      <span class="layout">// keywords</span>
    <button class="modal-open" id="ID_246_5" title="a definition with multiple references" data-urls="#ID line 68_55, 68_60, 69_55, 69_60, 101_55, 127_57, 130_57, 138_55, 145_88, 175_60, 176_53">ID</button> = <span class="cons_Lit">"if"</span>           {<span class="keyword">reject</span>}
    <button class="modal-open" id="ID_247_5" title="a definition with multiple references" data-urls="#ID line 68_55, 68_60, 69_55, 69_60, 101_55, 127_57, 130_57, 138_55, 145_88, 175_60, 176_53">ID</button> = <span class="cons_Lit">"then"</span>         {<span class="keyword">reject</span>}
    <button class="modal-open" id="ID_248_5" title="a definition with multiple references" data-urls="#ID line 68_55, 68_60, 69_55, 69_60, 101_55, 127_57, 130_57, 138_55, 145_88, 175_60, 176_53">ID</button> = <span class="cons_Lit">"else"</span>         {<span class="keyword">reject</span>}
    <button class="modal-open" id="ID_249_5" title="a definition with multiple references" data-urls="#ID line 68_55, 68_60, 69_55, 69_60, 101_55, 127_57, 130_57, 138_55, 145_88, 175_60, 176_53">ID</button> = <span class="cons_Lit">"fi"</span>           {<span class="keyword">reject</span>}

    <button class="modal-open" id="ID_251_5" title="a definition with multiple references" data-urls="#ID line 68_55, 68_60, 69_55, 69_60, 101_55, 127_57, 130_57, 138_55, 145_88, 175_60, 176_53">ID</button> = <span class="cons_Lit">"while"</span>        {<span class="keyword">reject</span>}
    <button class="modal-open" id="ID_252_5" title="a definition with multiple references" data-urls="#ID line 68_55, 68_60, 69_55, 69_60, 101_55, 127_57, 130_57, 138_55, 145_88, 175_60, 176_53">ID</button> = <span class="cons_Lit">"do"</span>           {<span class="keyword">reject</span>}
    <button class="modal-open" id="ID_253_5" title="a definition with multiple references" data-urls="#ID line 68_55, 68_60, 69_55, 69_60, 101_55, 127_57, 130_57, 138_55, 145_88, 175_60, 176_53">ID</button> = <span class="cons_Lit">"od"</span>           {<span class="keyword">reject</span>}

    <button class="modal-open" id="ID_255_5" title="a definition with multiple references" data-urls="#ID line 68_55, 68_60, 69_55, 69_60, 101_55, 127_57, 130_57, 138_55, 145_88, 175_60, 176_53">ID</button> = <span class="cons_Lit">"switch"</span>       {<span class="keyword">reject</span>}
    <button class="modal-open" id="ID_256_5" title="a definition with multiple references" data-urls="#ID line 68_55, 68_60, 69_55, 69_60, 101_55, 127_57, 130_57, 138_55, 145_88, 175_60, 176_53">ID</button> = <span class="cons_Lit">"case"</span>         {<span class="keyword">reject</span>}
    <button class="modal-open" id="ID_257_5" title="a definition with multiple references" data-urls="#ID line 68_55, 68_60, 69_55, 69_60, 101_55, 127_57, 130_57, 138_55, 145_88, 175_60, 176_53">ID</button> = <span class="cons_Lit">"default"</span>      {<span class="keyword">reject</span>}

    <button class="modal-open" id="ID_259_5" title="a definition with multiple references" data-urls="#ID line 68_55, 68_60, 69_55, 69_60, 101_55, 127_57, 130_57, 138_55, 145_88, 175_60, 176_53">ID</button> = <span class="cons_Lit">"par"</span>          {<span class="keyword">reject</span>}
    <button class="modal-open" id="ID_260_5" title="a definition with multiple references" data-urls="#ID line 68_55, 68_60, 69_55, 69_60, 101_55, 127_57, 130_57, 138_55, 145_88, 175_60, 176_53">ID</button> = <span class="cons_Lit">"and"</span>          {<span class="keyword">reject</span>}
    <button class="modal-open" id="ID_261_5" title="a definition with multiple references" data-urls="#ID line 68_55, 68_60, 69_55, 69_60, 101_55, 127_57, 130_57, 138_55, 145_88, 175_60, 176_53">ID</button> = <span class="cons_Lit">"rap"</span>          {<span class="keyword">reject</span>}

    <button class="modal-open" id="ID_263_5" title="a definition with multiple references" data-urls="#ID line 68_55, 68_60, 69_55, 69_60, 101_55, 127_57, 130_57, 138_55, 145_88, 175_60, 176_53">ID</button> = <span class="cons_Lit">"sel"</span>          {<span class="keyword">reject</span>}
    <button class="modal-open" id="ID_264_5" title="a definition with multiple references" data-urls="#ID line 68_55, 68_60, 69_55, 69_60, 101_55, 127_57, 130_57, 138_55, 145_88, 175_60, 176_53">ID</button> = <span class="cons_Lit">"or"</span>           {<span class="keyword">reject</span>}
    <button class="modal-open" id="ID_265_5" title="a definition with multiple references" data-urls="#ID line 68_55, 68_60, 69_55, 69_60, 101_55, 127_57, 130_57, 138_55, 145_88, 175_60, 176_53">ID</button> = <span class="cons_Lit">"les"</span>          {<span class="keyword">reject</span>}

    <button class="modal-open" id="ID_267_5" title="a definition with multiple references" data-urls="#ID line 68_55, 68_60, 69_55, 69_60, 101_55, 127_57, 130_57, 138_55, 145_88, 175_60, 176_53">ID</button> = <span class="cons_Lit">"abort"</span>        {<span class="keyword">reject</span>}
    <button class="modal-open" id="ID_268_5" title="a definition with multiple references" data-urls="#ID line 68_55, 68_60, 69_55, 69_60, 101_55, 127_57, 130_57, 138_55, 145_88, 175_60, 176_53">ID</button> = <span class="cons_Lit">"interrupt"</span>    {<span class="keyword">reject</span>}
    <button class="modal-open" id="ID_269_5" title="a definition with multiple references" data-urls="#ID line 68_55, 68_60, 69_55, 69_60, 101_55, 127_57, 130_57, 138_55, 145_88, 175_60, 176_53">ID</button> = <span class="cons_Lit">"with"</span>         {<span class="keyword">reject</span>}

    <button class="modal-open" id="ID_271_5" title="a definition with multiple references" data-urls="#ID line 68_55, 68_60, 69_55, 69_60, 101_55, 127_57, 130_57, 138_55, 145_88, 175_60, 176_53">ID</button> = <span class="cons_Lit">"delay"</span>        {<span class="keyword">reject</span>}
    <button class="modal-open" id="ID_272_5" title="a definition with multiple references" data-urls="#ID line 68_55, 68_60, 69_55, 69_60, 101_55, 127_57, 130_57, 138_55, 145_88, 175_60, 176_53">ID</button> = <span class="cons_Lit">"skip"</span>         {<span class="keyword">reject</span>}

    <button class="modal-open" id="ID_274_5" title="a definition with multiple references" data-urls="#ID line 68_55, 68_60, 69_55, 69_60, 101_55, 127_57, 130_57, 138_55, 145_88, 175_60, 176_53">ID</button> = <span class="cons_Lit">"currentTime"</span>  {<span class="keyword">reject</span>}
    <button class="modal-open" id="ID_275_5" title="a definition with multiple references" data-urls="#ID line 68_55, 68_60, 69_55, 69_60, 101_55, 127_57, 130_57, 138_55, 145_88, 175_60, 176_53">ID</button> = <span class="cons_Lit">"new"</span>          {<span class="keyword">reject</span>}
    <button class="modal-open" id="ID_276_5" title="a definition with multiple references" data-urls="#ID line 68_55, 68_60, 69_55, 69_60, 101_55, 127_57, 130_57, 138_55, 145_88, 175_60, 176_53">ID</button> = <span class="cons_Lit">"nil"</span>          {<span class="keyword">reject</span>}
    <button class="modal-open" id="ID_277_5" title="a definition with multiple references" data-urls="#ID line 68_55, 68_60, 69_55, 69_60, 101_55, 127_57, 130_57, 138_55, 145_88, 175_60, 176_53">ID</button> = <span class="cons_Lit">"self"</span>         {<span class="keyword">reject</span>}
    <button class="modal-open" id="ID_278_5" title="a definition with multiple references" data-urls="#ID line 68_55, 68_60, 69_55, 69_60, 101_55, 127_57, 130_57, 138_55, 145_88, 175_60, 176_53">ID</button> = <span class="cons_Lit">"return"</span>       {<span class="keyword">reject</span>}

</code></pre></td></tr></tbody></table></div>

<div id="modal">
  <div id="modal-content">
    <span id="modal-close">&times;</span>
    <h2 id="modal-h2"></h2>
    <p  id="modal-p"></p>
    <ul id="modal-ul"></ul>
  </div>
</div>
