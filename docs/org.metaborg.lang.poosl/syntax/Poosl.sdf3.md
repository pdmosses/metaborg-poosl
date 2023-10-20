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
<td class="code"><pre><code><span class="keyword">module</span> <a href="../Stratego-Poosl.sdf3/#Poosl_197_202" id="Poosl_7_12" title="Referenced at ../Stratego-Poosl.sdf3 line 11">Poosl</a>

<span class="keyword">imports</span>
    <a href="../Common.sdf3/#Common_7_13" id="Common_26_32" title="Defined at ../Common.sdf3 line 1">Common</a>
    <a href="../ExprStat.sdf3/#ExprStat_7_15" id="ExprStat_37_45" title="Defined at ../ExprStat.sdf3 line 1">ExprStat</a>

<span class="keyword">context-free start-symbols</span>
    <a href="#Poosl_108_113" id="Poosl_78_83" title="Defined at line 11, 50">Poosl</a>

<span class="keyword">context-free sorts</span>
    <a href="#Poosl_78_83" id="Poosl_108_113" title="Referenced at line 8">Poosl</a>
    <a href="#ImportList_819_829" id="ImportList_118_128" title="Referenced at line 51">ImportList</a>
    <a href="#Import_917_923" id="Import_133_139" title="Referenced at line 55">Import</a>
    <a href="#AnnotationList_1592_1606" id="AnnotationList_144_158" title="Referenced at line 73, 83, 88, 93, 135, 151, 170, 179, 191, 202">AnnotationList</a>
    <a href="#Annotation_1284_1294" id="Annotation_163_173" title="Referenced at line 65">Annotation</a>
    <a href="#OptAnnotationArgs_1359_1376" id="OptAnnotationArgs_178_195" title="Referenced at line 66">OptAnnotationArgs</a>
    <a href="#Class_992_997" id="Class_200_205" title="Referenced at line 56">Class</a>
    <a href="#ClassList_840_849" id="ClassList_210_219" title="Referenced at line 52">ClassList</a>
    <a href="#DataMethodList_1748_1762" id="DataMethodList_224_238" title="Referenced at line 78">DataMethodList</a>
    <a href="#DataMethod_1830_1840" id="DataMethod_243_253" title="Referenced at line 81">DataMethod</a>
    <a href="#OperatorBinary_2233_2247" id="OperatorBinary_258_272" title="Referenced at line 94, 104">OperatorBinary</a>
    <a href="#NativeClause_1617_1629" id="NativeClause_277_289" title="Referenced at line 74">NativeClause</a>
    <a href="#ExtendsClause_1648_1661" id="ExtendsClause_294_307" title="Referenced at line 74, 136">ExtendsClause</a>
    <a href="#IDList_3300_3306" id="IDList_312_318" title="Referenced at line 121, 122, 123">IDList</a>
    <a href="#Declaration_2250_2261" id="Declaration_323_334" title="Referenced at line 94, 104, 126, 127, 129">Declaration</a>
    <a href="#DeclarationOptCommaList_1694_1717" id="DeclarationOptCommaList_339_362" title="Referenced at line 76, 142">DeclarationOptCommaList</a>
    <a href="#DeclarationOptComma_3525_3544" id="DeclarationOptComma_367_386" title="Referenced at line 125">DeclarationOptComma</a>
    <a href="#ParameterList_4473_4486" id="ParameterList_391_404" title="Referenced at line 152">ParameterList</a>
    <a href="#OptEmptyList_2088_2100" id="OptEmptyList_409_421" title="Referenced at line 89, 101">OptEmptyList</a>
    <a href="#OptParameterList_1925_1941" id="OptParameterList_426_442" title="Referenced at line 84, 98, 136, 180">OptParameterList</a>
    <a href="#OptLocalVariableList_1951_1971" id="OptLocalVariableList_447_467" title="Referenced at line 84, 89, 94, 152">OptLocalVariableList</a>
    <a href="#ProcessMethodList_4289_4306" id="ProcessMethodList_472_489" title="Referenced at line 146">ProcessMethodList</a>
    <a href="#ProcessMethod_4374_4387" id="ProcessMethod_494_507" title="Referenced at line 149">ProcessMethod</a>
    <a href="#PortList_4097_4105" id="PortList_512_520" title="Referenced at line 138, 182">PortList</a>
    <a href="#Port_4616_4620" id="Port_525_529" title="Referenced at line 156">Port</a>
    <a href="#MessageSignatureList_4137_4157" id="MessageSignatureList_534_554" title="Referenced at line 140">MessageSignatureList</a>
    <a href="#MessageSignature_4768_4784" id="MessageSignature_559_575" title="Referenced at line 159">MessageSignature</a>
    <a href="#OptMessageParameterList_4861_4884" id="OptMessageParameterList_580_603" title="Referenced at line 160, 161">OptMessageParameterList</a>
    <a href="#InstanceList_5284_5296" id="InstanceList_608_620" title="Referenced at line 173, 184">InstanceList</a>
    <a href="#Instance_5636_5644" id="Instance_625_633" title="Referenced at line 189">Instance</a>
    <a href="#OptInstanceParameterList_5725_5749" id="OptInstanceParameterList_638_662" title="Referenced at line 192">OptInstanceParameterList</a>
    <a href="#InstanceParameter_5818_5835" id="InstanceParameter_667_684" title="Referenced at line 195">InstanceParameter</a>
    <a href="#ChannelList_5328_5339" id="ChannelList_689_700" title="Referenced at line 175, 186">ChannelList</a>
    <a href="#Channel_6045_6052" id="Channel_705_712" title="Referenced at line 200">Channel</a>
    <a href="#PortInstance_6208_6220" id="PortInstance_717_729" title="Referenced at line 206">PortInstance</a>
    <a href="#PortInstanceList_6122_6138" id="PortInstanceList_734_750" title="Referenced at line 203">PortInstanceList</a>
    <a href="#OptionalComma_4692_4705" id="OptionalComma_755_768" title="Referenced at line 157, 160, 161">OptionalComma</a>

<span class="keyword">context-free syntax</span>
    <a href="#Poosl_78_83" id="Poosl_794_799" title="Referenced at line 8">Poosl</a>.<span class="cons_Constructor"><span id="Poosl_800_805" title="Not referenced locally, nor via imports">Poosl</span></span> = [
        [<a href="#ImportList_118_128" id="ImportList_819_829" title="Defined at line 12, 55">ImportList</a>]
        [<a href="#ClassList_210_219" id="ClassList_840_849" title="Defined at line 18, 56">ClassList</a>]
    ]

    <a href="#ImportList_819_829" id="ImportList_862_872" title="Referenced at line 51">ImportList</a>.<span class="cons_Constructor"><span id="ImportList_873_883" title="Not referenced locally, nor via imports">ImportList</span></span> =                             [[{<a href="#Import_133_139" id="Import_917_923" title="Defined at line 13, 60, 61">Import</a> <span class="cons_Lit">"\n"</span>}*]]
    <a href="#ClassList_840_849" id="ClassList_937_946" title="Referenced at line 52">ClassList</a>.<span class="cons_Constructor"><span id="ClassList_947_956" title="Not referenced locally, nor via imports">ClassList</span></span> =                               [[{<a href="#Class_200_205" id="Class_992_997" title="Defined at line 17, 72, 134, 169, 178">Class</a> <span class="cons_Lit">"\n\n"</span>}*]]

    <span class="layout">// === Multiple files =======</span>

    <a href="#Import_917_923" id="Import_1049_1055" title="Referenced at line 55">Import</a>.<span class="cons_Constructor"><span id="Import_1056_1062" title="Not referenced locally, nor via imports">Import</span></span> =                                     [<span class="cons_String">import</span> [<a href="../Common.sdf3/#STRING_1285_1291" id="STRING_1110_1116" title="Defined at ../Common.sdf3 line 62, 66">STRING</a>]]
    <a href="#Import_917_923" id="Import_1123_1129" title="Referenced at line 55">Import</a>.<span class="cons_Constructor"><span id="ImportLib_1130_1139" title="Not referenced locally, nor via imports">ImportLib</span></span> =                                  [<span class="cons_String">importlib</span> [<a href="../Common.sdf3/#STRING_1285_1291" id="STRING_1187_1193" title="Defined at ../Common.sdf3 line 62, 66">STRING</a>]]

    <span class="layout">// === Annotation =======</span>

    <a href="#AnnotationList_1592_1606" id="AnnotationList_1232_1246" title="Referenced at line 73, 83, 88, 93, 135, 151, 170, 179, 191, 202">AnnotationList</a>.<span class="cons_Constructor"><span id="AnnotationList_1247_1261" title="Not referenced locally, nor via imports">AnnotationList</span></span> =                     <a href="#Annotation_163_173" id="Annotation_1284_1294" title="Defined at line 15, 66">Annotation</a>*
    <a href="#Annotation_1284_1294" id="Annotation_1300_1310" title="Referenced at line 65">Annotation</a>.<span class="cons_Constructor"><span id="Annotation_1311_1321" title="Not referenced locally, nor via imports">Annotation</span></span> =                             [<span class="cons_String">@</span>[<a href="#ID_6546_6548" id="ID_1355_1357" title="Defined at line 216, 217, 219, 220, 221, 222, 224">ID</a>][<a href="#OptAnnotationArgs_178_195" id="OptAnnotationArgs_1359_1376" title="Defined at line 16, 67, 68">OptAnnotationArgs</a>]]
    <a href="#OptAnnotationArgs_1359_1376" id="OptAnnotationArgs_1383_1400" title="Referenced at line 66">OptAnnotationArgs</a>.<span class="cons_Constructor"><span id="AnnotationArgs_1401_1415" title="Not referenced locally, nor via imports">AnnotationArgs</span></span> =                  [<span class="cons_String">(</span>[{<a href="../ExprStat.sdf3/#ExpressionConstant_395_413" id="ExpressionConstant_1439_1457" title="Defined at ../ExprStat.sdf3 line 25, 179, 180, 181, 182, 183, 184, 185, 186">ExpressionConstant</a> <span class="cons_Lit">", "</span>}*]<span class="cons_String">)</span>]
    <a href="#OptAnnotationArgs_1359_1376" id="OptAnnotationArgs_1472_1489" title="Referenced at line 66">OptAnnotationArgs</a>.<span class="cons_Constructor"><span id="NoAnnotationArgs_1490_1506" title="Not referenced locally, nor via imports">NoAnnotationArgs</span></span> =                []

    <span class="layout">// === Data Class =======</span>

    <a href="#Class_992_997" id="Class_1563_1568" title="Referenced at line 56">Class</a>.<span class="cons_Constructor"><span id="DataClass_1569_1578" title="Not referenced locally, nor via imports">DataClass</span></span> = [
        [<a href="#AnnotationList_144_158" id="AnnotationList_1592_1606" title="Defined at line 14, 65">AnnotationList</a>]
        [<a href="#NativeClause_277_289" id="NativeClause_1617_1629" title="Defined at line 22, 114, 115">NativeClause</a>] <span class="cons_String">data</span> <span class="cons_String">class</span> [<a href="#ID_6546_6548" id="ID_1643_1645" title="Defined at line 216, 217, 219, 220, 221, 222, 224">ID</a>] [<a href="#ExtendsClause_294_307" id="ExtendsClause_1648_1661" title="Defined at line 23, 117, 118">ExtendsClause</a>]
        <span class="cons_String">variables</span>
            [<a href="#DeclarationOptCommaList_339_362" id="DeclarationOptCommaList_1694_1717" title="Defined at line 26, 125">DeclarationOptCommaList</a>]
        <span class="cons_String">methods</span>
            [<a href="#DataMethodList_224_238" id="DataMethodList_1748_1762" title="Defined at line 19, 81">DataMethodList</a>]
    ]

    <a href="#DataMethodList_1748_1762" id="DataMethodList_1775_1789" title="Referenced at line 78">DataMethodList</a>.<span class="cons_Constructor"><span id="DataMethodList_1790_1804" title="Not referenced locally, nor via imports">DataMethodList</span></span> =                     [[{<a href="#DataMethod_243_253" id="DataMethod_1830_1840" title="Defined at line 20, 82, 87, 92, 97, 100, 103">DataMethod</a> <span class="cons_Lit">"\n\n"</span>}*]]
    <a href="#DataMethod_1830_1840" id="DataMethod_1856_1866" title="Referenced at line 81">DataMethod</a>.<span class="cons_Constructor"><span id="DataMethodNamed_1867_1882" title="Not referenced locally, nor via imports">DataMethodNamed</span></span> = [
        [<a href="#AnnotationList_144_158" id="AnnotationList_1896_1910" title="Defined at line 14, 65">AnnotationList</a>]
        [<a href="#ID_6546_6548" id="ID_1921_1923" title="Defined at line 216, 217, 219, 220, 221, 222, 224">ID</a>][<a href="#OptParameterList_426_442" id="OptParameterList_1925_1941" title="Defined at line 30, 127, 128">OptParameterList</a>] <span class="cons_String">:</span> [<a href="#ID_6546_6548" id="ID_1946_1948" title="Defined at line 216, 217, 219, 220, 221, 222, 224">ID</a>] [<a href="#OptLocalVariableList_447_467" id="OptLocalVariableList_1951_1971" title="Defined at line 31, 129, 130">OptLocalVariableList</a>]
            [<a href="../ExprStat.sdf3/#Expression_214_224" id="Expression_1986_1996" title="Defined at ../ExprStat.sdf3 line 16, 135">Expression</a>]
    ]
    <a href="#DataMethod_1830_1840" id="DataMethod_2008_2018" title="Referenced at line 81">DataMethod</a>.<span class="cons_Constructor"><span id="DataMethodUnary_2019_2034" title="Not referenced locally, nor via imports">DataMethodUnary</span></span> = [
        [<a href="#AnnotationList_144_158" id="AnnotationList_2048_2062" title="Defined at line 14, 65">AnnotationList</a>]
        [<a href="../ExprStat.sdf3/#UnaryOperator_418_431" id="UnaryOperator_2073_2086" title="Defined at ../ExprStat.sdf3 line 26, 206, 207">UnaryOperator</a>][<a href="#OptEmptyList_409_421" id="OptEmptyList_2088_2100" title="Defined at line 29, 107, 108">OptEmptyList</a>] <span class="cons_String">:</span> [<a href="#ID_6546_6548" id="ID_2105_2107" title="Defined at line 216, 217, 219, 220, 221, 222, 224">ID</a>] [<a href="#OptLocalVariableList_447_467" id="OptLocalVariableList_2110_2130" title="Defined at line 31, 129, 130">OptLocalVariableList</a>]
            [<a href="../ExprStat.sdf3/#Expression_214_224" id="Expression_2145_2155" title="Defined at ../ExprStat.sdf3 line 16, 135">Expression</a>]
    ]
    <a href="#DataMethod_1830_1840" id="DataMethod_2167_2177" title="Referenced at line 81">DataMethod</a>.<span class="cons_Constructor"><span id="DataMethodBinary_2178_2194" title="Not referenced locally, nor via imports">DataMethodBinary</span></span> = [
        [<a href="#AnnotationList_144_158" id="AnnotationList_2208_2222" title="Defined at line 14, 65">AnnotationList</a>]
        [<a href="#OperatorBinary_258_272" id="OperatorBinary_2233_2247" title="Defined at line 21, 110, 111, 112">OperatorBinary</a>]<span class="cons_String">(</span>[<a href="#Declaration_323_334" id="Declaration_2250_2261" title="Defined at line 25, 121">Declaration</a>]<span class="cons_String">)</span> <span class="cons_String">:</span> [<a href="#ID_6546_6548" id="ID_2267_2269" title="Defined at line 216, 217, 219, 220, 221, 222, 224">ID</a>] [<a href="#OptLocalVariableList_447_467" id="OptLocalVariableList_2272_2292" title="Defined at line 31, 129, 130">OptLocalVariableList</a>]
            [<a href="../ExprStat.sdf3/#Expression_214_224" id="Expression_2307_2317" title="Defined at ../ExprStat.sdf3 line 16, 135">Expression</a>]
    ]
    <a href="#DataMethod_1830_1840" id="DataMethod_2329_2339" title="Referenced at line 81">DataMethod</a>.<span class="cons_Constructor"><span id="DataMethodNamedNative_2340_2361" title="Not referenced locally, nor via imports">DataMethodNamedNative</span></span> = [
        <span class="cons_String">native</span> [<a href="#ID_6546_6548" id="ID_2382_2384" title="Defined at line 216, 217, 219, 220, 221, 222, 224">ID</a>][<a href="#OptParameterList_426_442" id="OptParameterList_2386_2402" title="Defined at line 30, 127, 128">OptParameterList</a>] <span class="cons_String">:</span> [<a href="#ID_6546_6548" id="ID_2407_2409" title="Defined at line 216, 217, 219, 220, 221, 222, 224">ID</a>]
    ]
    <a href="#DataMethod_1830_1840" id="DataMethod_2421_2431" title="Referenced at line 81">DataMethod</a>.<span class="cons_Constructor"><span id="DataMethodUnaryNative_2432_2453" title="Not referenced locally, nor via imports">DataMethodUnaryNative</span></span> = [
        <span class="cons_String">native</span> [<a href="../ExprStat.sdf3/#UnaryOperator_418_431" id="UnaryOperator_2474_2487" title="Defined at ../ExprStat.sdf3 line 26, 206, 207">UnaryOperator</a>][<a href="#OptEmptyList_409_421" id="OptEmptyList_2489_2501" title="Defined at line 29, 107, 108">OptEmptyList</a>] <span class="cons_String">:</span> [<a href="#ID_6546_6548" id="ID_2506_2508" title="Defined at line 216, 217, 219, 220, 221, 222, 224">ID</a>]
    ]
    <a href="#DataMethod_1830_1840" id="DataMethod_2520_2530" title="Referenced at line 81">DataMethod</a>.<span class="cons_Constructor"><span id="DataMethodBinaryNative_2531_2553" title="Not referenced locally, nor via imports">DataMethodBinaryNative</span></span> = [
        <span class="cons_String">native</span> [<a href="#OperatorBinary_258_272" id="OperatorBinary_2574_2588" title="Defined at line 21, 110, 111, 112">OperatorBinary</a>]<span class="cons_String">(</span>[<a href="#Declaration_323_334" id="Declaration_2591_2602" title="Defined at line 25, 121">Declaration</a>]<span class="cons_String">)</span> <span class="cons_String">:</span> [<a href="#ID_6546_6548" id="ID_2608_2610" title="Defined at line 216, 217, 219, 220, 221, 222, 224">ID</a>]
    ]

    <a href="#OptEmptyList_2088_2100" id="OptEmptyList_2623_2635" title="Referenced at line 89, 101">OptEmptyList</a>.<span class="cons_Constructor"><span id="NoList_2636_2642" title="Not referenced locally, nor via imports">NoList</span></span> = []
    <a href="#OptEmptyList_2088_2100" id="OptEmptyList_2652_2664" title="Referenced at line 89, 101">OptEmptyList</a>.<span class="cons_Constructor"><span id="EmptyList_2665_2674" title="Not referenced locally, nor via imports">EmptyList</span></span> = [<span class="cons_String">()</span>]

    <a href="#OperatorBinary_2233_2247" id="OperatorBinary_2687_2701" title="Referenced at line 94, 104">OperatorBinary</a>.<span class="cons_Constructor"><span id="OperatorBinary2_2702_2717" title="Not referenced locally, nor via imports">OperatorBinary2</span></span> =                    <a href="../ExprStat.sdf3/#BinaryOperatorLevel2_436_456" id="BinaryOperatorLevel2_2739_2759" title="Defined at ../ExprStat.sdf3 line 27, 209, 210, 211, 212, 213, 214, 215, 216">BinaryOperatorLevel2</a>
    <a href="#OperatorBinary_2233_2247" id="OperatorBinary_2764_2778" title="Referenced at line 94, 104">OperatorBinary</a>.<span class="cons_Constructor"><span id="OperatorBinary3_2779_2794" title="Not referenced locally, nor via imports">OperatorBinary3</span></span> =                    <a href="../ExprStat.sdf3/#BinaryOperatorLevel3_461_481" id="BinaryOperatorLevel3_2816_2836" title="Defined at ../ExprStat.sdf3 line 28, 218, 219, 220, 221">BinaryOperatorLevel3</a>
    <a href="#OperatorBinary_2233_2247" id="OperatorBinary_2841_2855" title="Referenced at line 94, 104">OperatorBinary</a>.<span class="cons_Constructor"><span id="OperatorBinary4_2856_2871" title="Not referenced locally, nor via imports">OperatorBinary4</span></span> =                    <a href="../ExprStat.sdf3/#BinaryOperatorLevel4_486_506" id="BinaryOperatorLevel4_2893_2913" title="Defined at ../ExprStat.sdf3 line 29, 223, 224">BinaryOperatorLevel4</a>

    <a href="#NativeClause_1617_1629" id="NativeClause_2919_2931" title="Referenced at line 74">NativeClause</a>.<span class="cons_Constructor"><span id="Native_2932_2938" title="Not referenced locally, nor via imports">Native</span></span> =                               [<span class="cons_String">native</span>]
    <a href="#NativeClause_1617_1629" id="NativeClause_2984_2996" title="Referenced at line 74">NativeClause</a>.<span class="cons_Constructor"><span id="NotNative_2997_3006" title="Not referenced locally, nor via imports">NotNative</span></span> =                            []

    <a href="#ExtendsClause_1648_1661" id="ExtendsClause_3044_3057" title="Referenced at line 74, 136">ExtendsClause</a>.<span class="cons_Constructor"><span id="Extends_3058_3065" title="Not referenced locally, nor via imports">Extends</span></span> =                             [<span class="cons_String">extends</span> [<a href="#ID_6546_6548" id="ID_3106_3108" title="Defined at line 216, 217, 219, 220, 221, 222, 224">ID</a>]]
    <a href="#ExtendsClause_1648_1661" id="ExtendsClause_3115_3128" title="Referenced at line 74, 136">ExtendsClause</a>.<span class="cons_Constructor"><span id="NoExtends_3129_3138" title="Not referenced locally, nor via imports">NoExtends</span></span> =                           []

    <a href="#IDList_3300_3306" id="IDList_3175_3181" title="Referenced at line 121, 122, 123">IDList</a>.<span class="cons_Constructor"><span id="IDList_3182_3188" title="Not referenced locally, nor via imports">IDList</span></span> =                                     [[{<a href="#ID_6546_6548" id="ID_3230_3232" title="Defined at line 216, 217, 219, 220, 221, 222, 224">ID</a> <span class="cons_Lit">", "</span>}*]]
    <a href="#Declaration_2250_2261" id="Declaration_3246_3257" title="Referenced at line 94, 104, 126, 127, 129">Declaration</a>.<span class="cons_Constructor"><span id="Declaration_3258_3269" title="Not referenced locally, nor via imports">Declaration</span></span> =                           [[<a href="#IDList_312_318" id="IDList_3300_3306" title="Defined at line 24, 120">IDList</a>] <span class="cons_String">:</span> [<a href="#ID_6546_6548" id="ID_3311_3313" title="Defined at line 216, 217, 219, 220, 221, 222, 224">ID</a>]]
    <a href="#DeclarationOptComma_3525_3544" id="DeclarationOptComma_3320_3339" title="Referenced at line 125">DeclarationOptComma</a>.<span class="cons_Constructor"><span id="DeclarationWithComma_3340_3360" title="Not referenced locally, nor via imports">DeclarationWithComma</span></span> =          [[<a href="#IDList_312_318" id="IDList_3374_3380" title="Defined at line 24, 120">IDList</a>] <span class="cons_String">:</span> [<a href="#ID_6546_6548" id="ID_3385_3387" title="Defined at line 216, 217, 219, 220, 221, 222, 224">ID</a>]<span class="cons_String">,</span>]
    <a href="#DeclarationOptComma_3525_3544" id="DeclarationOptComma_3395_3414" title="Referenced at line 125">DeclarationOptComma</a>.<span class="cons_Constructor"><span id="DeclarationWithoutComma_3415_3438" title="Not referenced locally, nor via imports">DeclarationWithoutComma</span></span> =       [[<a href="#IDList_312_318" id="IDList_3449_3455" title="Defined at line 24, 120">IDList</a>] <span class="cons_String">:</span> [<a href="#ID_6546_6548" id="ID_3460_3462" title="Defined at line 216, 217, 219, 220, 221, 222, 224">ID</a>]]

    <a href="#DeclarationOptCommaList_1694_1717" id="DeclarationOptCommaList_3470_3493" title="Referenced at line 76, 142">DeclarationOptCommaList</a>.<span class="cons_Constructor"><span id="DeclarationOptCommaList_3494_3517" title="Not referenced locally, nor via imports">DeclarationOptCommaList</span></span> =   [[{<a href="#DeclarationOptComma_367_386" id="DeclarationOptComma_3525_3544" title="Defined at line 27, 122, 123">DeclarationOptComma</a> <span class="cons_Lit">"\n"</span>}*]] 
    <a href="#ParameterList_4473_4486" id="ParameterList_3559_3572" title="Referenced at line 152">ParameterList</a>.<span class="cons_Constructor"><span id="ParameterList_3573_3586" title="Not referenced locally, nor via imports">ParameterList</span></span> =                       [<span class="cons_String">(</span>[{<a href="#Declaration_323_334" id="Declaration_3615_3626" title="Defined at line 25, 121">Declaration</a> <span class="cons_Lit">", "</span>}*]<span class="cons_String">)</span>]
    <a href="#OptParameterList_1925_1941" id="OptParameterList_3641_3657" title="Referenced at line 84, 98, 136, 180">OptParameterList</a>.<span class="cons_Constructor"><span id="Parameters_3658_3668" title="Not referenced locally, nor via imports">Parameters</span></span> =                       [<span class="cons_String">(</span>[{<a href="#Declaration_323_334" id="Declaration_3697_3708" title="Defined at line 25, 121">Declaration</a> <span class="cons_Lit">", "</span>}*]<span class="cons_String">)</span>]
    <a href="#OptParameterList_1925_1941" id="OptParameterList_3723_3739" title="Referenced at line 84, 98, 136, 180">OptParameterList</a>.<span class="cons_Constructor"><span id="NoParameters_3740_3752" title="Not referenced locally, nor via imports">NoParameters</span></span> =                     []
    <a href="#OptLocalVariableList_1951_1971" id="OptLocalVariableList_3782_3802" title="Referenced at line 84, 89, 94, 152">OptLocalVariableList</a>.<span class="cons_Constructor"><span id="LocalVariables_3803_3817" title="Not referenced locally, nor via imports">LocalVariables</span></span> =               [<span class="cons_String">|</span> [{<a href="#Declaration_323_334" id="Declaration_3839_3850" title="Defined at line 25, 121">Declaration</a> <span class="cons_Lit">", "</span>}*] <span class="cons_String">|</span>]
    <a href="#OptLocalVariableList_1951_1971" id="OptLocalVariableList_3866_3886" title="Referenced at line 84, 89, 94, 152">OptLocalVariableList</a>.<span class="cons_Constructor"><span id="NoLocalVariables_3887_3903" title="Not referenced locally, nor via imports">NoLocalVariables</span></span> =             []

    <span class="layout">// === Process Class =======</span>
 
    <a href="#Class_992_997" id="Class_3961_3966" title="Referenced at line 56">Class</a>.<span class="cons_Constructor"><span id="ProcessClass_3967_3979" title="Not referenced locally, nor via imports">ProcessClass</span></span> = [
        [<a href="#AnnotationList_144_158" id="AnnotationList_3993_4007" title="Defined at line 14, 65">AnnotationList</a>]
        <span class="cons_String">process</span> <span class="cons_String">class</span> [<a href="#ID_6546_6548" id="ID_4032_4034" title="Defined at line 216, 217, 219, 220, 221, 222, 224">ID</a>][<a href="#OptParameterList_426_442" id="OptParameterList_4036_4052" title="Defined at line 30, 127, 128">OptParameterList</a>] [<a href="#ExtendsClause_294_307" id="ExtendsClause_4055_4068" title="Defined at line 23, 117, 118">ExtendsClause</a>]
        <span class="cons_String">ports</span>
            [<a href="#PortList_512_520" id="PortList_4097_4105" title="Defined at line 34, 156">PortList</a>]
        <span class="cons_String">messages</span>
            [<a href="#MessageSignatureList_534_554" id="MessageSignatureList_4137_4157" title="Defined at line 36, 159">MessageSignatureList</a>]
        <span class="cons_String">variables</span>
            [<a href="#DeclarationOptCommaList_339_362" id="DeclarationOptCommaList_4190_4213" title="Defined at line 26, 125">DeclarationOptCommaList</a>]
        <span class="cons_String">init</span>
            [<a href="../ExprStat.sdf3/#ProcessMethodCall_127_144" id="ProcessMethodCall_4241_4258" title="Defined at ../ExprStat.sdf3 line 11, 101">ProcessMethodCall</a>]
        <span class="cons_String">methods</span>
            [<a href="#ProcessMethodList_472_489" id="ProcessMethodList_4289_4306" title="Defined at line 32, 149">ProcessMethodList</a>]
    ]

    <a href="#ProcessMethodList_4289_4306" id="ProcessMethodList_4319_4336" title="Referenced at line 146">ProcessMethodList</a>.<span class="cons_Constructor"><span id="ProcessMethodList_4337_4354" title="Not referenced locally, nor via imports">ProcessMethodList</span></span> =               [[{<a href="#ProcessMethod_494_507" id="ProcessMethod_4374_4387" title="Defined at line 33, 150">ProcessMethod</a> <span class="cons_Lit">"\n\n"</span>}*]]
    <a href="#ProcessMethod_4374_4387" id="ProcessMethod_4403_4416" title="Referenced at line 149">ProcessMethod</a>.<span class="cons_Constructor"><span id="ProcessMethod_4417_4430" title="Not referenced locally, nor via imports">ProcessMethod</span></span> = [
        [<a href="#AnnotationList_144_158" id="AnnotationList_4444_4458" title="Defined at line 14, 65">AnnotationList</a>]
        [<a href="#ID_6546_6548" id="ID_4469_4471" title="Defined at line 216, 217, 219, 220, 221, 222, 224">ID</a>][<a href="#ParameterList_391_404" id="ParameterList_4473_4486" title="Defined at line 28, 126">ParameterList</a>][<a href="#ParameterList_391_404" id="ParameterList_4488_4501" title="Defined at line 28, 126">ParameterList</a>] [<a href="#OptLocalVariableList_447_467" id="OptLocalVariableList_4504_4524" title="Defined at line 31, 129, 130">OptLocalVariableList</a>]
            [<a href="../ExprStat.sdf3/#Statement_60_69" id="Statement_4539_4548" title="Defined at ../ExprStat.sdf3 line 7, 38">Statement</a>]
    ]

    <a href="#PortList_4097_4105" id="PortList_4561_4569" title="Referenced at line 138, 182">PortList</a>.<span class="cons_Constructor"><span id="PortList_4570_4578" title="Not referenced locally, nor via imports">PortList</span></span> =                                 [[{<a href="#Port_525_529" id="Port_4616_4620" title="Defined at line 35, 157">Port</a> <span class="cons_Lit">"\n"</span>}*]]
    <a href="#Port_4616_4620" id="Port_4634_4638" title="Referenced at line 156">Port</a>.<span class="cons_Constructor"><span id="Port_4639_4643" title="Not referenced locally, nor via imports">Port</span></span> =                                         [[<a href="#ID_6546_6548" id="ID_4688_4690" title="Defined at line 216, 217, 219, 220, 221, 222, 224">ID</a>][<a href="#OptionalComma_755_768" id="OptionalComma_4692_4705" title="Defined at line 47, 212, 213">OptionalComma</a>]]

    <a href="#MessageSignatureList_4137_4157" id="MessageSignatureList_4713_4733" title="Referenced at line 140">MessageSignatureList</a>.<span class="cons_Constructor"><span id="MessageSignatureList_4734_4754" title="Not referenced locally, nor via imports">MessageSignatureList</span></span> =         [[{<a href="#MessageSignature_559_575" id="MessageSignature_4768_4784" title="Defined at line 37, 160, 161">MessageSignature</a> <span class="cons_Lit">"\n"</span>}*]]
    <a href="#MessageSignature_4768_4784" id="MessageSignature_4798_4814" title="Referenced at line 159">MessageSignature</a>.<span class="cons_Constructor"><span id="MessageReceiveSignature_4815_4838" title="Not referenced locally, nor via imports">MessageReceiveSignature</span></span> =          [[<a href="#ID_6546_6548" id="ID_4852_4854" title="Defined at line 216, 217, 219, 220, 221, 222, 224">ID</a>]<span class="cons_String">?</span>[<a href="#ID_6546_6548" id="ID_4857_4859" title="Defined at line 216, 217, 219, 220, 221, 222, 224">ID</a>][<a href="#OptMessageParameterList_580_603" id="OptMessageParameterList_4861_4884" title="Defined at line 38, 163, 164">OptMessageParameterList</a>][<a href="#OptionalComma_755_768" id="OptionalComma_4886_4899" title="Defined at line 47, 212, 213">OptionalComma</a>]] 
    <a href="#MessageSignature_4768_4784" id="MessageSignature_4907_4923" title="Referenced at line 159">MessageSignature</a>.<span class="cons_Constructor"><span id="MessageSendSignature_4924_4944" title="Not referenced locally, nor via imports">MessageSendSignature</span></span> =             [[<a href="#ID_6546_6548" id="ID_4961_4963" title="Defined at line 216, 217, 219, 220, 221, 222, 224">ID</a>]<span class="cons_String">!</span>[<a href="#ID_6546_6548" id="ID_4966_4968" title="Defined at line 216, 217, 219, 220, 221, 222, 224">ID</a>][<a href="#OptMessageParameterList_580_603" id="OptMessageParameterList_4970_4993" title="Defined at line 38, 163, 164">OptMessageParameterList</a>][<a href="#OptionalComma_755_768" id="OptionalComma_4995_5008" title="Defined at line 47, 212, 213">OptionalComma</a>]]

    <a href="#OptMessageParameterList_4861_4884" id="OptMessageParameterList_5016_5039" title="Referenced at line 160, 161">OptMessageParameterList</a>.<span class="cons_Constructor"><span id="MessageParameters_5040_5057" title="Not referenced locally, nor via imports">MessageParameters</span></span> =         [<span class="cons_String">(</span>[{<a href="#ID_6546_6548" id="ID_5072_5074" title="Defined at line 216, 217, 219, 220, 221, 222, 224">ID</a> <span class="cons_Lit">", "</span>}*]<span class="cons_String">)</span>]
    <a href="#OptMessageParameterList_4861_4884" id="OptMessageParameterList_5089_5112" title="Referenced at line 160, 161">OptMessageParameterList</a>.<span class="cons_Constructor"><span id="NoMessageParameters_5113_5132" title="Not referenced locally, nor via imports">NoMessageParameters</span></span> =       []


    <span class="layout">// === System and Cluster Class =======</span>

    <a href="#Class_992_997" id="Class_5195_5200" title="Referenced at line 56">Class</a>.<span class="cons_Constructor"><span id="System_5201_5207" title="Not referenced locally, nor via imports">System</span></span> =  [
        [<a href="#AnnotationList_144_158" id="AnnotationList_5222_5236" title="Defined at line 14, 65">AnnotationList</a>]
        <span class="cons_String">system</span>
        <span class="cons_String">instances</span>
            [<a href="#InstanceList_608_620" id="InstanceList_5284_5296" title="Defined at line 39, 189">InstanceList</a>]
        <span class="cons_String">channels</span>
            [<a href="#ChannelList_689_700" id="ChannelList_5328_5339" title="Defined at line 43, 200">ChannelList</a>]
    ]

    <a href="#Class_992_997" id="Class_5352_5357" title="Referenced at line 56">Class</a>.<span class="cons_Constructor"><span id="ClusterClass_5358_5370" title="Not referenced locally, nor via imports">ClusterClass</span></span> = [
        [<a href="#AnnotationList_144_158" id="AnnotationList_5384_5398" title="Defined at line 14, 65">AnnotationList</a>]
        <span class="cons_String">cluster</span> <span class="cons_String">class</span> [<a href="#ID_6546_6548" id="ID_5423_5425" title="Defined at line 216, 217, 219, 220, 221, 222, 224">ID</a>][<a href="#OptParameterList_426_442" id="OptParameterList_5427_5443" title="Defined at line 30, 127, 128">OptParameterList</a>]
        <span class="cons_String">ports</span>
            [<a href="#PortList_512_520" id="PortList_5472_5480" title="Defined at line 34, 156">PortList</a>]
        <span class="cons_String">instances</span>
            [<a href="#InstanceList_608_620" id="InstanceList_5513_5525" title="Defined at line 39, 189">InstanceList</a>]
        <span class="cons_String">channels</span>
            [<a href="#ChannelList_689_700" id="ChannelList_5557_5568" title="Defined at line 43, 200">ChannelList</a>]
    ]

    <a href="#InstanceList_5284_5296" id="InstanceList_5581_5593" title="Referenced at line 173, 184">InstanceList</a>.<span class="cons_Constructor"><span id="InstanceList_5594_5606" title="Not referenced locally, nor via imports">InstanceList</span></span> =                         [[{<a href="#Instance_625_633" id="Instance_5636_5644" title="Defined at line 40, 190">Instance</a> <span class="cons_Lit">"\n"</span>}*]]
    <a href="#Instance_5636_5644" id="Instance_5658_5666" title="Referenced at line 189">Instance</a>.<span class="cons_Constructor"><span id="Instance_5667_5675" title="Not referenced locally, nor via imports">Instance</span></span> = [
        [<a href="#AnnotationList_144_158" id="AnnotationList_5689_5703" title="Defined at line 14, 65">AnnotationList</a>]
        [<a href="#ID_6546_6548" id="ID_5714_5716" title="Defined at line 216, 217, 219, 220, 221, 222, 224">ID</a>] <span class="cons_String">:</span> [<a href="#ID_6546_6548" id="ID_5721_5723" title="Defined at line 216, 217, 219, 220, 221, 222, 224">ID</a>][<a href="#OptInstanceParameterList_638_662" id="OptInstanceParameterList_5725_5749" title="Defined at line 41, 195, 196">OptInstanceParameterList</a>]
    ]

    <a href="#OptInstanceParameterList_5725_5749" id="OptInstanceParameterList_5762_5786" title="Referenced at line 192">OptInstanceParameterList</a>.<span class="cons_Constructor"><span id="InstanceParameters_5787_5805" title="Not referenced locally, nor via imports">InstanceParameters</span></span> =       [<span class="cons_String">(</span>[{<a href="#InstanceParameter_667_684" id="InstanceParameter_5818_5835" title="Defined at line 42, 198">InstanceParameter</a> <span class="cons_Lit">", "</span>}*]<span class="cons_String">)</span>]
    <a href="#OptInstanceParameterList_5725_5749" id="OptInstanceParameterList_5850_5874" title="Referenced at line 192">OptInstanceParameterList</a>.<span class="cons_Constructor"><span id="NoInstanceParameters_5875_5895" title="Not referenced locally, nor via imports">NoInstanceParameters</span></span> =     []

    <a href="#InstanceParameter_5818_5835" id="InstanceParameter_5910_5927" title="Referenced at line 195">InstanceParameter</a>.<span class="cons_Constructor"><span id="InstanceParameter_5928_5945" title="Not referenced locally, nor via imports">InstanceParameter</span></span> =               [[<a href="#ID_6546_6548" id="ID_5964_5966" title="Defined at line 216, 217, 219, 220, 221, 222, 224">ID</a>] <span class="cons_String">:=</span> [<a href="../ExprStat.sdf3/#Expression_214_224" id="Expression_5972_5982" title="Defined at ../ExprStat.sdf3 line 16, 135">Expression</a>]]

    <a href="#ChannelList_5328_5339" id="ChannelList_5990_6001" title="Referenced at line 175, 186">ChannelList</a>.<span class="cons_Constructor"><span id="ChannelList_6002_6013" title="Not referenced locally, nor via imports">ChannelList</span></span> =                           [[{<a href="#Channel_705_712" id="Channel_6045_6052" title="Defined at line 44, 201">Channel</a> <span class="cons_Lit">"\n"</span>}*]]
    <a href="#Channel_6045_6052" id="Channel_6066_6073" title="Referenced at line 200">Channel</a>.<span class="cons_Constructor"><span id="Channel_6074_6081" title="Not referenced locally, nor via imports">Channel</span></span> = [
        [<a href="#AnnotationList_144_158" id="AnnotationList_6095_6109" title="Defined at line 14, 65">AnnotationList</a>]
        <span class="cons_String">{</span> [<a href="#PortInstanceList_734_750" id="PortInstanceList_6122_6138" title="Defined at line 46, 206">PortInstanceList</a>] <span class="cons_String">}</span>
    ]

    <a href="#PortInstanceList_6122_6138" id="PortInstanceList_6153_6169" title="Referenced at line 203">PortInstanceList</a>.<span class="cons_Constructor"><span id="PortInstanceList_6170_6186" title="Not referenced locally, nor via imports">PortInstanceList</span></span> =                 [[{<a href="#PortInstance_717_729" id="PortInstance_6208_6220" title="Defined at line 45, 207, 208">PortInstance</a> <span class="cons_Lit">", "</span>}+]]
    <a href="#PortInstance_6208_6220" id="PortInstance_6234_6246" title="Referenced at line 206">PortInstance</a>.<span class="cons_Constructor"><span id="InternalPort_6247_6259" title="Not referenced locally, nor via imports">InternalPort</span></span> =                         [[<a href="#ID_6546_6548" id="ID_6288_6290" title="Defined at line 216, 217, 219, 220, 221, 222, 224">ID</a>]<span class="cons_String">.</span>[<a href="#ID_6546_6548" id="ID_6293_6295" title="Defined at line 216, 217, 219, 220, 221, 222, 224">ID</a>]]
    <a href="#PortInstance_6208_6220" id="PortInstance_6302_6314" title="Referenced at line 206">PortInstance</a>.<span class="cons_Constructor"><span id="ExternalPort_6315_6327" title="Not referenced locally, nor via imports">ExternalPort</span></span> =                         <a href="#ID_6546_6548" id="ID_6354_6356" title="Defined at line 216, 217, 219, 220, 221, 222, 224">ID</a>

    <span class="layout">// === Workarounds =======</span>

    <a href="#OptionalComma_4692_4705" id="OptionalComma_6394_6407" title="Referenced at line 157, 160, 161">OptionalComma</a>.<span class="cons_Constructor"><span id="Comma_6408_6413" title="Not referenced locally, nor via imports">Comma</span></span> =                               [<span class="cons_String">,</span>]
    <a href="#OptionalComma_4692_4705" id="OptionalComma_6454_6467" title="Referenced at line 157, 160, 161">OptionalComma</a>.<span class="cons_Constructor"><span id="NoComma_6468_6475" title="Not referenced locally, nor via imports">NoComma</span></span> =                             []

<span class="keyword">lexical syntax</span>      <span class="layout">// keywords</span>
    <a href="#ID_1355_1357" id="ID_6546_6548" title="Referenced at line 66, 74, 84, 89, 94, 98, 101, 104, 117, 120, 121, 122, 123, 136, 152, 157, 160, 161, 163, 180, 192, 198, 207, 208">ID</a> = <span class="cons_Lit">"import"</span>       {<span class="keyword">reject</span>}
    <a href="#ID_1355_1357" id="ID_6579_6581" title="Referenced at line 66, 74, 84, 89, 94, 98, 101, 104, 117, 120, 121, 122, 123, 136, 152, 157, 160, 161, 163, 180, 192, 198, 207, 208">ID</a> = <span class="cons_Lit">"importlib"</span>    {<span class="keyword">reject</span>}

    <a href="#ID_1355_1357" id="ID_6613_6615" title="Referenced at line 66, 74, 84, 89, 94, 98, 101, 104, 117, 120, 121, 122, 123, 136, 152, 157, 160, 161, 163, 180, 192, 198, 207, 208">ID</a> = <span class="cons_Lit">"data"</span>         {<span class="keyword">reject</span>}
    <a href="#ID_1355_1357" id="ID_6646_6648" title="Referenced at line 66, 74, 84, 89, 94, 98, 101, 104, 117, 120, 121, 122, 123, 136, 152, 157, 160, 161, 163, 180, 192, 198, 207, 208">ID</a> = <span class="cons_Lit">"process"</span>      {<span class="keyword">reject</span>}
    <a href="#ID_1355_1357" id="ID_6679_6681" title="Referenced at line 66, 74, 84, 89, 94, 98, 101, 104, 117, 120, 121, 122, 123, 136, 152, 157, 160, 161, 163, 180, 192, 198, 207, 208">ID</a> = <span class="cons_Lit">"cluster"</span>      {<span class="keyword">reject</span>}
    <a href="#ID_1355_1357" id="ID_6712_6714" title="Referenced at line 66, 74, 84, 89, 94, 98, 101, 104, 117, 120, 121, 122, 123, 136, 152, 157, 160, 161, 163, 180, 192, 198, 207, 208">ID</a> = <span class="cons_Lit">"system"</span>       {<span class="keyword">reject</span>}

    <a href="#ID_1355_1357" id="ID_6746_6748" title="Referenced at line 66, 74, 84, 89, 94, 98, 101, 104, 117, 120, 121, 122, 123, 136, 152, 157, 160, 161, 163, 180, 192, 198, 207, 208">ID</a> = <span class="cons_Lit">"native"</span>       {<span class="keyword">reject</span>}

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