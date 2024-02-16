---
title: Poosl.sdf3
hide:
  - toc
---

# `Poosl.sdf3`

:simple-github: [pdmosses/metaborg-poosl/org.metaborg.lang.poosl/syntax/Poosl.sdf3]

[pdmosses/metaborg-poosl/org.metaborg.lang.poosl/syntax/Poosl.sdf3]: https://github.com/pdmosses/metaborg-poosl/blob/master/org.metaborg.lang.poosl/syntax/Poosl.sdf3 "The source file on GitHub"

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
</pre></div></td>
<td class="code"><pre><code><span class="keyword">module</span> <a href="../Stratego-Poosl.sdf3/#Poosl_11_5" id="Poosl_1_8" title="a definition with a single reference">Poosl</a>

<span class="keyword">imports</span>
    <a href="../Common.sdf3/#Common_1_8" id="Common_4_5" title="a reference to a single-file definition">Common</a>
    <a href="../ExprStat.sdf3/#ExprStat_1_8" id="ExprStat_5_5" title="a reference to a single-file definition">ExprStat</a>

<span class="keyword">context-free start-symbols</span>
    <a href="#Poosl_11_5" id="Poosl_8_5" title="a reference to a single-file definition">Poosl</a>

<span class="keyword">context-free sorts</span>
    <a href="#Poosl_8_5" id="Poosl_11_5" title="a definition with a single reference">Poosl</a>
    <a href="#ImportList_51_10" id="ImportList_12_5" title="a definition with a single reference">ImportList</a>
    <a href="#Import_55_60" id="Import_13_5" title="a definition with a single reference">Import</a>
    <button class="modal-open" id="AnnotationList_14_5" title="a definition with multiple references" data-urls="#AnnotationList line 73_10, 83_10, 88_10, 93_10, 135_10, 151_10, 170_10, 179_10, 191_10, 202_10">AnnotationList</button>
    <a href="#Annotation_65_57" id="Annotation_15_5" title="a definition with a single reference">Annotation</a>
    <a href="#OptAnnotationArgs_66_64" id="OptAnnotationArgs_16_5" title="a definition with a single reference">OptAnnotationArgs</a>
    <a href="#Class_56_60" id="Class_17_5" title="a definition with a single reference">Class</a>
    <a href="#ClassList_52_10" id="ClassList_18_5" title="a definition with a single reference">ClassList</a>
    <a href="#DataMethodList_78_14" id="DataMethodList_19_5" title="a definition with a single reference">DataMethodList</a>
    <a href="#DataMethod_81_60" id="DataMethod_20_5" title="a definition with a single reference">DataMethod</a>
    <button class="modal-open" id="OperatorBinary_21_5" title="a definition with multiple references" data-urls="#OperatorBinary line 94_10, 104_17">OperatorBinary</button>
    <a href="#NativeClause_74_10" id="NativeClause_22_5" title="a definition with a single reference">NativeClause</a>
    <button class="modal-open" id="ExtendsClause_23_5" title="a definition with multiple references" data-urls="#ExtendsClause line 74_41, 136_47">ExtendsClause</button>
    <button class="modal-open" id="IDList_24_5" title="a definition with multiple references" data-urls="#IDList line 121_59, 122_59, 123_59">IDList</button>
    <button class="modal-open" id="Declaration_25_5" title="a definition with multiple references" data-urls="#Declaration line 94_27, 104_34, 126_61, 127_61, 129_62">Declaration</button>
    <button class="modal-open" id="DeclarationOptCommaList_26_5" title="a definition with multiple references" data-urls="#DeclarationOptCommaList line 76_14, 142_14">DeclarationOptCommaList</button>
    <a href="#DeclarationOptComma_125_60" id="DeclarationOptComma_27_5" title="a definition with a single reference">DeclarationOptComma</a>
    <button class="modal-open" id="ParameterList_28_5" title="a definition with multiple references" data-urls="#ParameterList line 152_14, 152_29">ParameterList</button>
    <button class="modal-open" id="OptEmptyList_29_5" title="a definition with multiple references" data-urls="#OptEmptyList line 89_25, 101_32">OptEmptyList</button>
    <button class="modal-open" id="OptParameterList_30_5" title="a definition with multiple references" data-urls="#OptParameterList line 84_14, 98_21, 136_28, 180_28">OptParameterList</button>
    <button class="modal-open" id="OptLocalVariableList_31_5" title="a definition with multiple references" data-urls="#OptLocalVariableList line 84_40, 89_47, 94_49, 152_45">OptLocalVariableList</button>
    <a href="#ProcessMethodList_146_14" id="ProcessMethodList_32_5" title="a definition with a single reference">ProcessMethodList</a>
    <a href="#ProcessMethod_149_60" id="ProcessMethod_33_5" title="a definition with a single reference">ProcessMethod</a>
    <button class="modal-open" id="PortList_34_5" title="a definition with multiple references" data-urls="#PortList line 138_14, 182_14">PortList</button>
    <a href="#Port_156_60" id="Port_35_5" title="a definition with a single reference">Port</a>
    <a href="#MessageSignatureList_140_14" id="MessageSignatureList_36_5" title="a definition with a single reference">MessageSignatureList</a>
    <a href="#MessageSignature_159_60" id="MessageSignature_37_5" title="a definition with a single reference">MessageSignature</a>
    <button class="modal-open" id="OptMessageParameterList_38_5" title="a definition with multiple references" data-urls="#OptMessageParameterList line 160_68, 161_68">OptMessageParameterList</button>
    <button class="modal-open" id="InstanceList_39_5" title="a definition with multiple references" data-urls="#InstanceList line 173_14, 184_14">InstanceList</button>
    <a href="#Instance_189_60" id="Instance_40_5" title="a definition with a single reference">Instance</a>
    <a href="#OptInstanceParameterList_192_21" id="OptInstanceParameterList_41_5" title="a definition with a single reference">OptInstanceParameterList</a>
    <a href="#InstanceParameter_195_61" id="InstanceParameter_42_5" title="a definition with a single reference">InstanceParameter</a>
    <button class="modal-open" id="ChannelList_43_5" title="a definition with multiple references" data-urls="#ChannelList line 175_14, 186_14">ChannelList</button>
    <a href="#Channel_200_60" id="Channel_44_5" title="a definition with a single reference">Channel</a>
    <a href="#PortInstance_206_60" id="PortInstance_45_5" title="a definition with a single reference">PortInstance</a>
    <a href="#PortInstanceList_203_12" id="PortInstanceList_46_5" title="a definition with a single reference">PortInstanceList</a>
    <button class="modal-open" id="OptionalComma_47_5" title="a definition with multiple references" data-urls="#OptionalComma line 157_63, 160_93, 161_93">OptionalComma</button>

<span class="keyword">context-free syntax</span>
    <a href="#Poosl_8_5" id="Poosl_50_5" title="a definition with a single reference">Poosl</a>.<span class="cons_Constructor"><span id="Poosl_50_11" title="a definition with no references">Poosl</span></span> = [
        [<a href="#ImportList_12_5" id="ImportList_51_10" title="a reference to a single-file definition">ImportList</a>]
        [<a href="#ClassList_18_5" id="ClassList_52_10" title="a reference to a single-file definition">ClassList</a>]
    ]

    <a href="#ImportList_51_10" id="ImportList_55_5" title="a definition with a single reference">ImportList</a>.<span class="cons_Constructor"><span id="ImportList_55_16" title="a definition with no references">ImportList</span></span> =                             [[{<a href="#Import_13_5" id="Import_55_60" title="a reference to a single-file definition">Import</a> <span class="cons_Lit">"\n"</span>}*]]
    <a href="#ClassList_52_10" id="ClassList_56_5" title="a definition with a single reference">ClassList</a>.<span class="cons_Constructor"><span id="ClassList_56_15" title="a definition with no references">ClassList</span></span> =                               [[{<a href="#Class_17_5" id="Class_56_60" title="a reference to a single-file definition">Class</a> <span class="cons_Lit">"\n\n"</span>}*]]

    <span class="layout">// === Multiple files =======</span>

    <a href="#Import_55_60" id="Import_60_5" title="a definition with a single reference">Import</a>.<span class="cons_Constructor"><span id="Import_60_12" title="a definition with no references">Import</span></span> =                                     [<span class="cons_String">import</span> [<a href="../Common.sdf3/#STRING_62_3" id="STRING_60_66" title="a reference to a single-file definition">STRING</a>]]
    <a href="#Import_55_60" id="Import_61_5" title="a definition with a single reference">Import</a>.<span class="cons_Constructor"><span id="ImportLib_61_12" title="a definition with no references">ImportLib</span></span> =                                  [<span class="cons_String">importlib</span> [<a href="../Common.sdf3/#STRING_62_3" id="STRING_61_69" title="a reference to a single-file definition">STRING</a>]]

    <span class="layout">// === Annotation =======</span>

    <button class="modal-open" id="AnnotationList_65_5" title="a definition with multiple references" data-urls="#AnnotationList line 73_10, 83_10, 88_10, 93_10, 135_10, 151_10, 170_10, 179_10, 191_10, 202_10">AnnotationList</button>.<span class="cons_Constructor"><span id="AnnotationList_65_20" title="a definition with no references">AnnotationList</span></span> =                     <a href="#Annotation_15_5" id="Annotation_65_57" title="a reference to a single-file definition">Annotation</a>*
    <a href="#Annotation_65_57" id="Annotation_66_5" title="a definition with a single reference">Annotation</a>.<span class="cons_Constructor"><span id="Annotation_66_16" title="a definition with no references">Annotation</span></span> =                             [<span class="cons_String">@</span>[<a href="#ID_216_5" id="ID_66_60" title="a reference to a single-file definition">ID</a>][<a href="#OptAnnotationArgs_16_5" id="OptAnnotationArgs_66_64" title="a reference to a single-file definition">OptAnnotationArgs</a>]]
    <a href="#OptAnnotationArgs_66_64" id="OptAnnotationArgs_67_5" title="a definition with a single reference">OptAnnotationArgs</a>.<span class="cons_Constructor"><span id="AnnotationArgs_67_23" title="a definition with no references">AnnotationArgs</span></span> =                  [<span class="cons_String">(</span>[{<a href="../ExprStat.sdf3/#ExpressionConstant_25_5" id="ExpressionConstant_67_61" title="a reference to a single-file definition">ExpressionConstant</a> <span class="cons_Lit">", "</span>}*]<span class="cons_String">)</span>]
    <a href="#OptAnnotationArgs_66_64" id="OptAnnotationArgs_68_5" title="a definition with a single reference">OptAnnotationArgs</a>.<span class="cons_Constructor"><span id="NoAnnotationArgs_68_23" title="a definition with no references">NoAnnotationArgs</span></span> =                []

    <span class="layout">// === Data Class =======</span>

    <a href="#Class_56_60" id="Class_72_5" title="a definition with a single reference">Class</a>.<span class="cons_Constructor"><span id="DataClass_72_11" title="a definition with no references">DataClass</span></span> = [
        [<a href="#AnnotationList_14_5" id="AnnotationList_73_10" title="a reference to a single-file definition">AnnotationList</a>]
        [<a href="#NativeClause_22_5" id="NativeClause_74_10" title="a reference to a single-file definition">NativeClause</a>] <span class="cons_String">data</span> <span class="cons_String">class</span> [<a href="#ID_216_5" id="ID_74_36" title="a reference to a single-file definition">ID</a>] [<a href="#ExtendsClause_23_5" id="ExtendsClause_74_41" title="a reference to a single-file definition">ExtendsClause</a>]
        <span class="cons_String">variables</span>
            [<a href="#DeclarationOptCommaList_26_5" id="DeclarationOptCommaList_76_14" title="a reference to a single-file definition">DeclarationOptCommaList</a>]
        <span class="cons_String">methods</span>
            [<a href="#DataMethodList_19_5" id="DataMethodList_78_14" title="a reference to a single-file definition">DataMethodList</a>]
    ]

    <a href="#DataMethodList_78_14" id="DataMethodList_81_5" title="a definition with a single reference">DataMethodList</a>.<span class="cons_Constructor"><span id="DataMethodList_81_20" title="a definition with no references">DataMethodList</span></span> =                     [[{<a href="#DataMethod_20_5" id="DataMethod_81_60" title="a reference to a single-file definition">DataMethod</a> <span class="cons_Lit">"\n\n"</span>}*]]
    <a href="#DataMethod_81_60" id="DataMethod_82_5" title="a definition with a single reference">DataMethod</a>.<span class="cons_Constructor"><span id="DataMethodNamed_82_16" title="a definition with no references">DataMethodNamed</span></span> = [
        [<a href="#AnnotationList_14_5" id="AnnotationList_83_10" title="a reference to a single-file definition">AnnotationList</a>]
        [<a href="#ID_216_5" id="ID_84_10" title="a reference to a single-file definition">ID</a>][<a href="#OptParameterList_30_5" id="OptParameterList_84_14" title="a reference to a single-file definition">OptParameterList</a>] <span class="cons_String">:</span> [<a href="#ID_216_5" id="ID_84_35" title="a reference to a single-file definition">ID</a>] [<a href="#OptLocalVariableList_31_5" id="OptLocalVariableList_84_40" title="a reference to a single-file definition">OptLocalVariableList</a>]
            [<a href="../ExprStat.sdf3/#Expression_16_5" id="Expression_85_14" title="a reference to a single-file definition">Expression</a>]
    ]
    <a href="#DataMethod_81_60" id="DataMethod_87_5" title="a definition with a single reference">DataMethod</a>.<span class="cons_Constructor"><span id="DataMethodUnary_87_16" title="a definition with no references">DataMethodUnary</span></span> = [
        [<a href="#AnnotationList_14_5" id="AnnotationList_88_10" title="a reference to a single-file definition">AnnotationList</a>]
        [<a href="../ExprStat.sdf3/#UnaryOperator_26_5" id="UnaryOperator_89_10" title="a reference to a single-file definition">UnaryOperator</a>][<a href="#OptEmptyList_29_5" id="OptEmptyList_89_25" title="a reference to a single-file definition">OptEmptyList</a>] <span class="cons_String">:</span> [<a href="#ID_216_5" id="ID_89_42" title="a reference to a single-file definition">ID</a>] [<a href="#OptLocalVariableList_31_5" id="OptLocalVariableList_89_47" title="a reference to a single-file definition">OptLocalVariableList</a>]
            [<a href="../ExprStat.sdf3/#Expression_16_5" id="Expression_90_14" title="a reference to a single-file definition">Expression</a>]
    ]
    <a href="#DataMethod_81_60" id="DataMethod_92_5" title="a definition with a single reference">DataMethod</a>.<span class="cons_Constructor"><span id="DataMethodBinary_92_16" title="a definition with no references">DataMethodBinary</span></span> = [
        [<a href="#AnnotationList_14_5" id="AnnotationList_93_10" title="a reference to a single-file definition">AnnotationList</a>]
        [<a href="#OperatorBinary_21_5" id="OperatorBinary_94_10" title="a reference to a single-file definition">OperatorBinary</a>]<span class="cons_String">(</span>[<a href="#Declaration_25_5" id="Declaration_94_27" title="a reference to a single-file definition">Declaration</a>]<span class="cons_String">)</span> <span class="cons_String">:</span> [<a href="#ID_216_5" id="ID_94_44" title="a reference to a single-file definition">ID</a>] [<a href="#OptLocalVariableList_31_5" id="OptLocalVariableList_94_49" title="a reference to a single-file definition">OptLocalVariableList</a>]
            [<a href="../ExprStat.sdf3/#Expression_16_5" id="Expression_95_14" title="a reference to a single-file definition">Expression</a>]
    ]
    <a href="#DataMethod_81_60" id="DataMethod_97_5" title="a definition with a single reference">DataMethod</a>.<span class="cons_Constructor"><span id="DataMethodNamedNative_97_16" title="a definition with no references">DataMethodNamedNative</span></span> = [
        <span class="cons_String">native</span> [<a href="#ID_216_5" id="ID_98_17" title="a reference to a single-file definition">ID</a>][<a href="#OptParameterList_30_5" id="OptParameterList_98_21" title="a reference to a single-file definition">OptParameterList</a>] <span class="cons_String">:</span> [<a href="#ID_216_5" id="ID_98_42" title="a reference to a single-file definition">ID</a>]
    ]
    <a href="#DataMethod_81_60" id="DataMethod_100_5" title="a definition with a single reference">DataMethod</a>.<span class="cons_Constructor"><span id="DataMethodUnaryNative_100_16" title="a definition with no references">DataMethodUnaryNative</span></span> = [
        <span class="cons_String">native</span> [<a href="../ExprStat.sdf3/#UnaryOperator_26_5" id="UnaryOperator_101_17" title="a reference to a single-file definition">UnaryOperator</a>][<a href="#OptEmptyList_29_5" id="OptEmptyList_101_32" title="a reference to a single-file definition">OptEmptyList</a>] <span class="cons_String">:</span> [<a href="#ID_216_5" id="ID_101_49" title="a reference to a single-file definition">ID</a>]
    ]
    <a href="#DataMethod_81_60" id="DataMethod_103_5" title="a definition with a single reference">DataMethod</a>.<span class="cons_Constructor"><span id="DataMethodBinaryNative_103_16" title="a definition with no references">DataMethodBinaryNative</span></span> = [
        <span class="cons_String">native</span> [<a href="#OperatorBinary_21_5" id="OperatorBinary_104_17" title="a reference to a single-file definition">OperatorBinary</a>]<span class="cons_String">(</span>[<a href="#Declaration_25_5" id="Declaration_104_34" title="a reference to a single-file definition">Declaration</a>]<span class="cons_String">)</span> <span class="cons_String">:</span> [<a href="#ID_216_5" id="ID_104_51" title="a reference to a single-file definition">ID</a>]
    ]

    <button class="modal-open" id="OptEmptyList_107_5" title="a definition with multiple references" data-urls="#OptEmptyList line 89_25, 101_32">OptEmptyList</button>.<span class="cons_Constructor"><span id="NoList_107_18" title="a definition with no references">NoList</span></span> = []
    <button class="modal-open" id="OptEmptyList_108_5" title="a definition with multiple references" data-urls="#OptEmptyList line 89_25, 101_32">OptEmptyList</button>.<span class="cons_Constructor"><span id="EmptyList_108_18" title="a definition with no references">EmptyList</span></span> = [<span class="cons_String">()</span>]

    <button class="modal-open" id="OperatorBinary_110_5" title="a definition with multiple references" data-urls="#OperatorBinary line 94_10, 104_17">OperatorBinary</button>.<span class="cons_Constructor"><span id="OperatorBinary2_110_20" title="a definition with no references">OperatorBinary2</span></span> =                    <a href="../ExprStat.sdf3/#BinaryOperatorLevel2_27_5" id="BinaryOperatorLevel2_110_57" title="a reference to a single-file definition">BinaryOperatorLevel2</a>
    <button class="modal-open" id="OperatorBinary_111_5" title="a definition with multiple references" data-urls="#OperatorBinary line 94_10, 104_17">OperatorBinary</button>.<span class="cons_Constructor"><span id="OperatorBinary3_111_20" title="a definition with no references">OperatorBinary3</span></span> =                    <a href="../ExprStat.sdf3/#BinaryOperatorLevel3_28_5" id="BinaryOperatorLevel3_111_57" title="a reference to a single-file definition">BinaryOperatorLevel3</a>
    <button class="modal-open" id="OperatorBinary_112_5" title="a definition with multiple references" data-urls="#OperatorBinary line 94_10, 104_17">OperatorBinary</button>.<span class="cons_Constructor"><span id="OperatorBinary4_112_20" title="a definition with no references">OperatorBinary4</span></span> =                    <a href="../ExprStat.sdf3/#BinaryOperatorLevel4_29_5" id="BinaryOperatorLevel4_112_57" title="a reference to a single-file definition">BinaryOperatorLevel4</a>

    <a href="#NativeClause_74_10" id="NativeClause_114_5" title="a definition with a single reference">NativeClause</a>.<span class="cons_Constructor"><span id="Native_114_18" title="a definition with no references">Native</span></span> =                               [<span class="cons_String">native</span>]
    <a href="#NativeClause_74_10" id="NativeClause_115_5" title="a definition with a single reference">NativeClause</a>.<span class="cons_Constructor"><span id="NotNative_115_18" title="a definition with no references">NotNative</span></span> =                            []

    <button class="modal-open" id="ExtendsClause_117_5" title="a definition with multiple references" data-urls="#ExtendsClause line 74_41, 136_47">ExtendsClause</button>.<span class="cons_Constructor"><span id="Extends_117_19" title="a definition with no references">Extends</span></span> =                             [<span class="cons_String">extends</span> [<a href="#ID_216_5" id="ID_117_67" title="a reference to a single-file definition">ID</a>]]
    <button class="modal-open" id="ExtendsClause_118_5" title="a definition with multiple references" data-urls="#ExtendsClause line 74_41, 136_47">ExtendsClause</button>.<span class="cons_Constructor"><span id="NoExtends_118_19" title="a definition with no references">NoExtends</span></span> =                           []

    <button class="modal-open" id="IDList_120_5" title="a definition with multiple references" data-urls="#IDList line 121_59, 122_59, 123_59">IDList</button>.<span class="cons_Constructor"><span id="IDList_120_12" title="a definition with no references">IDList</span></span> =                                     [[{<a href="#ID_216_5" id="ID_120_60" title="a reference to a single-file definition">ID</a> <span class="cons_Lit">", "</span>}*]]
    <button class="modal-open" id="Declaration_121_5" title="a definition with multiple references" data-urls="#Declaration line 94_27, 104_34, 126_61, 127_61, 129_62">Declaration</button>.<span class="cons_Constructor"><span id="Declaration_121_17" title="a definition with no references">Declaration</span></span> =                           [[<a href="#IDList_24_5" id="IDList_121_59" title="a reference to a single-file definition">IDList</a>] <span class="cons_String">:</span> [<a href="#ID_216_5" id="ID_121_70" title="a reference to a single-file definition">ID</a>]]
    <a href="#DeclarationOptComma_125_60" id="DeclarationOptComma_122_5" title="a definition with a single reference">DeclarationOptComma</a>.<span class="cons_Constructor"><span id="DeclarationWithComma_122_25" title="a definition with no references">DeclarationWithComma</span></span> =          [[<a href="#IDList_24_5" id="IDList_122_59" title="a reference to a single-file definition">IDList</a>] <span class="cons_String">:</span> [<a href="#ID_216_5" id="ID_122_70" title="a reference to a single-file definition">ID</a>]<span class="cons_String">,</span>]
    <a href="#DeclarationOptComma_125_60" id="DeclarationOptComma_123_5" title="a definition with a single reference">DeclarationOptComma</a>.<span class="cons_Constructor"><span id="DeclarationWithoutComma_123_25" title="a definition with no references">DeclarationWithoutComma</span></span> =       [[<a href="#IDList_24_5" id="IDList_123_59" title="a reference to a single-file definition">IDList</a>] <span class="cons_String">:</span> [<a href="#ID_216_5" id="ID_123_70" title="a reference to a single-file definition">ID</a>]]

    <button class="modal-open" id="DeclarationOptCommaList_125_5" title="a definition with multiple references" data-urls="#DeclarationOptCommaList line 76_14, 142_14">DeclarationOptCommaList</button>.<span class="cons_Constructor"><span id="DeclarationOptCommaList_125_29" title="a definition with no references">DeclarationOptCommaList</span></span> =   [[{<a href="#DeclarationOptComma_27_5" id="DeclarationOptComma_125_60" title="a reference to a single-file definition">DeclarationOptComma</a> <span class="cons_Lit">"\n"</span>}*]] 
    <button class="modal-open" id="ParameterList_126_5" title="a definition with multiple references" data-urls="#ParameterList line 152_14, 152_29">ParameterList</button>.<span class="cons_Constructor"><span id="ParameterList_126_19" title="a definition with no references">ParameterList</span></span> =                       [<span class="cons_String">(</span>[{<a href="#Declaration_25_5" id="Declaration_126_61" title="a reference to a single-file definition">Declaration</a> <span class="cons_Lit">", "</span>}*]<span class="cons_String">)</span>]
    <button class="modal-open" id="OptParameterList_127_5" title="a definition with multiple references" data-urls="#OptParameterList line 84_14, 98_21, 136_28, 180_28">OptParameterList</button>.<span class="cons_Constructor"><span id="Parameters_127_22" title="a definition with no references">Parameters</span></span> =                       [<span class="cons_String">(</span>[{<a href="#Declaration_25_5" id="Declaration_127_61" title="a reference to a single-file definition">Declaration</a> <span class="cons_Lit">", "</span>}*]<span class="cons_String">)</span>]
    <button class="modal-open" id="OptParameterList_128_5" title="a definition with multiple references" data-urls="#OptParameterList line 84_14, 98_21, 136_28, 180_28">OptParameterList</button>.<span class="cons_Constructor"><span id="NoParameters_128_22" title="a definition with no references">NoParameters</span></span> =                     []
    <button class="modal-open" id="OptLocalVariableList_129_5" title="a definition with multiple references" data-urls="#OptLocalVariableList line 84_40, 89_47, 94_49, 152_45">OptLocalVariableList</button>.<span class="cons_Constructor"><span id="LocalVariables_129_26" title="a definition with no references">LocalVariables</span></span> =               [<span class="cons_String">|</span> [{<a href="#Declaration_25_5" id="Declaration_129_62" title="a reference to a single-file definition">Declaration</a> <span class="cons_Lit">", "</span>}*] <span class="cons_String">|</span>]
    <button class="modal-open" id="OptLocalVariableList_130_5" title="a definition with multiple references" data-urls="#OptLocalVariableList line 84_40, 89_47, 94_49, 152_45">OptLocalVariableList</button>.<span class="cons_Constructor"><span id="NoLocalVariables_130_26" title="a definition with no references">NoLocalVariables</span></span> =             []

    <span class="layout">// === Process Class =======</span>
 
    <a href="#Class_56_60" id="Class_134_5" title="a definition with a single reference">Class</a>.<span class="cons_Constructor"><span id="ProcessClass_134_11" title="a definition with no references">ProcessClass</span></span> = [
        [<a href="#AnnotationList_14_5" id="AnnotationList_135_10" title="a reference to a single-file definition">AnnotationList</a>]
        <span class="cons_String">process</span> <span class="cons_String">class</span> [<a href="#ID_216_5" id="ID_136_24" title="a reference to a single-file definition">ID</a>][<a href="#OptParameterList_30_5" id="OptParameterList_136_28" title="a reference to a single-file definition">OptParameterList</a>] [<a href="#ExtendsClause_23_5" id="ExtendsClause_136_47" title="a reference to a single-file definition">ExtendsClause</a>]
        <span class="cons_String">ports</span>
            [<a href="#PortList_34_5" id="PortList_138_14" title="a reference to a single-file definition">PortList</a>]
        <span class="cons_String">messages</span>
            [<a href="#MessageSignatureList_36_5" id="MessageSignatureList_140_14" title="a reference to a single-file definition">MessageSignatureList</a>]
        <span class="cons_String">variables</span>
            [<a href="#DeclarationOptCommaList_26_5" id="DeclarationOptCommaList_142_14" title="a reference to a single-file definition">DeclarationOptCommaList</a>]
        <span class="cons_String">init</span>
            [<a href="../ExprStat.sdf3/#ProcessMethodCall_11_5" id="ProcessMethodCall_144_14" title="a reference to a single-file definition">ProcessMethodCall</a>]
        <span class="cons_String">methods</span>
            [<a href="#ProcessMethodList_32_5" id="ProcessMethodList_146_14" title="a reference to a single-file definition">ProcessMethodList</a>]
    ]

    <a href="#ProcessMethodList_146_14" id="ProcessMethodList_149_5" title="a definition with a single reference">ProcessMethodList</a>.<span class="cons_Constructor"><span id="ProcessMethodList_149_23" title="a definition with no references">ProcessMethodList</span></span> =               [[{<a href="#ProcessMethod_33_5" id="ProcessMethod_149_60" title="a reference to a single-file definition">ProcessMethod</a> <span class="cons_Lit">"\n\n"</span>}*]]
    <a href="#ProcessMethod_149_60" id="ProcessMethod_150_5" title="a definition with a single reference">ProcessMethod</a>.<span class="cons_Constructor"><span id="ProcessMethod_150_19" title="a definition with no references">ProcessMethod</span></span> = [
        [<a href="#AnnotationList_14_5" id="AnnotationList_151_10" title="a reference to a single-file definition">AnnotationList</a>]
        [<a href="#ID_216_5" id="ID_152_10" title="a reference to a single-file definition">ID</a>][<a href="#ParameterList_28_5" id="ParameterList_152_14" title="a reference to a single-file definition">ParameterList</a>][<a href="#ParameterList_28_5" id="ParameterList_152_29" title="a reference to a single-file definition">ParameterList</a>] [<a href="#OptLocalVariableList_31_5" id="OptLocalVariableList_152_45" title="a reference to a single-file definition">OptLocalVariableList</a>]
            [<a href="../ExprStat.sdf3/#Statement_7_5" id="Statement_153_14" title="a reference to a single-file definition">Statement</a>]
    ]

    <button class="modal-open" id="PortList_156_5" title="a definition with multiple references" data-urls="#PortList line 138_14, 182_14">PortList</button>.<span class="cons_Constructor"><span id="PortList_156_14" title="a definition with no references">PortList</span></span> =                                 [[{<a href="#Port_35_5" id="Port_156_60" title="a reference to a single-file definition">Port</a> <span class="cons_Lit">"\n"</span>}*]]
    <a href="#Port_156_60" id="Port_157_5" title="a definition with a single reference">Port</a>.<span class="cons_Constructor"><span id="Port_157_10" title="a definition with no references">Port</span></span> =                                         [[<a href="#ID_216_5" id="ID_157_59" title="a reference to a single-file definition">ID</a>][<a href="#OptionalComma_47_5" id="OptionalComma_157_63" title="a reference to a single-file definition">OptionalComma</a>]]

    <a href="#MessageSignatureList_140_14" id="MessageSignatureList_159_5" title="a definition with a single reference">MessageSignatureList</a>.<span class="cons_Constructor"><span id="MessageSignatureList_159_26" title="a definition with no references">MessageSignatureList</span></span> =         [[{<a href="#MessageSignature_37_5" id="MessageSignature_159_60" title="a reference to a single-file definition">MessageSignature</a> <span class="cons_Lit">"\n"</span>}*]]
    <a href="#MessageSignature_159_60" id="MessageSignature_160_5" title="a definition with a single reference">MessageSignature</a>.<span class="cons_Constructor"><span id="MessageReceiveSignature_160_22" title="a definition with no references">MessageReceiveSignature</span></span> =          [[<a href="#ID_216_5" id="ID_160_59" title="a reference to a single-file definition">ID</a>]<span class="cons_String">?</span>[<a href="#ID_216_5" id="ID_160_64" title="a reference to a single-file definition">ID</a>][<a href="#OptMessageParameterList_38_5" id="OptMessageParameterList_160_68" title="a reference to a single-file definition">OptMessageParameterList</a>][<a href="#OptionalComma_47_5" id="OptionalComma_160_93" title="a reference to a single-file definition">OptionalComma</a>]] 
    <a href="#MessageSignature_159_60" id="MessageSignature_161_5" title="a definition with a single reference">MessageSignature</a>.<span class="cons_Constructor"><span id="MessageSendSignature_161_22" title="a definition with no references">MessageSendSignature</span></span> =             [[<a href="#ID_216_5" id="ID_161_59" title="a reference to a single-file definition">ID</a>]<span class="cons_String">!</span>[<a href="#ID_216_5" id="ID_161_64" title="a reference to a single-file definition">ID</a>][<a href="#OptMessageParameterList_38_5" id="OptMessageParameterList_161_68" title="a reference to a single-file definition">OptMessageParameterList</a>][<a href="#OptionalComma_47_5" id="OptionalComma_161_93" title="a reference to a single-file definition">OptionalComma</a>]]

    <button class="modal-open" id="OptMessageParameterList_163_5" title="a definition with multiple references" data-urls="#OptMessageParameterList line 160_68, 161_68">OptMessageParameterList</button>.<span class="cons_Constructor"><span id="MessageParameters_163_29" title="a definition with no references">MessageParameters</span></span> =         [<span class="cons_String">(</span>[{<a href="#ID_216_5" id="ID_163_61" title="a reference to a single-file definition">ID</a> <span class="cons_Lit">", "</span>}*]<span class="cons_String">)</span>]
    <button class="modal-open" id="OptMessageParameterList_164_5" title="a definition with multiple references" data-urls="#OptMessageParameterList line 160_68, 161_68">OptMessageParameterList</button>.<span class="cons_Constructor"><span id="NoMessageParameters_164_29" title="a definition with no references">NoMessageParameters</span></span> =       []


    <span class="layout">// === System and Cluster Class =======</span>

    <a href="#Class_56_60" id="Class_169_5" title="a definition with a single reference">Class</a>.<span class="cons_Constructor"><span id="System_169_11" title="a definition with no references">System</span></span> =  [
        [<a href="#AnnotationList_14_5" id="AnnotationList_170_10" title="a reference to a single-file definition">AnnotationList</a>]
        <span class="cons_String">system</span>
        <span class="cons_String">instances</span>
            [<a href="#InstanceList_39_5" id="InstanceList_173_14" title="a reference to a single-file definition">InstanceList</a>]
        <span class="cons_String">channels</span>
            [<a href="#ChannelList_43_5" id="ChannelList_175_14" title="a reference to a single-file definition">ChannelList</a>]
    ]

    <a href="#Class_56_60" id="Class_178_5" title="a definition with a single reference">Class</a>.<span class="cons_Constructor"><span id="ClusterClass_178_11" title="a definition with no references">ClusterClass</span></span> = [
        [<a href="#AnnotationList_14_5" id="AnnotationList_179_10" title="a reference to a single-file definition">AnnotationList</a>]
        <span class="cons_String">cluster</span> <span class="cons_String">class</span> [<a href="#ID_216_5" id="ID_180_24" title="a reference to a single-file definition">ID</a>][<a href="#OptParameterList_30_5" id="OptParameterList_180_28" title="a reference to a single-file definition">OptParameterList</a>]
        <span class="cons_String">ports</span>
            [<a href="#PortList_34_5" id="PortList_182_14" title="a reference to a single-file definition">PortList</a>]
        <span class="cons_String">instances</span>
            [<a href="#InstanceList_39_5" id="InstanceList_184_14" title="a reference to a single-file definition">InstanceList</a>]
        <span class="cons_String">channels</span>
            [<a href="#ChannelList_43_5" id="ChannelList_186_14" title="a reference to a single-file definition">ChannelList</a>]
    ]

    <button class="modal-open" id="InstanceList_189_5" title="a definition with multiple references" data-urls="#InstanceList line 173_14, 184_14">InstanceList</button>.<span class="cons_Constructor"><span id="InstanceList_189_18" title="a definition with no references">InstanceList</span></span> =                         [[{<a href="#Instance_40_5" id="Instance_189_60" title="a reference to a single-file definition">Instance</a> <span class="cons_Lit">"\n"</span>}*]]
    <a href="#Instance_189_60" id="Instance_190_5" title="a definition with a single reference">Instance</a>.<span class="cons_Constructor"><span id="Instance_190_14" title="a definition with no references">Instance</span></span> = [
        [<a href="#AnnotationList_14_5" id="AnnotationList_191_10" title="a reference to a single-file definition">AnnotationList</a>]
        [<a href="#ID_216_5" id="ID_192_10" title="a reference to a single-file definition">ID</a>] <span class="cons_String">:</span> [<a href="#ID_216_5" id="ID_192_17" title="a reference to a single-file definition">ID</a>][<a href="#OptInstanceParameterList_41_5" id="OptInstanceParameterList_192_21" title="a reference to a single-file definition">OptInstanceParameterList</a>]
    ]

    <a href="#OptInstanceParameterList_192_21" id="OptInstanceParameterList_195_5" title="a definition with a single reference">OptInstanceParameterList</a>.<span class="cons_Constructor"><span id="InstanceParameters_195_30" title="a definition with no references">InstanceParameters</span></span> =       [<span class="cons_String">(</span>[{<a href="#InstanceParameter_42_5" id="InstanceParameter_195_61" title="a reference to a single-file definition">InstanceParameter</a> <span class="cons_Lit">", "</span>}*]<span class="cons_String">)</span>]
    <a href="#OptInstanceParameterList_192_21" id="OptInstanceParameterList_196_5" title="a definition with a single reference">OptInstanceParameterList</a>.<span class="cons_Constructor"><span id="NoInstanceParameters_196_30" title="a definition with no references">NoInstanceParameters</span></span> =     []

    <a href="#InstanceParameter_195_61" id="InstanceParameter_198_5" title="a definition with a single reference">InstanceParameter</a>.<span class="cons_Constructor"><span id="InstanceParameter_198_23" title="a definition with no references">InstanceParameter</span></span> =               [[<a href="#ID_216_5" id="ID_198_59" title="a reference to a single-file definition">ID</a>] <span class="cons_String">:=</span> [<a href="../ExprStat.sdf3/#Expression_16_5" id="Expression_198_67" title="a reference to a single-file definition">Expression</a>]]

    <button class="modal-open" id="ChannelList_200_5" title="a definition with multiple references" data-urls="#ChannelList line 175_14, 186_14">ChannelList</button>.<span class="cons_Constructor"><span id="ChannelList_200_17" title="a definition with no references">ChannelList</span></span> =                           [[{<a href="#Channel_44_5" id="Channel_200_60" title="a reference to a single-file definition">Channel</a> <span class="cons_Lit">"\n"</span>}*]]
    <a href="#Channel_200_60" id="Channel_201_5" title="a definition with a single reference">Channel</a>.<span class="cons_Constructor"><span id="Channel_201_13" title="a definition with no references">Channel</span></span> = [
        [<a href="#AnnotationList_14_5" id="AnnotationList_202_10" title="a reference to a single-file definition">AnnotationList</a>]
        <span class="cons_String">{</span> [<a href="#PortInstanceList_46_5" id="PortInstanceList_203_12" title="a reference to a single-file definition">PortInstanceList</a>] <span class="cons_String">}</span>
    ]

    <a href="#PortInstanceList_203_12" id="PortInstanceList_206_5" title="a definition with a single reference">PortInstanceList</a>.<span class="cons_Constructor"><span id="PortInstanceList_206_22" title="a definition with no references">PortInstanceList</span></span> =                 [[{<a href="#PortInstance_45_5" id="PortInstance_206_60" title="a reference to a single-file definition">PortInstance</a> <span class="cons_Lit">", "</span>}+]]
    <a href="#PortInstance_206_60" id="PortInstance_207_5" title="a definition with a single reference">PortInstance</a>.<span class="cons_Constructor"><span id="InternalPort_207_18" title="a definition with no references">InternalPort</span></span> =                         [[<a href="#ID_216_5" id="ID_207_59" title="a reference to a single-file definition">ID</a>]<span class="cons_String">.</span>[<a href="#ID_216_5" id="ID_207_64" title="a reference to a single-file definition">ID</a>]]
    <a href="#PortInstance_206_60" id="PortInstance_208_5" title="a definition with a single reference">PortInstance</a>.<span class="cons_Constructor"><span id="ExternalPort_208_18" title="a definition with no references">ExternalPort</span></span> =                         <a href="#ID_216_5" id="ID_208_57" title="a reference to a single-file definition">ID</a>

    <span class="layout">// === Workarounds =======</span>

    <button class="modal-open" id="OptionalComma_212_5" title="a definition with multiple references" data-urls="#OptionalComma line 157_63, 160_93, 161_93">OptionalComma</button>.<span class="cons_Constructor"><span id="Comma_212_19" title="a definition with no references">Comma</span></span> =                               [<span class="cons_String">,</span>]
    <button class="modal-open" id="OptionalComma_213_5" title="a definition with multiple references" data-urls="#OptionalComma line 157_63, 160_93, 161_93">OptionalComma</button>.<span class="cons_Constructor"><span id="NoComma_213_19" title="a definition with no references">NoComma</span></span> =                             []

<span class="keyword">lexical syntax</span>      <span class="layout">// keywords</span>
    <button class="modal-open" id="ID_216_5" title="a definition with multiple references" data-urls="#ID line 66_60, 74_36, 84_10, 84_35, 89_42, 94_44, 98_17, 98_42, 101_49, 104_51, 117_67, 120_60, 121_70, 122_70, 123_70, 136_24, 152_10, 157_59, 160_59, 160_64, 161_59, 161_64, 163_61, 180_24, 192_10, 192_17, 198_59, 207_59, 207_64, 208_57">ID</button> = <span class="cons_Lit">"import"</span>       {<span class="keyword">reject</span>}
    <button class="modal-open" id="ID_217_5" title="a definition with multiple references" data-urls="#ID line 66_60, 74_36, 84_10, 84_35, 89_42, 94_44, 98_17, 98_42, 101_49, 104_51, 117_67, 120_60, 121_70, 122_70, 123_70, 136_24, 152_10, 157_59, 160_59, 160_64, 161_59, 161_64, 163_61, 180_24, 192_10, 192_17, 198_59, 207_59, 207_64, 208_57">ID</button> = <span class="cons_Lit">"importlib"</span>    {<span class="keyword">reject</span>}

    <button class="modal-open" id="ID_219_5" title="a definition with multiple references" data-urls="#ID line 66_60, 74_36, 84_10, 84_35, 89_42, 94_44, 98_17, 98_42, 101_49, 104_51, 117_67, 120_60, 121_70, 122_70, 123_70, 136_24, 152_10, 157_59, 160_59, 160_64, 161_59, 161_64, 163_61, 180_24, 192_10, 192_17, 198_59, 207_59, 207_64, 208_57">ID</button> = <span class="cons_Lit">"data"</span>         {<span class="keyword">reject</span>}
    <button class="modal-open" id="ID_220_5" title="a definition with multiple references" data-urls="#ID line 66_60, 74_36, 84_10, 84_35, 89_42, 94_44, 98_17, 98_42, 101_49, 104_51, 117_67, 120_60, 121_70, 122_70, 123_70, 136_24, 152_10, 157_59, 160_59, 160_64, 161_59, 161_64, 163_61, 180_24, 192_10, 192_17, 198_59, 207_59, 207_64, 208_57">ID</button> = <span class="cons_Lit">"process"</span>      {<span class="keyword">reject</span>}
    <button class="modal-open" id="ID_221_5" title="a definition with multiple references" data-urls="#ID line 66_60, 74_36, 84_10, 84_35, 89_42, 94_44, 98_17, 98_42, 101_49, 104_51, 117_67, 120_60, 121_70, 122_70, 123_70, 136_24, 152_10, 157_59, 160_59, 160_64, 161_59, 161_64, 163_61, 180_24, 192_10, 192_17, 198_59, 207_59, 207_64, 208_57">ID</button> = <span class="cons_Lit">"cluster"</span>      {<span class="keyword">reject</span>}
    <button class="modal-open" id="ID_222_5" title="a definition with multiple references" data-urls="#ID line 66_60, 74_36, 84_10, 84_35, 89_42, 94_44, 98_17, 98_42, 101_49, 104_51, 117_67, 120_60, 121_70, 122_70, 123_70, 136_24, 152_10, 157_59, 160_59, 160_64, 161_59, 161_64, 163_61, 180_24, 192_10, 192_17, 198_59, 207_59, 207_64, 208_57">ID</button> = <span class="cons_Lit">"system"</span>       {<span class="keyword">reject</span>}

    <button class="modal-open" id="ID_224_5" title="a definition with multiple references" data-urls="#ID line 66_60, 74_36, 84_10, 84_35, 89_42, 94_44, 98_17, 98_42, 101_49, 104_51, 117_67, 120_60, 121_70, 122_70, 123_70, 136_24, 152_10, 157_59, 160_59, 160_64, 161_59, 161_64, 163_61, 180_24, 192_10, 192_17, 198_59, 207_59, 207_64, 208_57">ID</button> = <span class="cons_Lit">"native"</span>       {<span class="keyword">reject</span>}

<span class="layout">// Note: No reserved words!</span>
<span class="layout">//  ID = "class"        {reject}</span>
<span class="layout">//  ID = "extends"      {reject}</span>
<span class="layout">//  ID = "variables"    {reject}</span>
<span class="layout">//  ID = "methods"      {reject}</span>
<span class="layout">//  ID = "ports"        {reject}</span>
<span class="layout">//  ID = "messages"     {reject}</span>
<span class="layout">//  ID = "init"         {reject}</span>
<span class="layout">//  ID = "channels"     {reject}</span>
<span class="layout">//  ID = "instances"    {reject}</span>

</code></pre></td></tr></tbody></table></div>

<div id="modal">
  <div id="modal-content">
    <span id="modal-close">&times;</span>
    <h2 id="modal-h2"></h2>
    <p  id="modal-p"></p>
    <ul id="modal-ul"></ul>
  </div>
</div>
