---
title: Stratego-Poosl.sdf3
hide:
  - toc
---

# `Stratego-Poosl.sdf3`

:simple-github: [pdmosses/metaborg-poosl/org.metaborg.lang.poosl/syntax/Stratego-Poosl.sdf3]

[pdmosses/metaborg-poosl/org.metaborg.lang.poosl/syntax/Stratego-Poosl.sdf3]: https://github.com/pdmosses/metaborg-poosl/blob/master/org.metaborg.lang.poosl/syntax/Stratego-Poosl.sdf3 "The source file on GitHub"

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
</pre></div></td>
<td class="code"><pre><code><span class="keyword">module</span> <span id="Stratego-Poosl_7_21" title="Not referenced locally, nor via imports">Stratego-Poosl</span>

<span class="keyword">imports</span>

    <span class="layout">// Meta language</span>
    <span title="External reference">StrategoLang/import-namespaced</span>
    <span title="External reference">StrategoLang/sugar/terms-namespaced</span>

    <span class="layout">// Object Language</span>
    <a href="../Poosl.sdf3#Poosl_7_12" id="Poosl_156_161" title="Defined at ../Poosl.sdf3 line 1">Poosl</a>
    <a href="../ExprStat.sdf3#ExprStat_7_15" id="ExprStat_166_174" title="Defined at ../ExprStat.sdf3 line 1">ExprStat</a>

<span class="keyword">context-free start-symbols</span>

    <a href="#Start_354_359" id="Start_208_213" title="Defined at line 19">Start</a>   <span class="layout">// Auxiliary start symbol is a workaround to avoid pretty-print error</span>

<span class="keyword">context-free syntax</span>     <span class="layout">// === Auxiliary start symbol =======</span>

    <a href="#Start_208_213" id="Start_354_359" title="Referenced at line 15">Start</a> = <span title="External reference">StrategoLang-Module</span> <span class="layout">// from StrategoLang/import-namespaced</span>

<span class="keyword">context-free syntax</span>     <span class="layout">// === Quotation =======</span>

    <span class="layout">// --- Poosl.sdf3 -------</span>
    <span id="StrategoLang-PreTerm_506_526" title="Not referenced locally, nor via imports">StrategoLang-PreTerm</span>.<span class="cons_Constructor"><span id="ToTerm_527_533" title="Not referenced locally, nor via imports">ToTerm</span></span> =                    <span class="cons_Lit">"|["</span> <a href="#Poosl_3298_3303" id="Poosl_560_565" title="Defined at line 66, 67">Poosl</a> <span class="cons_Lit">"]|"</span>
    <span id="StrategoLang-PreTerm_575_595" title="Not referenced locally, nor via imports">StrategoLang-PreTerm</span>.<span class="cons_Constructor"><span id="ToTerm_596_602" title="Not referenced locally, nor via imports">ToTerm</span></span> = <span class="cons_Lit">"poosl"</span>            <span class="cons_Lit">"|["</span> <a href="#Poosl_3298_3303" id="Poosl_629_634" title="Defined at line 66, 67">Poosl</a> <span class="cons_Lit">"]|"</span>
    <span id="StrategoLang-PreTerm_644_664" title="Not referenced locally, nor via imports">StrategoLang-PreTerm</span>.<span class="cons_Constructor"><span id="ToTerm_665_671" title="Not referenced locally, nor via imports">ToTerm</span></span> =                    <span class="cons_Lit">"|["</span> <a href="#Import_3463_3469" id="Import_698_704" title="Defined at line 69, 70">Import</a> <span class="cons_Lit">"]|"</span>
    <span id="StrategoLang-PreTerm_714_734" title="Not referenced locally, nor via imports">StrategoLang-PreTerm</span>.<span class="cons_Constructor"><span id="ToTerm_735_741" title="Not referenced locally, nor via imports">ToTerm</span></span> = <span class="cons_Lit">"import"</span>           <span class="cons_Lit">"|["</span> <a href="#Import_3463_3469" id="Import_768_774" title="Defined at line 69, 70">Import</a> <span class="cons_Lit">"]|"</span>
    <span id="StrategoLang-PreTerm_784_804" title="Not referenced locally, nor via imports">StrategoLang-PreTerm</span>.<span class="cons_Constructor"><span id="ToTerm_805_811" title="Not referenced locally, nor via imports">ToTerm</span></span> =                    <span class="cons_Lit">"|["</span> <a href="#Annotation_3792_3802" id="Annotation_838_848" title="Defined at line 74, 75">Annotation</a> <span class="cons_Lit">"]|"</span>
    <span id="StrategoLang-PreTerm_858_878" title="Not referenced locally, nor via imports">StrategoLang-PreTerm</span>.<span class="cons_Constructor"><span id="ToTerm_879_885" title="Not referenced locally, nor via imports">ToTerm</span></span> = <span class="cons_Lit">"annotation"</span>       <span class="cons_Lit">"|["</span> <a href="#Annotation_3792_3802" id="Annotation_912_922" title="Defined at line 74, 75">Annotation</a> <span class="cons_Lit">"]|"</span>
    <span id="StrategoLang-PreTerm_932_952" title="Not referenced locally, nor via imports">StrategoLang-PreTerm</span>.<span class="cons_Constructor"><span id="ToTerm_953_959" title="Not referenced locally, nor via imports">ToTerm</span></span> =                    <span class="cons_Lit">"|["</span> <a href="#Class_4121_4126" id="Class_986_991" title="Defined at line 79, 80">Class</a> <span class="cons_Lit">"]|"</span>
    <span id="StrategoLang-PreTerm_1001_1021" title="Not referenced locally, nor via imports">StrategoLang-PreTerm</span>.<span class="cons_Constructor"><span id="ToTerm_1022_1028" title="Not referenced locally, nor via imports">ToTerm</span></span> = <span class="cons_Lit">"class"</span>            <span class="cons_Lit">"|["</span> <a href="#Class_4121_4126" id="Class_1055_1060" title="Defined at line 79, 80">Class</a> <span class="cons_Lit">"]|"</span>
    <span id="StrategoLang-PreTerm_1070_1090" title="Not referenced locally, nor via imports">StrategoLang-PreTerm</span>.<span class="cons_Constructor"><span id="ToTerm_1091_1097" title="Not referenced locally, nor via imports">ToTerm</span></span> =                    <span class="cons_Lit">"|["</span> <a href="#DataMethod_4615_4625" id="DataMethod_1124_1134" title="Defined at line 87, 88">DataMethod</a> <span class="cons_Lit">"]|"</span>
    <span id="StrategoLang-PreTerm_1144_1164" title="Not referenced locally, nor via imports">StrategoLang-PreTerm</span>.<span class="cons_Constructor"><span id="ToTerm_1165_1171" title="Not referenced locally, nor via imports">ToTerm</span></span> = <span class="cons_Lit">"dataMethod"</span>       <span class="cons_Lit">"|["</span> <a href="#DataMethod_4615_4625" id="DataMethod_1198_1208" title="Defined at line 87, 88">DataMethod</a> <span class="cons_Lit">"]|"</span>
    <span id="StrategoLang-PreTerm_1218_1238" title="Not referenced locally, nor via imports">StrategoLang-PreTerm</span>.<span class="cons_Constructor"><span id="ToTerm_1239_1245" title="Not referenced locally, nor via imports">ToTerm</span></span> =                    <span class="cons_Lit">"|["</span> <a href="#ProcessMethod_4943_4956" id="ProcessMethod_1272_1285" title="Defined at line 91, 92">ProcessMethod</a> <span class="cons_Lit">"]|"</span>
    <span id="StrategoLang-PreTerm_1295_1315" title="Not referenced locally, nor via imports">StrategoLang-PreTerm</span>.<span class="cons_Constructor"><span id="ToTerm_1316_1322" title="Not referenced locally, nor via imports">ToTerm</span></span> = <span class="cons_Lit">"processMethod"</span>    <span class="cons_Lit">"|["</span> <a href="#ProcessMethod_4943_4956" id="ProcessMethod_1349_1362" title="Defined at line 91, 92">ProcessMethod</a> <span class="cons_Lit">"]|"</span>
    <span id="StrategoLang-PreTerm_1372_1392" title="Not referenced locally, nor via imports">StrategoLang-PreTerm</span>.<span class="cons_Constructor"><span id="ToTerm_1393_1399" title="Not referenced locally, nor via imports">ToTerm</span></span> =                    <span class="cons_Lit">"|["</span> <a href="#Port_7570_7574" id="Port_1426_1430" title="Defined at line 126, 127">Port</a> <span class="cons_Lit">"]|"</span>
    <span id="StrategoLang-PreTerm_1440_1460" title="Not referenced locally, nor via imports">StrategoLang-PreTerm</span>.<span class="cons_Constructor"><span id="ToTerm_1461_1467" title="Not referenced locally, nor via imports">ToTerm</span></span> = <span class="cons_Lit">"port"</span>             <span class="cons_Lit">"|["</span> <a href="#Port_7570_7574" id="Port_1494_1498" title="Defined at line 126, 127">Port</a> <span class="cons_Lit">"]|"</span>
    <span id="StrategoLang-PreTerm_1508_1528" title="Not referenced locally, nor via imports">StrategoLang-PreTerm</span>.<span class="cons_Constructor"><span id="ToTerm_1529_1535" title="Not referenced locally, nor via imports">ToTerm</span></span> =                    <span class="cons_Lit">"|["</span> <a href="#MessageSignature_7899_7915" id="MessageSignature_1562_1578" title="Defined at line 131, 132">MessageSignature</a> <span class="cons_Lit">"]|"</span>
    <span id="StrategoLang-PreTerm_1588_1608" title="Not referenced locally, nor via imports">StrategoLang-PreTerm</span>.<span class="cons_Constructor"><span id="ToTerm_1609_1615" title="Not referenced locally, nor via imports">ToTerm</span></span> = <span class="cons_Lit">"messageSignature"</span> <span class="cons_Lit">"|["</span> <a href="#MessageSignature_7899_7915" id="MessageSignature_1642_1658" title="Defined at line 131, 132">MessageSignature</a> <span class="cons_Lit">"]|"</span>
    <span id="StrategoLang-PreTerm_1668_1688" title="Not referenced locally, nor via imports">StrategoLang-PreTerm</span>.<span class="cons_Constructor"><span id="ToTerm_1689_1695" title="Not referenced locally, nor via imports">ToTerm</span></span> =                    <span class="cons_Lit">"|["</span> <a href="#Instance_8228_8236" id="Instance_1722_1730" title="Defined at line 136, 137">Instance</a> <span class="cons_Lit">"]|"</span>
    <span id="StrategoLang-PreTerm_1740_1760" title="Not referenced locally, nor via imports">StrategoLang-PreTerm</span>.<span class="cons_Constructor"><span id="ToTerm_1761_1767" title="Not referenced locally, nor via imports">ToTerm</span></span> = <span class="cons_Lit">"instance"</span>         <span class="cons_Lit">"|["</span> <a href="#Instance_8228_8236" id="Instance_1794_1802" title="Defined at line 136, 137">Instance</a> <span class="cons_Lit">"]|"</span>
    <span id="StrategoLang-PreTerm_1812_1832" title="Not referenced locally, nor via imports">StrategoLang-PreTerm</span>.<span class="cons_Constructor"><span id="ToTerm_1833_1839" title="Not referenced locally, nor via imports">ToTerm</span></span> =                    <span class="cons_Lit">"|["</span> <a href="#Channel_8557_8564" id="Channel_1866_1873" title="Defined at line 141, 142">Channel</a> <span class="cons_Lit">"]|"</span>
    <span id="StrategoLang-PreTerm_1883_1903" title="Not referenced locally, nor via imports">StrategoLang-PreTerm</span>.<span class="cons_Constructor"><span id="ToTerm_1904_1910" title="Not referenced locally, nor via imports">ToTerm</span></span> = <span class="cons_Lit">"channel"</span>          <span class="cons_Lit">"|["</span> <a href="#Channel_8557_8564" id="Channel_1937_1944" title="Defined at line 141, 142">Channel</a> <span class="cons_Lit">"]|"</span>
    <span id="StrategoLang-PreTerm_1954_1974" title="Not referenced locally, nor via imports">StrategoLang-PreTerm</span>.<span class="cons_Constructor"><span id="ToTerm_1975_1981" title="Not referenced locally, nor via imports">ToTerm</span></span> =                    <span class="cons_Lit">"|["</span> <a href="#PortInstance_9214_9226" id="PortInstance_2008_2020" title="Defined at line 150, 151">PortInstance</a> <span class="cons_Lit">"]|"</span>
    <span id="StrategoLang-PreTerm_2030_2050" title="Not referenced locally, nor via imports">StrategoLang-PreTerm</span>.<span class="cons_Constructor"><span id="ToTerm_2051_2057" title="Not referenced locally, nor via imports">ToTerm</span></span> = <span class="cons_Lit">"portInstance"</span>     <span class="cons_Lit">"|["</span> <a href="#PortInstance_9214_9226" id="PortInstance_2084_2096" title="Defined at line 150, 151">PortInstance</a> <span class="cons_Lit">"]|"</span>
    <span id="StrategoLang-PreTerm_2106_2126" title="Not referenced locally, nor via imports">StrategoLang-PreTerm</span>.<span class="cons_Constructor"><span id="ToTerm_2127_2133" title="Not referenced locally, nor via imports">ToTerm</span></span> =                    <span class="cons_Lit">"|["</span> <a href="#Declaration_6421_6432" id="Declaration_2160_2171" title="Defined at line 111, 112">Declaration</a> <span class="cons_Lit">"]|"</span>
    <span id="StrategoLang-PreTerm_2181_2201" title="Not referenced locally, nor via imports">StrategoLang-PreTerm</span>.<span class="cons_Constructor"><span id="ToTerm_2202_2208" title="Not referenced locally, nor via imports">ToTerm</span></span> = <span class="cons_Lit">"declaration"</span>      <span class="cons_Lit">"|["</span> <a href="#Declaration_6421_6432" id="Declaration_2235_2246" title="Defined at line 111, 112">Declaration</a> <span class="cons_Lit">"]|"</span>

    <span class="layout">// --- ExprStat.sdf3 -------</span>
    <span id="StrategoLang-PreTerm_2290_2310" title="Not referenced locally, nor via imports">StrategoLang-PreTerm</span>.<span class="cons_Constructor"><span id="ToTerm_2311_2317" title="Not referenced locally, nor via imports">ToTerm</span></span> =                    <span class="cons_Lit">"|["</span> <a href="#Statement_9412_9421" id="Statement_2344_2353" title="Defined at line 154, 155">Statement</a> <span class="cons_Lit">"]|"</span>
    <span id="StrategoLang-PreTerm_2363_2383" title="Not referenced locally, nor via imports">StrategoLang-PreTerm</span>.<span class="cons_Constructor"><span id="ToTerm_2384_2390" title="Not referenced locally, nor via imports">ToTerm</span></span> = <span class="cons_Lit">"statements"</span>       <span class="cons_Lit">"|["</span> <a href="#Statement_9412_9421" id="Statement_2417_2426" title="Defined at line 154, 155">Statement</a> <span class="cons_Lit">"]|"</span>
    <span id="StrategoLang-PreTerm_2436_2456" title="Not referenced locally, nor via imports">StrategoLang-PreTerm</span>.<span class="cons_Constructor"><span id="ToTerm_2457_2463" title="Not referenced locally, nor via imports">ToTerm</span></span> =                    <span class="cons_Lit">"|["</span> <a href="#SingleStatement_9576_9591" id="SingleStatement_2490_2505" title="Defined at line 156, 157">SingleStatement</a> <span class="cons_Lit">"]|"</span>
    <span id="StrategoLang-PreTerm_2515_2535" title="Not referenced locally, nor via imports">StrategoLang-PreTerm</span>.<span class="cons_Constructor"><span id="ToTerm_2536_2542" title="Not referenced locally, nor via imports">ToTerm</span></span> = <span class="cons_Lit">"statement"</span>        <span class="cons_Lit">"|["</span> <a href="#SingleStatement_9576_9591" id="SingleStatement_2569_2584" title="Defined at line 156, 157">SingleStatement</a> <span class="cons_Lit">"]|"</span>
    <span id="StrategoLang-PreTerm_2594_2614" title="Not referenced locally, nor via imports">StrategoLang-PreTerm</span>.<span class="cons_Constructor"><span id="ToTerm_2615_2621" title="Not referenced locally, nor via imports">ToTerm</span></span> =                    <span class="cons_Lit">"|["</span> <a href="#CaseStatement_9740_9753" id="CaseStatement_2648_2661" title="Defined at line 158, 159">CaseStatement</a> <span class="cons_Lit">"]|"</span>
    <span id="StrategoLang-PreTerm_2671_2691" title="Not referenced locally, nor via imports">StrategoLang-PreTerm</span>.<span class="cons_Constructor"><span id="ToTerm_2692_2698" title="Not referenced locally, nor via imports">ToTerm</span></span> = <span class="cons_Lit">"caseStatement"</span>    <span class="cons_Lit">"|["</span> <a href="#CaseStatement_9740_9753" id="CaseStatement_2725_2738" title="Defined at line 158, 159">CaseStatement</a> <span class="cons_Lit">"]|"</span>
    <span id="StrategoLang-PreTerm_2748_2768" title="Not referenced locally, nor via imports">StrategoLang-PreTerm</span>.<span class="cons_Constructor"><span id="ToTerm_2769_2775" title="Not referenced locally, nor via imports">ToTerm</span></span> =                    <span class="cons_Lit">"|["</span> <a href="#Expression_10068_10078" id="Expression_2802_2812" title="Defined at line 162, 163">Expression</a> <span class="cons_Lit">"]|"</span>
    <span id="StrategoLang-PreTerm_2822_2842" title="Not referenced locally, nor via imports">StrategoLang-PreTerm</span>.<span class="cons_Constructor"><span id="ToTerm_2843_2849" title="Not referenced locally, nor via imports">ToTerm</span></span> = <span class="cons_Lit">"expressions"</span>      <span class="cons_Lit">"|["</span> <a href="#Expression_10068_10078" id="Expression_2876_2886" title="Defined at line 162, 163">Expression</a> <span class="cons_Lit">"]|"</span>
    <span id="StrategoLang-PreTerm_2896_2916" title="Not referenced locally, nor via imports">StrategoLang-PreTerm</span>.<span class="cons_Constructor"><span id="ToTerm_2917_2923" title="Not referenced locally, nor via imports">ToTerm</span></span> =                    <span class="cons_Lit">"|["</span> <a href="#SingleExpression_10232_10248" id="SingleExpression_2950_2966" title="Defined at line 164, 165">SingleExpression</a> <span class="cons_Lit">"]|"</span>
    <span id="StrategoLang-PreTerm_2976_2996" title="Not referenced locally, nor via imports">StrategoLang-PreTerm</span>.<span class="cons_Constructor"><span id="ToTerm_2997_3003" title="Not referenced locally, nor via imports">ToTerm</span></span> = <span class="cons_Lit">"expression"</span>       <span class="cons_Lit">"|["</span> <a href="#SingleExpression_10232_10248" id="SingleExpression_3030_3046" title="Defined at line 164, 165">SingleExpression</a> <span class="cons_Lit">"]|"</span>
    <span id="StrategoLang-PreTerm_3056_3076" title="Not referenced locally, nor via imports">StrategoLang-PreTerm</span>.<span class="cons_Constructor"><span id="ToTerm_3077_3083" title="Not referenced locally, nor via imports">ToTerm</span></span> =                    <span class="cons_Lit">"|["</span> <a href="#CaseExpression_10396_10410" id="CaseExpression_3110_3124" title="Defined at line 166, 167">CaseExpression</a> <span class="cons_Lit">"]|"</span>
    <span id="StrategoLang-PreTerm_3134_3154" title="Not referenced locally, nor via imports">StrategoLang-PreTerm</span>.<span class="cons_Constructor"><span id="ToTerm_3155_3161" title="Not referenced locally, nor via imports">ToTerm</span></span> = <span class="cons_Lit">"caseExpression"</span>   <span class="cons_Lit">"|["</span> <a href="#CaseExpression_10396_10410" id="CaseExpression_3188_3202" title="Defined at line 166, 167">CaseExpression</a> <span class="cons_Lit">"]|"</span>

<span class="keyword">context-free syntax</span>     <span class="layout">// === Anti-quotation =======</span>

    <span class="layout">// --- Poosl.sdf3 -------</span>
    <a href="#Poosl_629_634" id="Poosl_3298_3303" title="Referenced at line 25">Poosl</a>                   .<span class="cons_Constructor"><span id="FromTerm_3323_3331" title="Not referenced locally, nor via imports">FromTerm</span></span> = <span class="cons_Lit">"~"</span>                     <span title="External reference">StrategoLang-Term</span>
    <a href="#Poosl_629_634" id="Poosl_3380_3385" title="Referenced at line 25">Poosl</a>                   .<span class="cons_Constructor"><span id="FromTerm_3405_3413" title="Not referenced locally, nor via imports">FromTerm</span></span> = <span class="cons_Lit">"~poosl:"</span>               <span title="External reference">StrategoLang-Term</span>

    <a href="#Import_768_774" id="Import_3463_3469" title="Referenced at line 27">Import</a>                  .<span class="cons_Constructor"><span id="FromTerm_3488_3496" title="Not referenced locally, nor via imports">FromTerm</span></span> = <span class="cons_Lit">"~"</span>                     <span title="External reference">StrategoLang-Term</span>
    <a href="#Import_768_774" id="Import_3545_3551" title="Referenced at line 27">Import</a>                  .<span class="cons_Constructor"><span id="FromTerm_3570_3578" title="Not referenced locally, nor via imports">FromTerm</span></span> = <span class="cons_Lit">"~import:"</span>              <span title="External reference">StrategoLang-Term</span>
    <span id="ImportList_3627_3637" title="Not referenced locally, nor via imports">ImportList</span>              .<span class="cons_Constructor"><span id="FromTerm_3652_3660" title="Not referenced locally, nor via imports">FromTerm</span></span> = <span class="cons_Lit">"~*"</span>                    <span title="External reference">StrategoLang-Term</span>
    <span id="ImportList_3709_3719" title="Not referenced locally, nor via imports">ImportList</span>              .<span class="cons_Constructor"><span id="FromTerm_3734_3742" title="Not referenced locally, nor via imports">FromTerm</span></span> = <span class="cons_Lit">"~*imports:"</span>            <span title="External reference">StrategoLang-Term</span>

    <a href="#Annotation_912_922" id="Annotation_3792_3802" title="Referenced at line 29">Annotation</a>              .<span class="cons_Constructor"><span id="FromTerm_3817_3825" title="Not referenced locally, nor via imports">FromTerm</span></span> = <span class="cons_Lit">"~"</span>                     <span title="External reference">StrategoLang-Term</span>
    <a href="#Annotation_912_922" id="Annotation_3874_3884" title="Referenced at line 29">Annotation</a>              .<span class="cons_Constructor"><span id="FromTerm_3899_3907" title="Not referenced locally, nor via imports">FromTerm</span></span> = <span class="cons_Lit">"~annotation:"</span>          <span title="External reference">StrategoLang-Term</span>
    <span id="AnnotationList_3956_3970" title="Not referenced locally, nor via imports">AnnotationList</span>          .<span class="cons_Constructor"><span id="FromTerm_3981_3989" title="Not referenced locally, nor via imports">FromTerm</span></span> = <span class="cons_Lit">"~*"</span>                    <span title="External reference">StrategoLang-Term</span>
    <span id="AnnotationList_4038_4052" title="Not referenced locally, nor via imports">AnnotationList</span>          .<span class="cons_Constructor"><span id="FromTerm_4063_4071" title="Not referenced locally, nor via imports">FromTerm</span></span> = <span class="cons_Lit">"~*annotations:"</span>        <span title="External reference">StrategoLang-Term</span>

    <a href="#Class_1055_1060" id="Class_4121_4126" title="Referenced at line 31">Class</a>                   .<span class="cons_Constructor"><span id="FromTerm_4146_4154" title="Not referenced locally, nor via imports">FromTerm</span></span> = <span class="cons_Lit">"~"</span>                     <span title="External reference">StrategoLang-Term</span>
    <a href="#Class_1055_1060" id="Class_4203_4208" title="Referenced at line 31">Class</a>                   .<span class="cons_Constructor"><span id="FromTerm_4228_4236" title="Not referenced locally, nor via imports">FromTerm</span></span> = <span class="cons_Lit">"~class:"</span>               <span title="External reference">StrategoLang-Term</span>
    <span id="ClassList_4285_4294" title="Not referenced locally, nor via imports">ClassList</span>               .<span class="cons_Constructor"><span id="FromTerm_4310_4318" title="Not referenced locally, nor via imports">FromTerm</span></span> = <span class="cons_Lit">"~*"</span>                    <span title="External reference">StrategoLang-Term</span>
    <span id="ClassList_4367_4376" title="Not referenced locally, nor via imports">ClassList</span>               .<span class="cons_Constructor"><span id="FromTerm_4392_4400" title="Not referenced locally, nor via imports">FromTerm</span></span> = <span class="cons_Lit">"~*classes:"</span>            <span title="External reference">StrategoLang-Term</span>

    <span id="ExtendsClause_4450_4463" title="Not referenced locally, nor via imports">ExtendsClause</span>           .<span class="cons_Constructor"><span id="FromTerm_4475_4483" title="Not referenced locally, nor via imports">FromTerm</span></span> = <span class="cons_Lit">"~"</span>                     <span title="External reference">StrategoLang-Term</span>
    <span id="ExtendsClause_4532_4545" title="Not referenced locally, nor via imports">ExtendsClause</span>           .<span class="cons_Constructor"><span id="FromTerm_4557_4565" title="Not referenced locally, nor via imports">FromTerm</span></span> = <span class="cons_Lit">"~extends:"</span>             <span title="External reference">StrategoLang-Term</span>

    <a href="#DataMethod_1198_1208" id="DataMethod_4615_4625" title="Referenced at line 33">DataMethod</a>              .<span class="cons_Constructor"><span id="FromTerm_4640_4648" title="Not referenced locally, nor via imports">FromTerm</span></span> = <span class="cons_Lit">"~"</span>                     <span title="External reference">StrategoLang-Term</span>
    <a href="#DataMethod_1198_1208" id="DataMethod_4697_4707" title="Referenced at line 33">DataMethod</a>              .<span class="cons_Constructor"><span id="FromTerm_4722_4730" title="Not referenced locally, nor via imports">FromTerm</span></span> = <span class="cons_Lit">"~method:"</span>              <span title="External reference">StrategoLang-Term</span>
    <span id="DataMethodList_4779_4793" title="Not referenced locally, nor via imports">DataMethodList</span>          .<span class="cons_Constructor"><span id="FromTerm_4804_4812" title="Not referenced locally, nor via imports">FromTerm</span></span> = <span class="cons_Lit">"~"</span>                     <span title="External reference">StrategoLang-Term</span>
    <span id="DataMethodList_4861_4875" title="Not referenced locally, nor via imports">DataMethodList</span>          .<span class="cons_Constructor"><span id="FromTerm_4886_4894" title="Not referenced locally, nor via imports">FromTerm</span></span> = <span class="cons_Lit">"~*methods:"</span>            <span title="External reference">StrategoLang-Term</span>
    <a href="#ProcessMethod_1349_1362" id="ProcessMethod_4943_4956" title="Referenced at line 35">ProcessMethod</a>           .<span class="cons_Constructor"><span id="FromTerm_4968_4976" title="Not referenced locally, nor via imports">FromTerm</span></span> = <span class="cons_Lit">"~"</span>                     <span title="External reference">StrategoLang-Term</span>
    <a href="#ProcessMethod_1349_1362" id="ProcessMethod_5025_5038" title="Referenced at line 35">ProcessMethod</a>           .<span class="cons_Constructor"><span id="FromTerm_5050_5058" title="Not referenced locally, nor via imports">FromTerm</span></span> = <span class="cons_Lit">"~method:"</span>              <span title="External reference">StrategoLang-Term</span>
    <span id="ProcessMethodList_5107_5124" title="Not referenced locally, nor via imports">ProcessMethodList</span>       .<span class="cons_Constructor"><span id="FromTerm_5132_5140" title="Not referenced locally, nor via imports">FromTerm</span></span> = <span class="cons_Lit">"~"</span>                     <span title="External reference">StrategoLang-Term</span>
    <span id="ProcessMethodList_5189_5206" title="Not referenced locally, nor via imports">ProcessMethodList</span>       .<span class="cons_Constructor"><span id="FromTerm_5214_5222" title="Not referenced locally, nor via imports">FromTerm</span></span> = <span class="cons_Lit">"~*methods:"</span>            <span title="External reference">StrategoLang-Term</span>

    <span id="ID_5272_5274" title="Not referenced locally, nor via imports">ID</span>                      .<span class="cons_Constructor"><span id="FromTerm_5297_5305" title="Not referenced locally, nor via imports">FromTerm</span></span> = <span class="cons_Lit">"~"</span>                     <span title="External reference">StrategoLang-Term</span>
    <span id="ID_5354_5356" title="Not referenced locally, nor via imports">ID</span>                      .<span class="cons_Constructor"><span id="FromTerm_5379_5387" title="Not referenced locally, nor via imports">FromTerm</span></span> = <span class="cons_Lit">"~id:"</span>                  <span title="External reference">StrategoLang-Term</span>
    <span id="IDList_5436_5442" title="Not referenced locally, nor via imports">IDList</span>                  .<span class="cons_Constructor"><span id="FromTerm_5461_5469" title="Not referenced locally, nor via imports">FromTerm</span></span> = <span class="cons_Lit">"~*"</span>                    <span title="External reference">StrategoLang-Term</span>
    <span id="IDList_5518_5524" title="Not referenced locally, nor via imports">IDList</span>                  .<span class="cons_Constructor"><span id="FromTerm_5543_5551" title="Not referenced locally, nor via imports">FromTerm</span></span> = <span class="cons_Lit">"~*ids:"</span>                <span title="External reference">StrategoLang-Term</span>
    <span id="OptMessageParameterList_5600_5623" title="Not referenced locally, nor via imports">OptMessageParameterList</span> .<span class="cons_Constructor"><span id="FromTerm_5625_5633" title="Not referenced locally, nor via imports">FromTerm</span></span> = <span class="cons_Lit">"~*"</span>                    <span title="External reference">StrategoLang-Term</span>
    <span id="OptMessageParameterList_5682_5705" title="Not referenced locally, nor via imports">OptMessageParameterList</span> .<span class="cons_Constructor"><span id="FromTerm_5707_5715" title="Not referenced locally, nor via imports">FromTerm</span></span> = <span class="cons_Lit">"~*ids:"</span>                <span title="External reference">StrategoLang-Term</span>
    <span id="OptVariableList_5764_5779" title="Not referenced locally, nor via imports">OptVariableList</span>         .<span class="cons_Constructor"><span id="FromTerm_5789_5797" title="Not referenced locally, nor via imports">FromTerm</span></span> = <span class="cons_Lit">"~*"</span>                    <span title="External reference">StrategoLang-Term</span>
    <span id="OptVariableList_5846_5861" title="Not referenced locally, nor via imports">OptVariableList</span>         .<span class="cons_Constructor"><span id="FromTerm_5871_5879" title="Not referenced locally, nor via imports">FromTerm</span></span> = <span class="cons_Lit">"~*ids:"</span>                <span title="External reference">StrategoLang-Term</span>
    <span id="VariableList_5928_5940" title="Not referenced locally, nor via imports">VariableList</span>            .<span class="cons_Constructor"><span id="FromTerm_5953_5961" title="Not referenced locally, nor via imports">FromTerm</span></span> = <span class="cons_Lit">"~*"</span>                    <span title="External reference">StrategoLang-Term</span>
    <span id="VariableList_6010_6022" title="Not referenced locally, nor via imports">VariableList</span>            .<span class="cons_Constructor"><span id="FromTerm_6035_6043" title="Not referenced locally, nor via imports">FromTerm</span></span> = <span class="cons_Lit">"~*ids:"</span>                <span title="External reference">StrategoLang-Term</span>
    <span id="UnaryOperator_6092_6105" title="Not referenced locally, nor via imports">UnaryOperator</span>           .<span class="cons_Constructor"><span id="FromTerm_6117_6125" title="Not referenced locally, nor via imports">FromTerm</span></span> = <span class="cons_Lit">"~"</span>                     <span title="External reference">StrategoLang-Term</span>
    <span id="UnaryOperator_6174_6187" title="Not referenced locally, nor via imports">UnaryOperator</span>           .<span class="cons_Constructor"><span id="FromTerm_6199_6207" title="Not referenced locally, nor via imports">FromTerm</span></span> = <span class="cons_Lit">"~unOp:"</span>                <span title="External reference">StrategoLang-Term</span>
    <span id="OperatorBinary_6256_6270" title="Not referenced locally, nor via imports">OperatorBinary</span>          .<span class="cons_Constructor"><span id="FromTerm_6281_6289" title="Not referenced locally, nor via imports">FromTerm</span></span> = <span class="cons_Lit">"~"</span>                     <span title="External reference">StrategoLang-Term</span>
    <span id="OperatorBinary_6338_6352" title="Not referenced locally, nor via imports">OperatorBinary</span>          .<span class="cons_Constructor"><span id="FromTerm_6363_6371" title="Not referenced locally, nor via imports">FromTerm</span></span> = <span class="cons_Lit">"~binOp:"</span>               <span title="External reference">StrategoLang-Term</span>

    <a href="#Declaration_2235_2246" id="Declaration_6421_6432" title="Referenced at line 47">Declaration</a>             .<span class="cons_Constructor"><span id="FromTerm_6446_6454" title="Not referenced locally, nor via imports">FromTerm</span></span> = <span class="cons_Lit">"~"</span>                     <span title="External reference">StrategoLang-Term</span>
    <a href="#Declaration_2235_2246" id="Declaration_6503_6514" title="Referenced at line 47">Declaration</a>             .<span class="cons_Constructor"><span id="FromTerm_6528_6536" title="Not referenced locally, nor via imports">FromTerm</span></span> = <span class="cons_Lit">"~declaration:"</span>         <span title="External reference">StrategoLang-Term</span>
    <span id="DeclarationOptComma_6585_6604" title="Not referenced locally, nor via imports">DeclarationOptComma</span>     .<span class="cons_Constructor"><span id="FromTerm_6610_6618" title="Not referenced locally, nor via imports">FromTerm</span></span> = <span class="cons_Lit">"~"</span>                     <span title="External reference">StrategoLang-Term</span>
    <span id="DeclarationOptComma_6667_6686" title="Not referenced locally, nor via imports">DeclarationOptComma</span>     .<span class="cons_Constructor"><span id="FromTerm_6692_6700" title="Not referenced locally, nor via imports">FromTerm</span></span> = <span class="cons_Lit">"~declaration:"</span>         <span title="External reference">StrategoLang-Term</span>
    <span id="DeclarationOptCommaList_6749_6772" title="Not referenced locally, nor via imports">DeclarationOptCommaList</span> .<span class="cons_Constructor"><span id="FromTerm_6774_6782" title="Not referenced locally, nor via imports">FromTerm</span></span> = <span class="cons_Lit">"~*"</span>                    <span title="External reference">StrategoLang-Term</span>
    <span id="DeclarationOptCommaList_6831_6854" title="Not referenced locally, nor via imports">DeclarationOptCommaList</span> .<span class="cons_Constructor"><span id="FromTerm_6856_6864" title="Not referenced locally, nor via imports">FromTerm</span></span> = <span class="cons_Lit">"~*declarations:"</span>       <span title="External reference">StrategoLang-Term</span>
    <span id="ParameterList_6913_6926" title="Not referenced locally, nor via imports">ParameterList</span>           .<span class="cons_Constructor"><span id="FromTerm_6938_6946" title="Not referenced locally, nor via imports">FromTerm</span></span> = <span class="cons_Lit">"~*"</span>                    <span title="External reference">StrategoLang-Term</span>
    <span id="ParameterList_6995_7008" title="Not referenced locally, nor via imports">ParameterList</span>           .<span class="cons_Constructor"><span id="FromTerm_7020_7028" title="Not referenced locally, nor via imports">FromTerm</span></span> = <span class="cons_Lit">"~*declarations:"</span>       <span title="External reference">StrategoLang-Term</span>
    <span id="OptParameterList_7077_7093" title="Not referenced locally, nor via imports">OptParameterList</span>        .<span class="cons_Constructor"><span id="FromTerm_7102_7110" title="Not referenced locally, nor via imports">FromTerm</span></span> = <span class="cons_Lit">"~*"</span>                    <span title="External reference">StrategoLang-Term</span>
    <span id="OptParameterList_7159_7175" title="Not referenced locally, nor via imports">OptParameterList</span>        .<span class="cons_Constructor"><span id="FromTerm_7184_7192" title="Not referenced locally, nor via imports">FromTerm</span></span> = <span class="cons_Lit">"~*declarations:"</span>       <span title="External reference">StrategoLang-Term</span>
    <span id="OptLocalVariableList_7241_7261" title="Not referenced locally, nor via imports">OptLocalVariableList</span>    .<span class="cons_Constructor"><span id="FromTerm_7266_7274" title="Not referenced locally, nor via imports">FromTerm</span></span> = <span class="cons_Lit">"~*"</span>                    <span title="External reference">StrategoLang-Term</span>
    <span id="OptLocalVariableList_7323_7343" title="Not referenced locally, nor via imports">OptLocalVariableList</span>    .<span class="cons_Constructor"><span id="FromTerm_7348_7356" title="Not referenced locally, nor via imports">FromTerm</span></span> = <span class="cons_Lit">"~*declarations:"</span>       <span title="External reference">StrategoLang-Term</span>
    <span id="OptEmptyList_7405_7417" title="Not referenced locally, nor via imports">OptEmptyList</span>            .<span class="cons_Constructor"><span id="FromTerm_7430_7438" title="Not referenced locally, nor via imports">FromTerm</span></span> = <span class="cons_Lit">"~*"</span>                    <span title="External reference">StrategoLang-Term</span>
    <span id="OptEmptyList_7487_7499" title="Not referenced locally, nor via imports">OptEmptyList</span>            .<span class="cons_Constructor"><span id="FromTerm_7512_7520" title="Not referenced locally, nor via imports">FromTerm</span></span> = <span class="cons_Lit">"~*declarations:"</span>       <span title="External reference">StrategoLang-Term</span>

    <a href="#Port_1494_1498" id="Port_7570_7574" title="Referenced at line 37">Port</a>                    .<span class="cons_Constructor"><span id="FromTerm_7595_7603" title="Not referenced locally, nor via imports">FromTerm</span></span> = <span class="cons_Lit">"~"</span>                     <span title="External reference">StrategoLang-Term</span>
    <a href="#Port_1494_1498" id="Port_7652_7656" title="Referenced at line 37">Port</a>                    .<span class="cons_Constructor"><span id="FromTerm_7677_7685" title="Not referenced locally, nor via imports">FromTerm</span></span> = <span class="cons_Lit">"~port:"</span>                <span title="External reference">StrategoLang-Term</span>
    <span id="PortList_7734_7742" title="Not referenced locally, nor via imports">PortList</span>                .<span class="cons_Constructor"><span id="FromTerm_7759_7767" title="Not referenced locally, nor via imports">FromTerm</span></span> = <span class="cons_Lit">"~*"</span>                    <span title="External reference">StrategoLang-Term</span>
    <span id="PortList_7816_7824" title="Not referenced locally, nor via imports">PortList</span>                .<span class="cons_Constructor"><span id="FromTerm_7841_7849" title="Not referenced locally, nor via imports">FromTerm</span></span> = <span class="cons_Lit">"~*ports:"</span>              <span title="External reference">StrategoLang-Term</span>

    <a href="#MessageSignature_1642_1658" id="MessageSignature_7899_7915" title="Referenced at line 39">MessageSignature</a>        .<span class="cons_Constructor"><span id="FromTerm_7924_7932" title="Not referenced locally, nor via imports">FromTerm</span></span> = <span class="cons_Lit">"~"</span>                     <span title="External reference">StrategoLang-Term</span>
    <a href="#MessageSignature_1642_1658" id="MessageSignature_7981_7997" title="Referenced at line 39">MessageSignature</a>        .<span class="cons_Constructor"><span id="FromTerm_8006_8014" title="Not referenced locally, nor via imports">FromTerm</span></span> = <span class="cons_Lit">"~message:"</span>             <span title="External reference">StrategoLang-Term</span>
    <span id="MessageSignatureList_8063_8083" title="Not referenced locally, nor via imports">MessageSignatureList</span>    .<span class="cons_Constructor"><span id="FromTerm_8088_8096" title="Not referenced locally, nor via imports">FromTerm</span></span> = <span class="cons_Lit">"~*"</span>                    <span title="External reference">StrategoLang-Term</span>
    <span id="MessageSignatureList_8145_8165" title="Not referenced locally, nor via imports">MessageSignatureList</span>    .<span class="cons_Constructor"><span id="FromTerm_8170_8178" title="Not referenced locally, nor via imports">FromTerm</span></span> = <span class="cons_Lit">"~*messages:"</span>           <span title="External reference">StrategoLang-Term</span>

    <a href="#Instance_1794_1802" id="Instance_8228_8236" title="Referenced at line 41">Instance</a>                .<span class="cons_Constructor"><span id="FromTerm_8253_8261" title="Not referenced locally, nor via imports">FromTerm</span></span> = <span class="cons_Lit">"~"</span>                     <span title="External reference">StrategoLang-Term</span>
    <a href="#Instance_1794_1802" id="Instance_8310_8318" title="Referenced at line 41">Instance</a>                .<span class="cons_Constructor"><span id="FromTerm_8335_8343" title="Not referenced locally, nor via imports">FromTerm</span></span> = <span class="cons_Lit">"~instance:"</span>            <span title="External reference">StrategoLang-Term</span>
    <span id="InstanceList_8392_8404" title="Not referenced locally, nor via imports">InstanceList</span>            .<span class="cons_Constructor"><span id="FromTerm_8417_8425" title="Not referenced locally, nor via imports">FromTerm</span></span> = <span class="cons_Lit">"~*"</span>                    <span title="External reference">StrategoLang-Term</span>
    <span id="InstanceList_8474_8486" title="Not referenced locally, nor via imports">InstanceList</span>            .<span class="cons_Constructor"><span id="FromTerm_8499_8507" title="Not referenced locally, nor via imports">FromTerm</span></span> = <span class="cons_Lit">"~*instances:"</span>          <span title="External reference">StrategoLang-Term</span>

    <a href="#Channel_1937_1944" id="Channel_8557_8564" title="Referenced at line 43">Channel</a>                 .<span class="cons_Constructor"><span id="FromTerm_8582_8590" title="Not referenced locally, nor via imports">FromTerm</span></span> = <span class="cons_Lit">"~"</span>                     <span title="External reference">StrategoLang-Term</span>
    <a href="#Channel_1937_1944" id="Channel_8639_8646" title="Referenced at line 43">Channel</a>                 .<span class="cons_Constructor"><span id="FromTerm_8664_8672" title="Not referenced locally, nor via imports">FromTerm</span></span> = <span class="cons_Lit">"~channel:"</span>             <span title="External reference">StrategoLang-Term</span>
    <span id="ChannelList_8721_8732" title="Not referenced locally, nor via imports">ChannelList</span>             .<span class="cons_Constructor"><span id="FromTerm_8746_8754" title="Not referenced locally, nor via imports">FromTerm</span></span> = <span class="cons_Lit">"~*"</span>                    <span title="External reference">StrategoLang-Term</span>
    <span id="ChannelList_8803_8814" title="Not referenced locally, nor via imports">ChannelList</span>             .<span class="cons_Constructor"><span id="FromTerm_8828_8836" title="Not referenced locally, nor via imports">FromTerm</span></span> = <span class="cons_Lit">"~*channels:"</span>           <span title="External reference">StrategoLang-Term</span>

    <span id="InstanceParameter_8886_8903" title="Not referenced locally, nor via imports">InstanceParameter</span>       .<span class="cons_Constructor"><span id="FromTerm_8911_8919" title="Not referenced locally, nor via imports">FromTerm</span></span> = <span class="cons_Lit">"~"</span>                     <span title="External reference">StrategoLang-Term</span>
    <span id="InstanceParameter_8968_8985" title="Not referenced locally, nor via imports">InstanceParameter</span>       .<span class="cons_Constructor"><span id="FromTerm_8993_9001" title="Not referenced locally, nor via imports">FromTerm</span></span> = <span class="cons_Lit">"~instanceParameter:"</span>   <span title="External reference">StrategoLang-Term</span>
    <span id="OptInstanceParameterList_9050_9074" title="Not referenced locally, nor via imports">OptInstanceParameterList</span>.<span class="cons_Constructor"><span id="FromTerm_9075_9083" title="Not referenced locally, nor via imports">FromTerm</span></span> = <span class="cons_Lit">"~*"</span>                    <span title="External reference">StrategoLang-Term</span>
    <span id="OptInstanceParameterList_9132_9156" title="Not referenced locally, nor via imports">OptInstanceParameterList</span>.<span class="cons_Constructor"><span id="FromTerm_9157_9165" title="Not referenced locally, nor via imports">FromTerm</span></span> = <span class="cons_Lit">"~*instanceParameters:"</span> <span title="External reference">StrategoLang-Term</span>
    <a href="#PortInstance_2084_2096" id="PortInstance_9214_9226" title="Referenced at line 45">PortInstance</a>            .<span class="cons_Constructor"><span id="FromTerm_9239_9247" title="Not referenced locally, nor via imports">FromTerm</span></span> = <span class="cons_Lit">"~"</span>                     <span title="External reference">StrategoLang-Term</span>
    <a href="#PortInstance_2084_2096" id="PortInstance_9296_9308" title="Referenced at line 45">PortInstance</a>            .<span class="cons_Constructor"><span id="FromTerm_9321_9329" title="Not referenced locally, nor via imports">FromTerm</span></span> = <span class="cons_Lit">"~portInstance:"</span>        <span title="External reference">StrategoLang-Term</span>

    <span class="layout">// --- ExprStat.sdf3 -------</span>
    <a href="#Statement_2417_2426" id="Statement_9412_9421" title="Referenced at line 51">Statement</a>               .<span class="cons_Constructor"><span id="FromTerm_9437_9445" title="Not referenced locally, nor via imports">FromTerm</span></span> = <span class="cons_Lit">"~*"</span>                    <span title="External reference">StrategoLang-Term</span>
    <a href="#Statement_2417_2426" id="Statement_9494_9503" title="Referenced at line 51">Statement</a>               .<span class="cons_Constructor"><span id="FromTerm_9519_9527" title="Not referenced locally, nor via imports">FromTerm</span></span> = <span class="cons_Lit">"~*statements:"</span>         <span title="External reference">StrategoLang-Term</span>
    <a href="#SingleStatement_2569_2584" id="SingleStatement_9576_9591" title="Referenced at line 53">SingleStatement</a>         .<span class="cons_Constructor"><span id="FromTerm_9601_9609" title="Not referenced locally, nor via imports">FromTerm</span></span> = <span class="cons_Lit">"~"</span>                     <span title="External reference">StrategoLang-Term</span>
    <a href="#SingleStatement_2569_2584" id="SingleStatement_9658_9673" title="Referenced at line 53">SingleStatement</a>         .<span class="cons_Constructor"><span id="FromTerm_9683_9691" title="Not referenced locally, nor via imports">FromTerm</span></span> = <span class="cons_Lit">"~statement:"</span>           <span title="External reference">StrategoLang-Term</span>
    <a href="#CaseStatement_2725_2738" id="CaseStatement_9740_9753" title="Referenced at line 55">CaseStatement</a>           .<span class="cons_Constructor"><span id="FromTerm_9765_9773" title="Not referenced locally, nor via imports">FromTerm</span></span> = <span class="cons_Lit">"~"</span>                     <span title="External reference">StrategoLang-Term</span>
    <a href="#CaseStatement_2725_2738" id="CaseStatement_9822_9835" title="Referenced at line 55">CaseStatement</a>           .<span class="cons_Constructor"><span id="FromTerm_9847_9855" title="Not referenced locally, nor via imports">FromTerm</span></span> = <span class="cons_Lit">"~caseStatement:"</span>       <span title="External reference">StrategoLang-Term</span>
    <span id="CaseStatementList_9904_9921" title="Not referenced locally, nor via imports">CaseStatementList</span>       .<span class="cons_Constructor"><span id="FromTerm_9929_9937" title="Not referenced locally, nor via imports">FromTerm</span></span> = <span class="cons_Lit">"~*"</span>                    <span title="External reference">StrategoLang-Term</span>
    <span id="CaseStatementList_9986_10003" title="Not referenced locally, nor via imports">CaseStatementList</span>       .<span class="cons_Constructor"><span id="FromTerm_10011_10019" title="Not referenced locally, nor via imports">FromTerm</span></span> = <span class="cons_Lit">"~*caseStatements:"</span>     <span title="External reference">StrategoLang-Term</span>
    <a href="#Expression_2876_2886" id="Expression_10068_10078" title="Referenced at line 57">Expression</a>              .<span class="cons_Constructor"><span id="FromTerm_10093_10101" title="Not referenced locally, nor via imports">FromTerm</span></span> = <span class="cons_Lit">"~*"</span>                    <span title="External reference">StrategoLang-Term</span>
    <a href="#Expression_2876_2886" id="Expression_10150_10160" title="Referenced at line 57">Expression</a>              .<span class="cons_Constructor"><span id="FromTerm_10175_10183" title="Not referenced locally, nor via imports">FromTerm</span></span> = <span class="cons_Lit">"~*expressions:"</span>        <span title="External reference">StrategoLang-Term</span>
    <a href="#SingleExpression_3030_3046" id="SingleExpression_10232_10248" title="Referenced at line 59">SingleExpression</a>        .<span class="cons_Constructor"><span id="FromTerm_10257_10265" title="Not referenced locally, nor via imports">FromTerm</span></span> = <span class="cons_Lit">"~"</span>                     <span title="External reference">StrategoLang-Term</span>
    <a href="#SingleExpression_3030_3046" id="SingleExpression_10314_10330" title="Referenced at line 59">SingleExpression</a>        .<span class="cons_Constructor"><span id="FromTerm_10339_10347" title="Not referenced locally, nor via imports">FromTerm</span></span> = <span class="cons_Lit">"~expression:"</span>          <span title="External reference">StrategoLang-Term</span>
    <a href="#CaseExpression_3188_3202" id="CaseExpression_10396_10410" title="Referenced at line 61">CaseExpression</a>          .<span class="cons_Constructor"><span id="FromTerm_10421_10429" title="Not referenced locally, nor via imports">FromTerm</span></span> = <span class="cons_Lit">"~"</span>                     <span title="External reference">StrategoLang-Term</span>
    <a href="#CaseExpression_3188_3202" id="CaseExpression_10478_10492" title="Referenced at line 61">CaseExpression</a>          .<span class="cons_Constructor"><span id="FromTerm_10503_10511" title="Not referenced locally, nor via imports">FromTerm</span></span> = <span class="cons_Lit">"~caseExpression:"</span>      <span title="External reference">StrategoLang-Term</span>
    <span id="CaseExpressionList_10560_10578" title="Not referenced locally, nor via imports">CaseExpressionList</span>      .<span class="cons_Constructor"><span id="FromTerm_10585_10593" title="Not referenced locally, nor via imports">FromTerm</span></span> = <span class="cons_Lit">"~*"</span>                    <span title="External reference">StrategoLang-Term</span>
    <span id="CaseExpressionList_10642_10660" title="Not referenced locally, nor via imports">CaseExpressionList</span>      .<span class="cons_Constructor"><span id="FromTerm_10667_10675" title="Not referenced locally, nor via imports">FromTerm</span></span> = <span class="cons_Lit">"~*caseExpressions:"</span>    <span title="External reference">StrategoLang-Term</span>

    <span class="layout">// --- Common.sdf3 -------</span>
    <span id="BOOL_10756_10760" title="Not referenced locally, nor via imports">BOOL</span>                    .<span class="cons_Constructor"><span id="FromTerm_10781_10789" title="Not referenced locally, nor via imports">FromTerm</span></span> = <span class="cons_Lit">"~boolean:"</span>             <span title="External reference">StrategoLang-Term</span>
    <span id="CHARACTER_10838_10847" title="Not referenced locally, nor via imports">CHARACTER</span>               .<span class="cons_Constructor"><span id="FromTerm_10863_10871" title="Not referenced locally, nor via imports">FromTerm</span></span> = <span class="cons_Lit">"~char:"</span>                <span title="External reference">StrategoLang-Term</span>
    <span id="FLOAT_10920_10925" title="Not referenced locally, nor via imports">FLOAT</span>                   .<span class="cons_Constructor"><span id="FromTerm_10945_10953" title="Not referenced locally, nor via imports">FromTerm</span></span> = <span class="cons_Lit">"~float:"</span>               <span title="External reference">StrategoLang-Term</span>
    <span id="INT_11002_11005" title="Not referenced locally, nor via imports">INT</span>                     .<span class="cons_Constructor"><span id="FromTerm_11027_11035" title="Not referenced locally, nor via imports">FromTerm</span></span> = <span class="cons_Lit">"~int:"</span>                 <span title="External reference">StrategoLang-Term</span>
    <span id="REAL_11084_11088" title="Not referenced locally, nor via imports">REAL</span>                    .<span class="cons_Constructor"><span id="FromTerm_11109_11117" title="Not referenced locally, nor via imports">FromTerm</span></span> = <span class="cons_Lit">"~real:"</span>                <span title="External reference">StrategoLang-Term</span>
    <span id="STRING_11166_11172" title="Not referenced locally, nor via imports">STRING</span>                  .<span class="cons_Constructor"><span id="FromTerm_11191_11199" title="Not referenced locally, nor via imports">FromTerm</span></span> = <span class="cons_Lit">"~string:"</span>              <span title="External reference">StrategoLang-Term</span>

</code></pre></td></tr></tbody></table></div>