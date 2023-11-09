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
<td class="code"><pre><code><span class="keyword">module</span> <a href="../Stratego-Poosl.sdf3/#Poosl_11_5" id="Poosl_1_8" title="Referenced at ../Stratego-Poosl.sdf3 line 11">Poosl</a>

<span class="keyword">imports</span>
    <a href="../Common.sdf3/#Common_1_8" id="Common_4_5" title="Defined at ../Common.sdf3 line 1">Common</a>
    <a href="../ExprStat.sdf3/#ExprStat_1_8" id="ExprStat_5_5" title="Defined at ../ExprStat.sdf3 line 1">ExprStat</a>

<span class="keyword">context-free start-symbols</span>
    <a href="#Poosl_11_5" id="Poosl_8_5" title="Defined at line 11, 50">Poosl</a>

<span class="keyword">context-free sorts</span>
    <a href="#Poosl_8_5" id="Poosl_11_5" title="Referenced at line 8">Poosl</a>
    <a href="#ImportList_51_10" id="ImportList_12_5" title="Referenced at line 51">ImportList</a>
    <a href="#Import_55_60" id="Import_13_5" title="Referenced at line 55">Import</a>
    <a href="#AnnotationList_73_10" id="AnnotationList_14_5" title="Referenced at line 73, 83, 88, 93, 135, 151, 170, 179, 191, 202">AnnotationList</a>
    <a href="#Annotation_65_57" id="Annotation_15_5" title="Referenced at line 65">Annotation</a>
    <a href="#OptAnnotationArgs_66_64" id="OptAnnotationArgs_16_5" title="Referenced at line 66">OptAnnotationArgs</a>
    <a href="#Class_56_60" id="Class_17_5" title="Referenced at line 56">Class</a>
    <a href="#ClassList_52_10" id="ClassList_18_5" title="Referenced at line 52">ClassList</a>
    <a href="#DataMethodList_78_14" id="DataMethodList_19_5" title="Referenced at line 78">DataMethodList</a>
    <a href="#DataMethod_81_60" id="DataMethod_20_5" title="Referenced at line 81">DataMethod</a>
    <a href="#OperatorBinary_94_10" id="OperatorBinary_21_5" title="Referenced at line 94, 104">OperatorBinary</a>
    <a href="#NativeClause_74_10" id="NativeClause_22_5" title="Referenced at line 74">NativeClause</a>
    <a href="#ExtendsClause_74_41" id="ExtendsClause_23_5" title="Referenced at line 74, 136">ExtendsClause</a>
    <a href="#IDList_121_59" id="IDList_24_5" title="Referenced at line 121, 122, 123">IDList</a>
    <a href="#Declaration_94_27" id="Declaration_25_5" title="Referenced at line 94, 104, 126, 127, 129">Declaration</a>
    <a href="#DeclarationOptCommaList_76_14" id="DeclarationOptCommaList_26_5" title="Referenced at line 76, 142">DeclarationOptCommaList</a>
    <a href="#DeclarationOptComma_125_60" id="DeclarationOptComma_27_5" title="Referenced at line 125">DeclarationOptComma</a>
    <a href="#ParameterList_152_14" id="ParameterList_28_5" title="Referenced at line 152">ParameterList</a>
    <a href="#OptEmptyList_89_25" id="OptEmptyList_29_5" title="Referenced at line 89, 101">OptEmptyList</a>
    <a href="#OptParameterList_84_14" id="OptParameterList_30_5" title="Referenced at line 84, 98, 136, 180">OptParameterList</a>
    <a href="#OptLocalVariableList_84_40" id="OptLocalVariableList_31_5" title="Referenced at line 84, 89, 94, 152">OptLocalVariableList</a>
    <a href="#ProcessMethodList_146_14" id="ProcessMethodList_32_5" title="Referenced at line 146">ProcessMethodList</a>
    <a href="#ProcessMethod_149_60" id="ProcessMethod_33_5" title="Referenced at line 149">ProcessMethod</a>
    <a href="#PortList_138_14" id="PortList_34_5" title="Referenced at line 138, 182">PortList</a>
    <a href="#Port_156_60" id="Port_35_5" title="Referenced at line 156">Port</a>
    <a href="#MessageSignatureList_140_14" id="MessageSignatureList_36_5" title="Referenced at line 140">MessageSignatureList</a>
    <a href="#MessageSignature_159_60" id="MessageSignature_37_5" title="Referenced at line 159">MessageSignature</a>
    <a href="#OptMessageParameterList_160_68" id="OptMessageParameterList_38_5" title="Referenced at line 160, 161">OptMessageParameterList</a>
    <a href="#InstanceList_173_14" id="InstanceList_39_5" title="Referenced at line 173, 184">InstanceList</a>
    <a href="#Instance_189_60" id="Instance_40_5" title="Referenced at line 189">Instance</a>
    <a href="#OptInstanceParameterList_192_21" id="OptInstanceParameterList_41_5" title="Referenced at line 192">OptInstanceParameterList</a>
    <a href="#InstanceParameter_195_61" id="InstanceParameter_42_5" title="Referenced at line 195">InstanceParameter</a>
    <a href="#ChannelList_175_14" id="ChannelList_43_5" title="Referenced at line 175, 186">ChannelList</a>
    <a href="#Channel_200_60" id="Channel_44_5" title="Referenced at line 200">Channel</a>
    <a href="#PortInstance_206_60" id="PortInstance_45_5" title="Referenced at line 206">PortInstance</a>
    <a href="#PortInstanceList_203_12" id="PortInstanceList_46_5" title="Referenced at line 203">PortInstanceList</a>
    <a href="#OptionalComma_157_63" id="OptionalComma_47_5" title="Referenced at line 157, 160, 161">OptionalComma</a>

<span class="keyword">context-free syntax</span>
    <a href="#Poosl_8_5" id="Poosl_50_5" title="Referenced at line 8">Poosl</a>.<span class="cons_Constructor"><span id="Poosl_50_11" title="Not referenced">Poosl</span></span> = [
        [<a href="#ImportList_12_5" id="ImportList_51_10" title="Defined at line 12, 55">ImportList</a>]
        [<a href="#ClassList_18_5" id="ClassList_52_10" title="Defined at line 18, 56">ClassList</a>]
    ]

    <a href="#ImportList_51_10" id="ImportList_55_5" title="Referenced at line 51">ImportList</a>.<span class="cons_Constructor"><span id="ImportList_55_16" title="Not referenced">ImportList</span></span> =                             [[{<a href="#Import_13_5" id="Import_55_60" title="Defined at line 13, 60, 61">Import</a> <span class="cons_Lit">"\n"</span>}*]]
    <a href="#ClassList_52_10" id="ClassList_56_5" title="Referenced at line 52">ClassList</a>.<span class="cons_Constructor"><span id="ClassList_56_15" title="Not referenced">ClassList</span></span> =                               [[{<a href="#Class_17_5" id="Class_56_60" title="Defined at line 17, 72, 134, 169, 178">Class</a> <span class="cons_Lit">"\n\n"</span>}*]]

    <span class="layout">// === Multiple files =======</span>

    <a href="#Import_55_60" id="Import_60_5" title="Referenced at line 55">Import</a>.<span class="cons_Constructor"><span id="Import_60_12" title="Not referenced">Import</span></span> =                                     [<span class="cons_String">import</span> [<a href="../Common.sdf3/#STRING_62_3" id="STRING_60_66" title="Defined at ../Common.sdf3 line 62, 66">STRING</a>]]
    <a href="#Import_55_60" id="Import_61_5" title="Referenced at line 55">Import</a>.<span class="cons_Constructor"><span id="ImportLib_61_12" title="Not referenced">ImportLib</span></span> =                                  [<span class="cons_String">importlib</span> [<a href="../Common.sdf3/#STRING_62_3" id="STRING_61_69" title="Defined at ../Common.sdf3 line 62, 66">STRING</a>]]

    <span class="layout">// === Annotation =======</span>

    <a href="#AnnotationList_73_10" id="AnnotationList_65_5" title="Referenced at line 73, 83, 88, 93, 135, 151, 170, 179, 191, 202">AnnotationList</a>.<span class="cons_Constructor"><span id="AnnotationList_65_20" title="Not referenced">AnnotationList</span></span> =                     <a href="#Annotation_15_5" id="Annotation_65_57" title="Defined at line 15, 66">Annotation</a>*
    <a href="#Annotation_65_57" id="Annotation_66_5" title="Referenced at line 65">Annotation</a>.<span class="cons_Constructor"><span id="Annotation_66_16" title="Not referenced">Annotation</span></span> =                             [<span class="cons_String">@</span>[<a href="#ID_216_5" id="ID_66_60" title="Defined at line 216, 217, 219, 220, 221, 222, 224">ID</a>][<a href="#OptAnnotationArgs_16_5" id="OptAnnotationArgs_66_64" title="Defined at line 16, 67, 68">OptAnnotationArgs</a>]]
    <a href="#OptAnnotationArgs_66_64" id="OptAnnotationArgs_67_5" title="Referenced at line 66">OptAnnotationArgs</a>.<span class="cons_Constructor"><span id="AnnotationArgs_67_23" title="Not referenced">AnnotationArgs</span></span> =                  [<span class="cons_String">(</span>[{<a href="../ExprStat.sdf3/#ExpressionConstant_25_5" id="ExpressionConstant_67_61" title="Defined at ../ExprStat.sdf3 line 25, 179, 180, 181, 182, 183, 184, 185, 186">ExpressionConstant</a> <span class="cons_Lit">", "</span>}*]<span class="cons_String">)</span>]
    <a href="#OptAnnotationArgs_66_64" id="OptAnnotationArgs_68_5" title="Referenced at line 66">OptAnnotationArgs</a>.<span class="cons_Constructor"><span id="NoAnnotationArgs_68_23" title="Not referenced">NoAnnotationArgs</span></span> =                []

    <span class="layout">// === Data Class =======</span>

    <a href="#Class_56_60" id="Class_72_5" title="Referenced at line 56">Class</a>.<span class="cons_Constructor"><span id="DataClass_72_11" title="Not referenced">DataClass</span></span> = [
        [<a href="#AnnotationList_14_5" id="AnnotationList_73_10" title="Defined at line 14, 65">AnnotationList</a>]
        [<a href="#NativeClause_22_5" id="NativeClause_74_10" title="Defined at line 22, 114, 115">NativeClause</a>] <span class="cons_String">data</span> <span class="cons_String">class</span> [<a href="#ID_216_5" id="ID_74_36" title="Defined at line 216, 217, 219, 220, 221, 222, 224">ID</a>] [<a href="#ExtendsClause_23_5" id="ExtendsClause_74_41" title="Defined at line 23, 117, 118">ExtendsClause</a>]
        <span class="cons_String">variables</span>
            [<a href="#DeclarationOptCommaList_26_5" id="DeclarationOptCommaList_76_14" title="Defined at line 26, 125">DeclarationOptCommaList</a>]
        <span class="cons_String">methods</span>
            [<a href="#DataMethodList_19_5" id="DataMethodList_78_14" title="Defined at line 19, 81">DataMethodList</a>]
    ]

    <a href="#DataMethodList_78_14" id="DataMethodList_81_5" title="Referenced at line 78">DataMethodList</a>.<span class="cons_Constructor"><span id="DataMethodList_81_20" title="Not referenced">DataMethodList</span></span> =                     [[{<a href="#DataMethod_20_5" id="DataMethod_81_60" title="Defined at line 20, 82, 87, 92, 97, 100, 103">DataMethod</a> <span class="cons_Lit">"\n\n"</span>}*]]
    <a href="#DataMethod_81_60" id="DataMethod_82_5" title="Referenced at line 81">DataMethod</a>.<span class="cons_Constructor"><span id="DataMethodNamed_82_16" title="Not referenced">DataMethodNamed</span></span> = [
        [<a href="#AnnotationList_14_5" id="AnnotationList_83_10" title="Defined at line 14, 65">AnnotationList</a>]
        [<a href="#ID_216_5" id="ID_84_10" title="Defined at line 216, 217, 219, 220, 221, 222, 224">ID</a>][<a href="#OptParameterList_30_5" id="OptParameterList_84_14" title="Defined at line 30, 127, 128">OptParameterList</a>] <span class="cons_String">:</span> [<a href="#ID_216_5" id="ID_84_35" title="Defined at line 216, 217, 219, 220, 221, 222, 224">ID</a>] [<a href="#OptLocalVariableList_31_5" id="OptLocalVariableList_84_40" title="Defined at line 31, 129, 130">OptLocalVariableList</a>]
            [<a href="../ExprStat.sdf3/#Expression_16_5" id="Expression_85_14" title="Defined at ../ExprStat.sdf3 line 16, 135">Expression</a>]
    ]
    <a href="#DataMethod_81_60" id="DataMethod_87_5" title="Referenced at line 81">DataMethod</a>.<span class="cons_Constructor"><span id="DataMethodUnary_87_16" title="Not referenced">DataMethodUnary</span></span> = [
        [<a href="#AnnotationList_14_5" id="AnnotationList_88_10" title="Defined at line 14, 65">AnnotationList</a>]
        [<a href="../ExprStat.sdf3/#UnaryOperator_26_5" id="UnaryOperator_89_10" title="Defined at ../ExprStat.sdf3 line 26, 206, 207">UnaryOperator</a>][<a href="#OptEmptyList_29_5" id="OptEmptyList_89_25" title="Defined at line 29, 107, 108">OptEmptyList</a>] <span class="cons_String">:</span> [<a href="#ID_216_5" id="ID_89_42" title="Defined at line 216, 217, 219, 220, 221, 222, 224">ID</a>] [<a href="#OptLocalVariableList_31_5" id="OptLocalVariableList_89_47" title="Defined at line 31, 129, 130">OptLocalVariableList</a>]
            [<a href="../ExprStat.sdf3/#Expression_16_5" id="Expression_90_14" title="Defined at ../ExprStat.sdf3 line 16, 135">Expression</a>]
    ]
    <a href="#DataMethod_81_60" id="DataMethod_92_5" title="Referenced at line 81">DataMethod</a>.<span class="cons_Constructor"><span id="DataMethodBinary_92_16" title="Not referenced">DataMethodBinary</span></span> = [
        [<a href="#AnnotationList_14_5" id="AnnotationList_93_10" title="Defined at line 14, 65">AnnotationList</a>]
        [<a href="#OperatorBinary_21_5" id="OperatorBinary_94_10" title="Defined at line 21, 110, 111, 112">OperatorBinary</a>]<span class="cons_String">(</span>[<a href="#Declaration_25_5" id="Declaration_94_27" title="Defined at line 25, 121">Declaration</a>]<span class="cons_String">)</span> <span class="cons_String">:</span> [<a href="#ID_216_5" id="ID_94_44" title="Defined at line 216, 217, 219, 220, 221, 222, 224">ID</a>] [<a href="#OptLocalVariableList_31_5" id="OptLocalVariableList_94_49" title="Defined at line 31, 129, 130">OptLocalVariableList</a>]
            [<a href="../ExprStat.sdf3/#Expression_16_5" id="Expression_95_14" title="Defined at ../ExprStat.sdf3 line 16, 135">Expression</a>]
    ]
    <a href="#DataMethod_81_60" id="DataMethod_97_5" title="Referenced at line 81">DataMethod</a>.<span class="cons_Constructor"><span id="DataMethodNamedNative_97_16" title="Not referenced">DataMethodNamedNative</span></span> = [
        <span class="cons_String">native</span> [<a href="#ID_216_5" id="ID_98_17" title="Defined at line 216, 217, 219, 220, 221, 222, 224">ID</a>][<a href="#OptParameterList_30_5" id="OptParameterList_98_21" title="Defined at line 30, 127, 128">OptParameterList</a>] <span class="cons_String">:</span> [<a href="#ID_216_5" id="ID_98_42" title="Defined at line 216, 217, 219, 220, 221, 222, 224">ID</a>]
    ]
    <a href="#DataMethod_81_60" id="DataMethod_100_5" title="Referenced at line 81">DataMethod</a>.<span class="cons_Constructor"><span id="DataMethodUnaryNative_100_16" title="Not referenced">DataMethodUnaryNative</span></span> = [
        <span class="cons_String">native</span> [<a href="../ExprStat.sdf3/#UnaryOperator_26_5" id="UnaryOperator_101_17" title="Defined at ../ExprStat.sdf3 line 26, 206, 207">UnaryOperator</a>][<a href="#OptEmptyList_29_5" id="OptEmptyList_101_32" title="Defined at line 29, 107, 108">OptEmptyList</a>] <span class="cons_String">:</span> [<a href="#ID_216_5" id="ID_101_49" title="Defined at line 216, 217, 219, 220, 221, 222, 224">ID</a>]
    ]
    <a href="#DataMethod_81_60" id="DataMethod_103_5" title="Referenced at line 81">DataMethod</a>.<span class="cons_Constructor"><span id="DataMethodBinaryNative_103_16" title="Not referenced">DataMethodBinaryNative</span></span> = [
        <span class="cons_String">native</span> [<a href="#OperatorBinary_21_5" id="OperatorBinary_104_17" title="Defined at line 21, 110, 111, 112">OperatorBinary</a>]<span class="cons_String">(</span>[<a href="#Declaration_25_5" id="Declaration_104_34" title="Defined at line 25, 121">Declaration</a>]<span class="cons_String">)</span> <span class="cons_String">:</span> [<a href="#ID_216_5" id="ID_104_51" title="Defined at line 216, 217, 219, 220, 221, 222, 224">ID</a>]
    ]

    <a href="#OptEmptyList_89_25" id="OptEmptyList_107_5" title="Referenced at line 89, 101">OptEmptyList</a>.<span class="cons_Constructor"><span id="NoList_107_18" title="Not referenced">NoList</span></span> = []
    <a href="#OptEmptyList_89_25" id="OptEmptyList_108_5" title="Referenced at line 89, 101">OptEmptyList</a>.<span class="cons_Constructor"><span id="EmptyList_108_18" title="Not referenced">EmptyList</span></span> = [<span class="cons_String">()</span>]

    <a href="#OperatorBinary_94_10" id="OperatorBinary_110_5" title="Referenced at line 94, 104">OperatorBinary</a>.<span class="cons_Constructor"><span id="OperatorBinary2_110_20" title="Not referenced">OperatorBinary2</span></span> =                    <a href="../ExprStat.sdf3/#BinaryOperatorLevel2_27_5" id="BinaryOperatorLevel2_110_57" title="Defined at ../ExprStat.sdf3 line 27, 209, 210, 211, 212, 213, 214, 215, 216">BinaryOperatorLevel2</a>
    <a href="#OperatorBinary_94_10" id="OperatorBinary_111_5" title="Referenced at line 94, 104">OperatorBinary</a>.<span class="cons_Constructor"><span id="OperatorBinary3_111_20" title="Not referenced">OperatorBinary3</span></span> =                    <a href="../ExprStat.sdf3/#BinaryOperatorLevel3_28_5" id="BinaryOperatorLevel3_111_57" title="Defined at ../ExprStat.sdf3 line 28, 218, 219, 220, 221">BinaryOperatorLevel3</a>
    <a href="#OperatorBinary_94_10" id="OperatorBinary_112_5" title="Referenced at line 94, 104">OperatorBinary</a>.<span class="cons_Constructor"><span id="OperatorBinary4_112_20" title="Not referenced">OperatorBinary4</span></span> =                    <a href="../ExprStat.sdf3/#BinaryOperatorLevel4_29_5" id="BinaryOperatorLevel4_112_57" title="Defined at ../ExprStat.sdf3 line 29, 223, 224">BinaryOperatorLevel4</a>

    <a href="#NativeClause_74_10" id="NativeClause_114_5" title="Referenced at line 74">NativeClause</a>.<span class="cons_Constructor"><span id="Native_114_18" title="Not referenced">Native</span></span> =                               [<span class="cons_String">native</span>]
    <a href="#NativeClause_74_10" id="NativeClause_115_5" title="Referenced at line 74">NativeClause</a>.<span class="cons_Constructor"><span id="NotNative_115_18" title="Not referenced">NotNative</span></span> =                            []

    <a href="#ExtendsClause_74_41" id="ExtendsClause_117_5" title="Referenced at line 74, 136">ExtendsClause</a>.<span class="cons_Constructor"><span id="Extends_117_19" title="Not referenced">Extends</span></span> =                             [<span class="cons_String">extends</span> [<a href="#ID_216_5" id="ID_117_67" title="Defined at line 216, 217, 219, 220, 221, 222, 224">ID</a>]]
    <a href="#ExtendsClause_74_41" id="ExtendsClause_118_5" title="Referenced at line 74, 136">ExtendsClause</a>.<span class="cons_Constructor"><span id="NoExtends_118_19" title="Not referenced">NoExtends</span></span> =                           []

    <a href="#IDList_121_59" id="IDList_120_5" title="Referenced at line 121, 122, 123">IDList</a>.<span class="cons_Constructor"><span id="IDList_120_12" title="Not referenced">IDList</span></span> =                                     [[{<a href="#ID_216_5" id="ID_120_60" title="Defined at line 216, 217, 219, 220, 221, 222, 224">ID</a> <span class="cons_Lit">", "</span>}*]]
    <a href="#Declaration_94_27" id="Declaration_121_5" title="Referenced at line 94, 104, 126, 127, 129">Declaration</a>.<span class="cons_Constructor"><span id="Declaration_121_17" title="Not referenced">Declaration</span></span> =                           [[<a href="#IDList_24_5" id="IDList_121_59" title="Defined at line 24, 120">IDList</a>] <span class="cons_String">:</span> [<a href="#ID_216_5" id="ID_121_70" title="Defined at line 216, 217, 219, 220, 221, 222, 224">ID</a>]]
    <a href="#DeclarationOptComma_125_60" id="DeclarationOptComma_122_5" title="Referenced at line 125">DeclarationOptComma</a>.<span class="cons_Constructor"><span id="DeclarationWithComma_122_25" title="Not referenced">DeclarationWithComma</span></span> =          [[<a href="#IDList_24_5" id="IDList_122_59" title="Defined at line 24, 120">IDList</a>] <span class="cons_String">:</span> [<a href="#ID_216_5" id="ID_122_70" title="Defined at line 216, 217, 219, 220, 221, 222, 224">ID</a>]<span class="cons_String">,</span>]
    <a href="#DeclarationOptComma_125_60" id="DeclarationOptComma_123_5" title="Referenced at line 125">DeclarationOptComma</a>.<span class="cons_Constructor"><span id="DeclarationWithoutComma_123_25" title="Not referenced">DeclarationWithoutComma</span></span> =       [[<a href="#IDList_24_5" id="IDList_123_59" title="Defined at line 24, 120">IDList</a>] <span class="cons_String">:</span> [<a href="#ID_216_5" id="ID_123_70" title="Defined at line 216, 217, 219, 220, 221, 222, 224">ID</a>]]

    <a href="#DeclarationOptCommaList_76_14" id="DeclarationOptCommaList_125_5" title="Referenced at line 76, 142">DeclarationOptCommaList</a>.<span class="cons_Constructor"><span id="DeclarationOptCommaList_125_29" title="Not referenced">DeclarationOptCommaList</span></span> =   [[{<a href="#DeclarationOptComma_27_5" id="DeclarationOptComma_125_60" title="Defined at line 27, 122, 123">DeclarationOptComma</a> <span class="cons_Lit">"\n"</span>}*]] 
    <a href="#ParameterList_152_14" id="ParameterList_126_5" title="Referenced at line 152">ParameterList</a>.<span class="cons_Constructor"><span id="ParameterList_126_19" title="Not referenced">ParameterList</span></span> =                       [<span class="cons_String">(</span>[{<a href="#Declaration_25_5" id="Declaration_126_61" title="Defined at line 25, 121">Declaration</a> <span class="cons_Lit">", "</span>}*]<span class="cons_String">)</span>]
    <a href="#OptParameterList_84_14" id="OptParameterList_127_5" title="Referenced at line 84, 98, 136, 180">OptParameterList</a>.<span class="cons_Constructor"><span id="Parameters_127_22" title="Not referenced">Parameters</span></span> =                       [<span class="cons_String">(</span>[{<a href="#Declaration_25_5" id="Declaration_127_61" title="Defined at line 25, 121">Declaration</a> <span class="cons_Lit">", "</span>}*]<span class="cons_String">)</span>]
    <a href="#OptParameterList_84_14" id="OptParameterList_128_5" title="Referenced at line 84, 98, 136, 180">OptParameterList</a>.<span class="cons_Constructor"><span id="NoParameters_128_22" title="Not referenced">NoParameters</span></span> =                     []
    <a href="#OptLocalVariableList_84_40" id="OptLocalVariableList_129_5" title="Referenced at line 84, 89, 94, 152">OptLocalVariableList</a>.<span class="cons_Constructor"><span id="LocalVariables_129_26" title="Not referenced">LocalVariables</span></span> =               [<span class="cons_String">|</span> [{<a href="#Declaration_25_5" id="Declaration_129_62" title="Defined at line 25, 121">Declaration</a> <span class="cons_Lit">", "</span>}*] <span class="cons_String">|</span>]
    <a href="#OptLocalVariableList_84_40" id="OptLocalVariableList_130_5" title="Referenced at line 84, 89, 94, 152">OptLocalVariableList</a>.<span class="cons_Constructor"><span id="NoLocalVariables_130_26" title="Not referenced">NoLocalVariables</span></span> =             []

    <span class="layout">// === Process Class =======</span>
 
    <a href="#Class_56_60" id="Class_134_5" title="Referenced at line 56">Class</a>.<span class="cons_Constructor"><span id="ProcessClass_134_11" title="Not referenced">ProcessClass</span></span> = [
        [<a href="#AnnotationList_14_5" id="AnnotationList_135_10" title="Defined at line 14, 65">AnnotationList</a>]
        <span class="cons_String">process</span> <span class="cons_String">class</span> [<a href="#ID_216_5" id="ID_136_24" title="Defined at line 216, 217, 219, 220, 221, 222, 224">ID</a>][<a href="#OptParameterList_30_5" id="OptParameterList_136_28" title="Defined at line 30, 127, 128">OptParameterList</a>] [<a href="#ExtendsClause_23_5" id="ExtendsClause_136_47" title="Defined at line 23, 117, 118">ExtendsClause</a>]
        <span class="cons_String">ports</span>
            [<a href="#PortList_34_5" id="PortList_138_14" title="Defined at line 34, 156">PortList</a>]
        <span class="cons_String">messages</span>
            [<a href="#MessageSignatureList_36_5" id="MessageSignatureList_140_14" title="Defined at line 36, 159">MessageSignatureList</a>]
        <span class="cons_String">variables</span>
            [<a href="#DeclarationOptCommaList_26_5" id="DeclarationOptCommaList_142_14" title="Defined at line 26, 125">DeclarationOptCommaList</a>]
        <span class="cons_String">init</span>
            [<a href="../ExprStat.sdf3/#ProcessMethodCall_11_5" id="ProcessMethodCall_144_14" title="Defined at ../ExprStat.sdf3 line 11, 101">ProcessMethodCall</a>]
        <span class="cons_String">methods</span>
            [<a href="#ProcessMethodList_32_5" id="ProcessMethodList_146_14" title="Defined at line 32, 149">ProcessMethodList</a>]
    ]

    <a href="#ProcessMethodList_146_14" id="ProcessMethodList_149_5" title="Referenced at line 146">ProcessMethodList</a>.<span class="cons_Constructor"><span id="ProcessMethodList_149_23" title="Not referenced">ProcessMethodList</span></span> =               [[{<a href="#ProcessMethod_33_5" id="ProcessMethod_149_60" title="Defined at line 33, 150">ProcessMethod</a> <span class="cons_Lit">"\n\n"</span>}*]]
    <a href="#ProcessMethod_149_60" id="ProcessMethod_150_5" title="Referenced at line 149">ProcessMethod</a>.<span class="cons_Constructor"><span id="ProcessMethod_150_19" title="Not referenced">ProcessMethod</span></span> = [
        [<a href="#AnnotationList_14_5" id="AnnotationList_151_10" title="Defined at line 14, 65">AnnotationList</a>]
        [<a href="#ID_216_5" id="ID_152_10" title="Defined at line 216, 217, 219, 220, 221, 222, 224">ID</a>][<a href="#ParameterList_28_5" id="ParameterList_152_14" title="Defined at line 28, 126">ParameterList</a>][<a href="#ParameterList_28_5" id="ParameterList_152_29" title="Defined at line 28, 126">ParameterList</a>] [<a href="#OptLocalVariableList_31_5" id="OptLocalVariableList_152_45" title="Defined at line 31, 129, 130">OptLocalVariableList</a>]
            [<a href="../ExprStat.sdf3/#Statement_7_5" id="Statement_153_14" title="Defined at ../ExprStat.sdf3 line 7, 38">Statement</a>]
    ]

    <a href="#PortList_138_14" id="PortList_156_5" title="Referenced at line 138, 182">PortList</a>.<span class="cons_Constructor"><span id="PortList_156_14" title="Not referenced">PortList</span></span> =                                 [[{<a href="#Port_35_5" id="Port_156_60" title="Defined at line 35, 157">Port</a> <span class="cons_Lit">"\n"</span>}*]]
    <a href="#Port_156_60" id="Port_157_5" title="Referenced at line 156">Port</a>.<span class="cons_Constructor"><span id="Port_157_10" title="Not referenced">Port</span></span> =                                         [[<a href="#ID_216_5" id="ID_157_59" title="Defined at line 216, 217, 219, 220, 221, 222, 224">ID</a>][<a href="#OptionalComma_47_5" id="OptionalComma_157_63" title="Defined at line 47, 212, 213">OptionalComma</a>]]

    <a href="#MessageSignatureList_140_14" id="MessageSignatureList_159_5" title="Referenced at line 140">MessageSignatureList</a>.<span class="cons_Constructor"><span id="MessageSignatureList_159_26" title="Not referenced">MessageSignatureList</span></span> =         [[{<a href="#MessageSignature_37_5" id="MessageSignature_159_60" title="Defined at line 37, 160, 161">MessageSignature</a> <span class="cons_Lit">"\n"</span>}*]]
    <a href="#MessageSignature_159_60" id="MessageSignature_160_5" title="Referenced at line 159">MessageSignature</a>.<span class="cons_Constructor"><span id="MessageReceiveSignature_160_22" title="Not referenced">MessageReceiveSignature</span></span> =          [[<a href="#ID_216_5" id="ID_160_59" title="Defined at line 216, 217, 219, 220, 221, 222, 224">ID</a>]<span class="cons_String">?</span>[<a href="#ID_216_5" id="ID_160_64" title="Defined at line 216, 217, 219, 220, 221, 222, 224">ID</a>][<a href="#OptMessageParameterList_38_5" id="OptMessageParameterList_160_68" title="Defined at line 38, 163, 164">OptMessageParameterList</a>][<a href="#OptionalComma_47_5" id="OptionalComma_160_93" title="Defined at line 47, 212, 213">OptionalComma</a>]] 
    <a href="#MessageSignature_159_60" id="MessageSignature_161_5" title="Referenced at line 159">MessageSignature</a>.<span class="cons_Constructor"><span id="MessageSendSignature_161_22" title="Not referenced">MessageSendSignature</span></span> =             [[<a href="#ID_216_5" id="ID_161_59" title="Defined at line 216, 217, 219, 220, 221, 222, 224">ID</a>]<span class="cons_String">!</span>[<a href="#ID_216_5" id="ID_161_64" title="Defined at line 216, 217, 219, 220, 221, 222, 224">ID</a>][<a href="#OptMessageParameterList_38_5" id="OptMessageParameterList_161_68" title="Defined at line 38, 163, 164">OptMessageParameterList</a>][<a href="#OptionalComma_47_5" id="OptionalComma_161_93" title="Defined at line 47, 212, 213">OptionalComma</a>]]

    <a href="#OptMessageParameterList_160_68" id="OptMessageParameterList_163_5" title="Referenced at line 160, 161">OptMessageParameterList</a>.<span class="cons_Constructor"><span id="MessageParameters_163_29" title="Not referenced">MessageParameters</span></span> =         [<span class="cons_String">(</span>[{<a href="#ID_216_5" id="ID_163_61" title="Defined at line 216, 217, 219, 220, 221, 222, 224">ID</a> <span class="cons_Lit">", "</span>}*]<span class="cons_String">)</span>]
    <a href="#OptMessageParameterList_160_68" id="OptMessageParameterList_164_5" title="Referenced at line 160, 161">OptMessageParameterList</a>.<span class="cons_Constructor"><span id="NoMessageParameters_164_29" title="Not referenced">NoMessageParameters</span></span> =       []


    <span class="layout">// === System and Cluster Class =======</span>

    <a href="#Class_56_60" id="Class_169_5" title="Referenced at line 56">Class</a>.<span class="cons_Constructor"><span id="System_169_11" title="Not referenced">System</span></span> =  [
        [<a href="#AnnotationList_14_5" id="AnnotationList_170_10" title="Defined at line 14, 65">AnnotationList</a>]
        <span class="cons_String">system</span>
        <span class="cons_String">instances</span>
            [<a href="#InstanceList_39_5" id="InstanceList_173_14" title="Defined at line 39, 189">InstanceList</a>]
        <span class="cons_String">channels</span>
            [<a href="#ChannelList_43_5" id="ChannelList_175_14" title="Defined at line 43, 200">ChannelList</a>]
    ]

    <a href="#Class_56_60" id="Class_178_5" title="Referenced at line 56">Class</a>.<span class="cons_Constructor"><span id="ClusterClass_178_11" title="Not referenced">ClusterClass</span></span> = [
        [<a href="#AnnotationList_14_5" id="AnnotationList_179_10" title="Defined at line 14, 65">AnnotationList</a>]
        <span class="cons_String">cluster</span> <span class="cons_String">class</span> [<a href="#ID_216_5" id="ID_180_24" title="Defined at line 216, 217, 219, 220, 221, 222, 224">ID</a>][<a href="#OptParameterList_30_5" id="OptParameterList_180_28" title="Defined at line 30, 127, 128">OptParameterList</a>]
        <span class="cons_String">ports</span>
            [<a href="#PortList_34_5" id="PortList_182_14" title="Defined at line 34, 156">PortList</a>]
        <span class="cons_String">instances</span>
            [<a href="#InstanceList_39_5" id="InstanceList_184_14" title="Defined at line 39, 189">InstanceList</a>]
        <span class="cons_String">channels</span>
            [<a href="#ChannelList_43_5" id="ChannelList_186_14" title="Defined at line 43, 200">ChannelList</a>]
    ]

    <a href="#InstanceList_173_14" id="InstanceList_189_5" title="Referenced at line 173, 184">InstanceList</a>.<span class="cons_Constructor"><span id="InstanceList_189_18" title="Not referenced">InstanceList</span></span> =                         [[{<a href="#Instance_40_5" id="Instance_189_60" title="Defined at line 40, 190">Instance</a> <span class="cons_Lit">"\n"</span>}*]]
    <a href="#Instance_189_60" id="Instance_190_5" title="Referenced at line 189">Instance</a>.<span class="cons_Constructor"><span id="Instance_190_14" title="Not referenced">Instance</span></span> = [
        [<a href="#AnnotationList_14_5" id="AnnotationList_191_10" title="Defined at line 14, 65">AnnotationList</a>]
        [<a href="#ID_216_5" id="ID_192_10" title="Defined at line 216, 217, 219, 220, 221, 222, 224">ID</a>] <span class="cons_String">:</span> [<a href="#ID_216_5" id="ID_192_17" title="Defined at line 216, 217, 219, 220, 221, 222, 224">ID</a>][<a href="#OptInstanceParameterList_41_5" id="OptInstanceParameterList_192_21" title="Defined at line 41, 195, 196">OptInstanceParameterList</a>]
    ]

    <a href="#OptInstanceParameterList_192_21" id="OptInstanceParameterList_195_5" title="Referenced at line 192">OptInstanceParameterList</a>.<span class="cons_Constructor"><span id="InstanceParameters_195_30" title="Not referenced">InstanceParameters</span></span> =       [<span class="cons_String">(</span>[{<a href="#InstanceParameter_42_5" id="InstanceParameter_195_61" title="Defined at line 42, 198">InstanceParameter</a> <span class="cons_Lit">", "</span>}*]<span class="cons_String">)</span>]
    <a href="#OptInstanceParameterList_192_21" id="OptInstanceParameterList_196_5" title="Referenced at line 192">OptInstanceParameterList</a>.<span class="cons_Constructor"><span id="NoInstanceParameters_196_30" title="Not referenced">NoInstanceParameters</span></span> =     []

    <a href="#InstanceParameter_195_61" id="InstanceParameter_198_5" title="Referenced at line 195">InstanceParameter</a>.<span class="cons_Constructor"><span id="InstanceParameter_198_23" title="Not referenced">InstanceParameter</span></span> =               [[<a href="#ID_216_5" id="ID_198_59" title="Defined at line 216, 217, 219, 220, 221, 222, 224">ID</a>] <span class="cons_String">:=</span> [<a href="../ExprStat.sdf3/#Expression_16_5" id="Expression_198_67" title="Defined at ../ExprStat.sdf3 line 16, 135">Expression</a>]]

    <a href="#ChannelList_175_14" id="ChannelList_200_5" title="Referenced at line 175, 186">ChannelList</a>.<span class="cons_Constructor"><span id="ChannelList_200_17" title="Not referenced">ChannelList</span></span> =                           [[{<a href="#Channel_44_5" id="Channel_200_60" title="Defined at line 44, 201">Channel</a> <span class="cons_Lit">"\n"</span>}*]]
    <a href="#Channel_200_60" id="Channel_201_5" title="Referenced at line 200">Channel</a>.<span class="cons_Constructor"><span id="Channel_201_13" title="Not referenced">Channel</span></span> = [
        [<a href="#AnnotationList_14_5" id="AnnotationList_202_10" title="Defined at line 14, 65">AnnotationList</a>]
        <span class="cons_String">{</span> [<a href="#PortInstanceList_46_5" id="PortInstanceList_203_12" title="Defined at line 46, 206">PortInstanceList</a>] <span class="cons_String">}</span>
    ]

    <a href="#PortInstanceList_203_12" id="PortInstanceList_206_5" title="Referenced at line 203">PortInstanceList</a>.<span class="cons_Constructor"><span id="PortInstanceList_206_22" title="Not referenced">PortInstanceList</span></span> =                 [[{<a href="#PortInstance_45_5" id="PortInstance_206_60" title="Defined at line 45, 207, 208">PortInstance</a> <span class="cons_Lit">", "</span>}+]]
    <a href="#PortInstance_206_60" id="PortInstance_207_5" title="Referenced at line 206">PortInstance</a>.<span class="cons_Constructor"><span id="InternalPort_207_18" title="Not referenced">InternalPort</span></span> =                         [[<a href="#ID_216_5" id="ID_207_59" title="Defined at line 216, 217, 219, 220, 221, 222, 224">ID</a>]<span class="cons_String">.</span>[<a href="#ID_216_5" id="ID_207_64" title="Defined at line 216, 217, 219, 220, 221, 222, 224">ID</a>]]
    <a href="#PortInstance_206_60" id="PortInstance_208_5" title="Referenced at line 206">PortInstance</a>.<span class="cons_Constructor"><span id="ExternalPort_208_18" title="Not referenced">ExternalPort</span></span> =                         <a href="#ID_216_5" id="ID_208_57" title="Defined at line 216, 217, 219, 220, 221, 222, 224">ID</a>

    <span class="layout">// === Workarounds =======</span>

    <a href="#OptionalComma_157_63" id="OptionalComma_212_5" title="Referenced at line 157, 160, 161">OptionalComma</a>.<span class="cons_Constructor"><span id="Comma_212_19" title="Not referenced">Comma</span></span> =                               [<span class="cons_String">,</span>]
    <a href="#OptionalComma_157_63" id="OptionalComma_213_5" title="Referenced at line 157, 160, 161">OptionalComma</a>.<span class="cons_Constructor"><span id="NoComma_213_19" title="Not referenced">NoComma</span></span> =                             []

<span class="keyword">lexical syntax</span>      <span class="layout">// keywords</span>
    <a href="#ID_66_60" id="ID_216_5" title="Referenced at line 66, 74, 84, 89, 94, 98, 101, 104, 117, 120, 121, 122, 123, 136, 152, 157, 160, 161, 163, 180, 192, 198, 207, 208">ID</a> = <span class="cons_Lit">"import"</span>       {<span class="keyword">reject</span>}
    <a href="#ID_66_60" id="ID_217_5" title="Referenced at line 66, 74, 84, 89, 94, 98, 101, 104, 117, 120, 121, 122, 123, 136, 152, 157, 160, 161, 163, 180, 192, 198, 207, 208">ID</a> = <span class="cons_Lit">"importlib"</span>    {<span class="keyword">reject</span>}

    <a href="#ID_66_60" id="ID_219_5" title="Referenced at line 66, 74, 84, 89, 94, 98, 101, 104, 117, 120, 121, 122, 123, 136, 152, 157, 160, 161, 163, 180, 192, 198, 207, 208">ID</a> = <span class="cons_Lit">"data"</span>         {<span class="keyword">reject</span>}
    <a href="#ID_66_60" id="ID_220_5" title="Referenced at line 66, 74, 84, 89, 94, 98, 101, 104, 117, 120, 121, 122, 123, 136, 152, 157, 160, 161, 163, 180, 192, 198, 207, 208">ID</a> = <span class="cons_Lit">"process"</span>      {<span class="keyword">reject</span>}
    <a href="#ID_66_60" id="ID_221_5" title="Referenced at line 66, 74, 84, 89, 94, 98, 101, 104, 117, 120, 121, 122, 123, 136, 152, 157, 160, 161, 163, 180, 192, 198, 207, 208">ID</a> = <span class="cons_Lit">"cluster"</span>      {<span class="keyword">reject</span>}
    <a href="#ID_66_60" id="ID_222_5" title="Referenced at line 66, 74, 84, 89, 94, 98, 101, 104, 117, 120, 121, 122, 123, 136, 152, 157, 160, 161, 163, 180, 192, 198, 207, 208">ID</a> = <span class="cons_Lit">"system"</span>       {<span class="keyword">reject</span>}

    <a href="#ID_66_60" id="ID_224_5" title="Referenced at line 66, 74, 84, 89, 94, 98, 101, 104, 117, 120, 121, 122, 123, 136, 152, 157, 160, 161, 163, 180, 192, 198, 207, 208">ID</a> = <span class="cons_Lit">"native"</span>       {<span class="keyword">reject</span>}

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
