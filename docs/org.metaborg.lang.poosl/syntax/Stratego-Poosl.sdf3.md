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
178
</pre></div></td>
<td class="code"><pre><code><span class="keyword">module</span> <span id="Stratego-Poosl_1_8" title="Not referenced">Stratego-Poosl</span>

<span class="keyword">imports</span>

    <span class="layout">// Meta language</span>
    <span title="External reference">StrategoLang/import-namespaced</span>
    <span title="External reference">StrategoLang/sugar/terms-namespaced</span>
    <span title="External reference">StrategoLang/core/modules-namespaced</span>

    <span class="layout">// Object Language</span>
    <a href="../Poosl.sdf3/#Poosl_1_8" id="Poosl_11_5" title="Defined at ../Poosl.sdf3 line 1">Poosl</a>
    <a href="../ExprStat.sdf3/#ExprStat_1_8" id="ExprStat_12_5" title="Defined at ../ExprStat.sdf3 line 1">ExprStat</a>

<span class="keyword">context-free start-symbols</span>

    <a href="#Start_20_5" id="Start_16_5" title="Defined at line 20">Start</a>   <span class="layout">// Auxiliary start symbol is a workaround to avoid pretty-print error</span>

<span class="keyword">context-free syntax</span>     <span class="layout">// === Auxiliary start symbol =======</span>

    <a href="#Start_16_5" id="Start_20_5" title="Referenced at line 16">Start</a> = <span title="External reference">StrategoLang-Module</span> <span class="layout">// from StrategoLang/import-namespaced</span>

<span class="keyword">context-free syntax</span>     <span class="layout">// === Quotation =======</span>

    <span class="layout">// --- Poosl.sdf3 -------</span>
    <span id="StrategoLang-PreTerm_25_5" title="Not referenced">StrategoLang-PreTerm</span>.<span class="cons_Constructor"><span id="ToTerm_25_26" title="Not referenced">ToTerm</span></span> =                    <span class="cons_Lit">"|["</span> <a href="#Poosl_67_5" id="Poosl_25_59" title="Defined at line 67, 68">Poosl</a> <span class="cons_Lit">"]|"</span>
    <span id="StrategoLang-PreTerm_26_5" title="Not referenced">StrategoLang-PreTerm</span>.<span class="cons_Constructor"><span id="ToTerm_26_26" title="Not referenced">ToTerm</span></span> = <span class="cons_Lit">"poosl"</span>            <span class="cons_Lit">"|["</span> <a href="#Poosl_67_5" id="Poosl_26_59" title="Defined at line 67, 68">Poosl</a> <span class="cons_Lit">"]|"</span>
    <span id="StrategoLang-PreTerm_27_5" title="Not referenced">StrategoLang-PreTerm</span>.<span class="cons_Constructor"><span id="ToTerm_27_26" title="Not referenced">ToTerm</span></span> =                    <span class="cons_Lit">"|["</span> <a href="#Import_70_5" id="Import_27_59" title="Defined at line 70, 71">Import</a> <span class="cons_Lit">"]|"</span>
    <span id="StrategoLang-PreTerm_28_5" title="Not referenced">StrategoLang-PreTerm</span>.<span class="cons_Constructor"><span id="ToTerm_28_26" title="Not referenced">ToTerm</span></span> = <span class="cons_Lit">"import"</span>           <span class="cons_Lit">"|["</span> <a href="#Import_70_5" id="Import_28_59" title="Defined at line 70, 71">Import</a> <span class="cons_Lit">"]|"</span>
    <span id="StrategoLang-PreTerm_29_5" title="Not referenced">StrategoLang-PreTerm</span>.<span class="cons_Constructor"><span id="ToTerm_29_26" title="Not referenced">ToTerm</span></span> =                    <span class="cons_Lit">"|["</span> <a href="#Annotation_75_5" id="Annotation_29_59" title="Defined at line 75, 76">Annotation</a> <span class="cons_Lit">"]|"</span>
    <span id="StrategoLang-PreTerm_30_5" title="Not referenced">StrategoLang-PreTerm</span>.<span class="cons_Constructor"><span id="ToTerm_30_26" title="Not referenced">ToTerm</span></span> = <span class="cons_Lit">"annotation"</span>       <span class="cons_Lit">"|["</span> <a href="#Annotation_75_5" id="Annotation_30_59" title="Defined at line 75, 76">Annotation</a> <span class="cons_Lit">"]|"</span>
    <span id="StrategoLang-PreTerm_31_5" title="Not referenced">StrategoLang-PreTerm</span>.<span class="cons_Constructor"><span id="ToTerm_31_26" title="Not referenced">ToTerm</span></span> =                    <span class="cons_Lit">"|["</span> <a href="#Class_80_5" id="Class_31_59" title="Defined at line 80, 81">Class</a> <span class="cons_Lit">"]|"</span>
    <span id="StrategoLang-PreTerm_32_5" title="Not referenced">StrategoLang-PreTerm</span>.<span class="cons_Constructor"><span id="ToTerm_32_26" title="Not referenced">ToTerm</span></span> = <span class="cons_Lit">"class"</span>            <span class="cons_Lit">"|["</span> <a href="#Class_80_5" id="Class_32_59" title="Defined at line 80, 81">Class</a> <span class="cons_Lit">"]|"</span>
    <span id="StrategoLang-PreTerm_33_5" title="Not referenced">StrategoLang-PreTerm</span>.<span class="cons_Constructor"><span id="ToTerm_33_26" title="Not referenced">ToTerm</span></span> =                    <span class="cons_Lit">"|["</span> <a href="#DataMethod_88_5" id="DataMethod_33_59" title="Defined at line 88, 89">DataMethod</a> <span class="cons_Lit">"]|"</span>
    <span id="StrategoLang-PreTerm_34_5" title="Not referenced">StrategoLang-PreTerm</span>.<span class="cons_Constructor"><span id="ToTerm_34_26" title="Not referenced">ToTerm</span></span> = <span class="cons_Lit">"dataMethod"</span>       <span class="cons_Lit">"|["</span> <a href="#DataMethod_88_5" id="DataMethod_34_59" title="Defined at line 88, 89">DataMethod</a> <span class="cons_Lit">"]|"</span>
    <span id="StrategoLang-PreTerm_35_5" title="Not referenced">StrategoLang-PreTerm</span>.<span class="cons_Constructor"><span id="ToTerm_35_26" title="Not referenced">ToTerm</span></span> =                    <span class="cons_Lit">"|["</span> <a href="#ProcessMethod_92_5" id="ProcessMethod_35_59" title="Defined at line 92, 93">ProcessMethod</a> <span class="cons_Lit">"]|"</span>
    <span id="StrategoLang-PreTerm_36_5" title="Not referenced">StrategoLang-PreTerm</span>.<span class="cons_Constructor"><span id="ToTerm_36_26" title="Not referenced">ToTerm</span></span> = <span class="cons_Lit">"processMethod"</span>    <span class="cons_Lit">"|["</span> <a href="#ProcessMethod_92_5" id="ProcessMethod_36_59" title="Defined at line 92, 93">ProcessMethod</a> <span class="cons_Lit">"]|"</span>
    <span id="StrategoLang-PreTerm_37_5" title="Not referenced">StrategoLang-PreTerm</span>.<span class="cons_Constructor"><span id="ToTerm_37_26" title="Not referenced">ToTerm</span></span> =                    <span class="cons_Lit">"|["</span> <a href="#Port_127_5" id="Port_37_59" title="Defined at line 127, 128">Port</a> <span class="cons_Lit">"]|"</span>
    <span id="StrategoLang-PreTerm_38_5" title="Not referenced">StrategoLang-PreTerm</span>.<span class="cons_Constructor"><span id="ToTerm_38_26" title="Not referenced">ToTerm</span></span> = <span class="cons_Lit">"port"</span>             <span class="cons_Lit">"|["</span> <a href="#Port_127_5" id="Port_38_59" title="Defined at line 127, 128">Port</a> <span class="cons_Lit">"]|"</span>
    <span id="StrategoLang-PreTerm_39_5" title="Not referenced">StrategoLang-PreTerm</span>.<span class="cons_Constructor"><span id="ToTerm_39_26" title="Not referenced">ToTerm</span></span> =                    <span class="cons_Lit">"|["</span> <a href="#MessageSignature_132_5" id="MessageSignature_39_59" title="Defined at line 132, 133">MessageSignature</a> <span class="cons_Lit">"]|"</span>
    <span id="StrategoLang-PreTerm_40_5" title="Not referenced">StrategoLang-PreTerm</span>.<span class="cons_Constructor"><span id="ToTerm_40_26" title="Not referenced">ToTerm</span></span> = <span class="cons_Lit">"messageSignature"</span> <span class="cons_Lit">"|["</span> <a href="#MessageSignature_132_5" id="MessageSignature_40_59" title="Defined at line 132, 133">MessageSignature</a> <span class="cons_Lit">"]|"</span>
    <span id="StrategoLang-PreTerm_41_5" title="Not referenced">StrategoLang-PreTerm</span>.<span class="cons_Constructor"><span id="ToTerm_41_26" title="Not referenced">ToTerm</span></span> =                    <span class="cons_Lit">"|["</span> <a href="#Instance_137_5" id="Instance_41_59" title="Defined at line 137, 138">Instance</a> <span class="cons_Lit">"]|"</span>
    <span id="StrategoLang-PreTerm_42_5" title="Not referenced">StrategoLang-PreTerm</span>.<span class="cons_Constructor"><span id="ToTerm_42_26" title="Not referenced">ToTerm</span></span> = <span class="cons_Lit">"instance"</span>         <span class="cons_Lit">"|["</span> <a href="#Instance_137_5" id="Instance_42_59" title="Defined at line 137, 138">Instance</a> <span class="cons_Lit">"]|"</span>
    <span id="StrategoLang-PreTerm_43_5" title="Not referenced">StrategoLang-PreTerm</span>.<span class="cons_Constructor"><span id="ToTerm_43_26" title="Not referenced">ToTerm</span></span> =                    <span class="cons_Lit">"|["</span> <a href="#Channel_142_5" id="Channel_43_59" title="Defined at line 142, 143">Channel</a> <span class="cons_Lit">"]|"</span>
    <span id="StrategoLang-PreTerm_44_5" title="Not referenced">StrategoLang-PreTerm</span>.<span class="cons_Constructor"><span id="ToTerm_44_26" title="Not referenced">ToTerm</span></span> = <span class="cons_Lit">"channel"</span>          <span class="cons_Lit">"|["</span> <a href="#Channel_142_5" id="Channel_44_59" title="Defined at line 142, 143">Channel</a> <span class="cons_Lit">"]|"</span>
    <span id="StrategoLang-PreTerm_45_5" title="Not referenced">StrategoLang-PreTerm</span>.<span class="cons_Constructor"><span id="ToTerm_45_26" title="Not referenced">ToTerm</span></span> =                    <span class="cons_Lit">"|["</span> <a href="#PortInstance_151_5" id="PortInstance_45_59" title="Defined at line 151, 152">PortInstance</a> <span class="cons_Lit">"]|"</span>
    <span id="StrategoLang-PreTerm_46_5" title="Not referenced">StrategoLang-PreTerm</span>.<span class="cons_Constructor"><span id="ToTerm_46_26" title="Not referenced">ToTerm</span></span> = <span class="cons_Lit">"portInstance"</span>     <span class="cons_Lit">"|["</span> <a href="#PortInstance_151_5" id="PortInstance_46_59" title="Defined at line 151, 152">PortInstance</a> <span class="cons_Lit">"]|"</span>
    <span id="StrategoLang-PreTerm_47_5" title="Not referenced">StrategoLang-PreTerm</span>.<span class="cons_Constructor"><span id="ToTerm_47_26" title="Not referenced">ToTerm</span></span> =                    <span class="cons_Lit">"|["</span> <a href="#Declaration_112_5" id="Declaration_47_59" title="Defined at line 112, 113">Declaration</a> <span class="cons_Lit">"]|"</span>
    <span id="StrategoLang-PreTerm_48_5" title="Not referenced">StrategoLang-PreTerm</span>.<span class="cons_Constructor"><span id="ToTerm_48_26" title="Not referenced">ToTerm</span></span> = <span class="cons_Lit">"declaration"</span>      <span class="cons_Lit">"|["</span> <a href="#Declaration_112_5" id="Declaration_48_59" title="Defined at line 112, 113">Declaration</a> <span class="cons_Lit">"]|"</span>

    <span class="layout">// --- ExprStat.sdf3 -------</span>
    <span id="StrategoLang-PreTerm_51_5" title="Not referenced">StrategoLang-PreTerm</span>.<span class="cons_Constructor"><span id="ToTerm_51_26" title="Not referenced">ToTerm</span></span> =                    <span class="cons_Lit">"|["</span> <a href="#Statement_155_5" id="Statement_51_59" title="Defined at line 155, 156">Statement</a> <span class="cons_Lit">"]|"</span>
    <span id="StrategoLang-PreTerm_52_5" title="Not referenced">StrategoLang-PreTerm</span>.<span class="cons_Constructor"><span id="ToTerm_52_26" title="Not referenced">ToTerm</span></span> = <span class="cons_Lit">"statements"</span>       <span class="cons_Lit">"|["</span> <a href="#Statement_155_5" id="Statement_52_59" title="Defined at line 155, 156">Statement</a> <span class="cons_Lit">"]|"</span>
    <span id="StrategoLang-PreTerm_53_5" title="Not referenced">StrategoLang-PreTerm</span>.<span class="cons_Constructor"><span id="ToTerm_53_26" title="Not referenced">ToTerm</span></span> =                    <span class="cons_Lit">"|["</span> <a href="#SingleStatement_157_5" id="SingleStatement_53_59" title="Defined at line 157, 158">SingleStatement</a> <span class="cons_Lit">"]|"</span>
    <span id="StrategoLang-PreTerm_54_5" title="Not referenced">StrategoLang-PreTerm</span>.<span class="cons_Constructor"><span id="ToTerm_54_26" title="Not referenced">ToTerm</span></span> = <span class="cons_Lit">"statement"</span>        <span class="cons_Lit">"|["</span> <a href="#SingleStatement_157_5" id="SingleStatement_54_59" title="Defined at line 157, 158">SingleStatement</a> <span class="cons_Lit">"]|"</span>
    <span id="StrategoLang-PreTerm_55_5" title="Not referenced">StrategoLang-PreTerm</span>.<span class="cons_Constructor"><span id="ToTerm_55_26" title="Not referenced">ToTerm</span></span> =                    <span class="cons_Lit">"|["</span> <a href="#CaseStatement_159_5" id="CaseStatement_55_59" title="Defined at line 159, 160">CaseStatement</a> <span class="cons_Lit">"]|"</span>
    <span id="StrategoLang-PreTerm_56_5" title="Not referenced">StrategoLang-PreTerm</span>.<span class="cons_Constructor"><span id="ToTerm_56_26" title="Not referenced">ToTerm</span></span> = <span class="cons_Lit">"caseStatement"</span>    <span class="cons_Lit">"|["</span> <a href="#CaseStatement_159_5" id="CaseStatement_56_59" title="Defined at line 159, 160">CaseStatement</a> <span class="cons_Lit">"]|"</span>
    <span id="StrategoLang-PreTerm_57_5" title="Not referenced">StrategoLang-PreTerm</span>.<span class="cons_Constructor"><span id="ToTerm_57_26" title="Not referenced">ToTerm</span></span> =                    <span class="cons_Lit">"|["</span> <a href="#Expression_163_5" id="Expression_57_59" title="Defined at line 163, 164">Expression</a> <span class="cons_Lit">"]|"</span>
    <span id="StrategoLang-PreTerm_58_5" title="Not referenced">StrategoLang-PreTerm</span>.<span class="cons_Constructor"><span id="ToTerm_58_26" title="Not referenced">ToTerm</span></span> = <span class="cons_Lit">"expressions"</span>      <span class="cons_Lit">"|["</span> <a href="#Expression_163_5" id="Expression_58_59" title="Defined at line 163, 164">Expression</a> <span class="cons_Lit">"]|"</span>
    <span id="StrategoLang-PreTerm_59_5" title="Not referenced">StrategoLang-PreTerm</span>.<span class="cons_Constructor"><span id="ToTerm_59_26" title="Not referenced">ToTerm</span></span> =                    <span class="cons_Lit">"|["</span> <a href="#SingleExpression_165_5" id="SingleExpression_59_59" title="Defined at line 165, 166">SingleExpression</a> <span class="cons_Lit">"]|"</span>
    <span id="StrategoLang-PreTerm_60_5" title="Not referenced">StrategoLang-PreTerm</span>.<span class="cons_Constructor"><span id="ToTerm_60_26" title="Not referenced">ToTerm</span></span> = <span class="cons_Lit">"expression"</span>       <span class="cons_Lit">"|["</span> <a href="#SingleExpression_165_5" id="SingleExpression_60_59" title="Defined at line 165, 166">SingleExpression</a> <span class="cons_Lit">"]|"</span>
    <span id="StrategoLang-PreTerm_61_5" title="Not referenced">StrategoLang-PreTerm</span>.<span class="cons_Constructor"><span id="ToTerm_61_26" title="Not referenced">ToTerm</span></span> =                    <span class="cons_Lit">"|["</span> <a href="#CaseExpression_167_5" id="CaseExpression_61_59" title="Defined at line 167, 168">CaseExpression</a> <span class="cons_Lit">"]|"</span>
    <span id="StrategoLang-PreTerm_62_5" title="Not referenced">StrategoLang-PreTerm</span>.<span class="cons_Constructor"><span id="ToTerm_62_26" title="Not referenced">ToTerm</span></span> = <span class="cons_Lit">"caseExpression"</span>   <span class="cons_Lit">"|["</span> <a href="#CaseExpression_167_5" id="CaseExpression_62_59" title="Defined at line 167, 168">CaseExpression</a> <span class="cons_Lit">"]|"</span>

<span class="keyword">context-free syntax</span>     <span class="layout">// === Anti-quotation =======</span>

    <span class="layout">// --- Poosl.sdf3 -------</span>
    <a href="#Poosl_25_59" id="Poosl_67_5" title="Referenced at line 25, 26">Poosl</a>                   .<span class="cons_Constructor"><span id="FromTerm_67_30" title="Not referenced">FromTerm</span></span> = <span class="cons_Lit">"~"</span>                     <span title="External reference">StrategoLang-Term</span>
    <a href="#Poosl_25_59" id="Poosl_68_5" title="Referenced at line 25, 26">Poosl</a>                   .<span class="cons_Constructor"><span id="FromTerm_68_30" title="Not referenced">FromTerm</span></span> = <span class="cons_Lit">"~poosl:"</span>               <span title="External reference">StrategoLang-Term</span>

    <a href="#Import_27_59" id="Import_70_5" title="Referenced at line 27, 28">Import</a>                  .<span class="cons_Constructor"><span id="FromTerm_70_30" title="Not referenced">FromTerm</span></span> = <span class="cons_Lit">"~"</span>                     <span title="External reference">StrategoLang-Term</span>
    <a href="#Import_27_59" id="Import_71_5" title="Referenced at line 27, 28">Import</a>                  .<span class="cons_Constructor"><span id="FromTerm_71_30" title="Not referenced">FromTerm</span></span> = <span class="cons_Lit">"~import:"</span>              <span title="External reference">StrategoLang-Term</span>
    <span id="ImportList_72_5" title="Not referenced">ImportList</span>              .<span class="cons_Constructor"><span id="FromTerm_72_30" title="Not referenced">FromTerm</span></span> = <span class="cons_Lit">"~*"</span>                    <span title="External reference">StrategoLang-Term</span>
    <span id="ImportList_73_5" title="Not referenced">ImportList</span>              .<span class="cons_Constructor"><span id="FromTerm_73_30" title="Not referenced">FromTerm</span></span> = <span class="cons_Lit">"~*imports:"</span>            <span title="External reference">StrategoLang-Term</span>

    <a href="#Annotation_29_59" id="Annotation_75_5" title="Referenced at line 29, 30">Annotation</a>              .<span class="cons_Constructor"><span id="FromTerm_75_30" title="Not referenced">FromTerm</span></span> = <span class="cons_Lit">"~"</span>                     <span title="External reference">StrategoLang-Term</span>
    <a href="#Annotation_29_59" id="Annotation_76_5" title="Referenced at line 29, 30">Annotation</a>              .<span class="cons_Constructor"><span id="FromTerm_76_30" title="Not referenced">FromTerm</span></span> = <span class="cons_Lit">"~annotation:"</span>          <span title="External reference">StrategoLang-Term</span>
    <span id="AnnotationList_77_5" title="Not referenced">AnnotationList</span>          .<span class="cons_Constructor"><span id="FromTerm_77_30" title="Not referenced">FromTerm</span></span> = <span class="cons_Lit">"~*"</span>                    <span title="External reference">StrategoLang-Term</span>
    <span id="AnnotationList_78_5" title="Not referenced">AnnotationList</span>          .<span class="cons_Constructor"><span id="FromTerm_78_30" title="Not referenced">FromTerm</span></span> = <span class="cons_Lit">"~*annotations:"</span>        <span title="External reference">StrategoLang-Term</span>

    <a href="#Class_31_59" id="Class_80_5" title="Referenced at line 31, 32">Class</a>                   .<span class="cons_Constructor"><span id="FromTerm_80_30" title="Not referenced">FromTerm</span></span> = <span class="cons_Lit">"~"</span>                     <span title="External reference">StrategoLang-Term</span>
    <a href="#Class_31_59" id="Class_81_5" title="Referenced at line 31, 32">Class</a>                   .<span class="cons_Constructor"><span id="FromTerm_81_30" title="Not referenced">FromTerm</span></span> = <span class="cons_Lit">"~class:"</span>               <span title="External reference">StrategoLang-Term</span>
    <span id="ClassList_82_5" title="Not referenced">ClassList</span>               .<span class="cons_Constructor"><span id="FromTerm_82_30" title="Not referenced">FromTerm</span></span> = <span class="cons_Lit">"~*"</span>                    <span title="External reference">StrategoLang-Term</span>
    <span id="ClassList_83_5" title="Not referenced">ClassList</span>               .<span class="cons_Constructor"><span id="FromTerm_83_30" title="Not referenced">FromTerm</span></span> = <span class="cons_Lit">"~*classes:"</span>            <span title="External reference">StrategoLang-Term</span>

    <span id="ExtendsClause_85_5" title="Not referenced">ExtendsClause</span>           .<span class="cons_Constructor"><span id="FromTerm_85_30" title="Not referenced">FromTerm</span></span> = <span class="cons_Lit">"~"</span>                     <span title="External reference">StrategoLang-Term</span>
    <span id="ExtendsClause_86_5" title="Not referenced">ExtendsClause</span>           .<span class="cons_Constructor"><span id="FromTerm_86_30" title="Not referenced">FromTerm</span></span> = <span class="cons_Lit">"~extends:"</span>             <span title="External reference">StrategoLang-Term</span>

    <a href="#DataMethod_33_59" id="DataMethod_88_5" title="Referenced at line 33, 34">DataMethod</a>              .<span class="cons_Constructor"><span id="FromTerm_88_30" title="Not referenced">FromTerm</span></span> = <span class="cons_Lit">"~"</span>                     <span title="External reference">StrategoLang-Term</span>
    <a href="#DataMethod_33_59" id="DataMethod_89_5" title="Referenced at line 33, 34">DataMethod</a>              .<span class="cons_Constructor"><span id="FromTerm_89_30" title="Not referenced">FromTerm</span></span> = <span class="cons_Lit">"~method:"</span>              <span title="External reference">StrategoLang-Term</span>
    <span id="DataMethodList_90_5" title="Not referenced">DataMethodList</span>          .<span class="cons_Constructor"><span id="FromTerm_90_30" title="Not referenced">FromTerm</span></span> = <span class="cons_Lit">"~"</span>                     <span title="External reference">StrategoLang-Term</span>
    <span id="DataMethodList_91_5" title="Not referenced">DataMethodList</span>          .<span class="cons_Constructor"><span id="FromTerm_91_30" title="Not referenced">FromTerm</span></span> = <span class="cons_Lit">"~*methods:"</span>            <span title="External reference">StrategoLang-Term</span>
    <a href="#ProcessMethod_35_59" id="ProcessMethod_92_5" title="Referenced at line 35, 36">ProcessMethod</a>           .<span class="cons_Constructor"><span id="FromTerm_92_30" title="Not referenced">FromTerm</span></span> = <span class="cons_Lit">"~"</span>                     <span title="External reference">StrategoLang-Term</span>
    <a href="#ProcessMethod_35_59" id="ProcessMethod_93_5" title="Referenced at line 35, 36">ProcessMethod</a>           .<span class="cons_Constructor"><span id="FromTerm_93_30" title="Not referenced">FromTerm</span></span> = <span class="cons_Lit">"~method:"</span>              <span title="External reference">StrategoLang-Term</span>
    <span id="ProcessMethodList_94_5" title="Not referenced">ProcessMethodList</span>       .<span class="cons_Constructor"><span id="FromTerm_94_30" title="Not referenced">FromTerm</span></span> = <span class="cons_Lit">"~"</span>                     <span title="External reference">StrategoLang-Term</span>
    <span id="ProcessMethodList_95_5" title="Not referenced">ProcessMethodList</span>       .<span class="cons_Constructor"><span id="FromTerm_95_30" title="Not referenced">FromTerm</span></span> = <span class="cons_Lit">"~*methods:"</span>            <span title="External reference">StrategoLang-Term</span>

    <span id="ID_97_5" title="Not referenced">ID</span>                      .<span class="cons_Constructor"><span id="FromTerm_97_30" title="Not referenced">FromTerm</span></span> = <span class="cons_Lit">"~"</span>                     <span title="External reference">StrategoLang-Term</span>
    <span id="ID_98_5" title="Not referenced">ID</span>                      .<span class="cons_Constructor"><span id="FromTerm_98_30" title="Not referenced">FromTerm</span></span> = <span class="cons_Lit">"~id:"</span>                  <span title="External reference">StrategoLang-Term</span>
    <span id="IDList_99_5" title="Not referenced">IDList</span>                  .<span class="cons_Constructor"><span id="FromTerm_99_30" title="Not referenced">FromTerm</span></span> = <span class="cons_Lit">"~*"</span>                    <span title="External reference">StrategoLang-Term</span>
    <span id="IDList_100_5" title="Not referenced">IDList</span>                  .<span class="cons_Constructor"><span id="FromTerm_100_30" title="Not referenced">FromTerm</span></span> = <span class="cons_Lit">"~*ids:"</span>                <span title="External reference">StrategoLang-Term</span>
    <span id="OptMessageParameterList_101_5" title="Not referenced">OptMessageParameterList</span> .<span class="cons_Constructor"><span id="FromTerm_101_30" title="Not referenced">FromTerm</span></span> = <span class="cons_Lit">"~*"</span>                    <span title="External reference">StrategoLang-Term</span>
    <span id="OptMessageParameterList_102_5" title="Not referenced">OptMessageParameterList</span> .<span class="cons_Constructor"><span id="FromTerm_102_30" title="Not referenced">FromTerm</span></span> = <span class="cons_Lit">"~*ids:"</span>                <span title="External reference">StrategoLang-Term</span>
    <span id="OptVariableList_103_5" title="Not referenced">OptVariableList</span>         .<span class="cons_Constructor"><span id="FromTerm_103_30" title="Not referenced">FromTerm</span></span> = <span class="cons_Lit">"~*"</span>                    <span title="External reference">StrategoLang-Term</span>
    <span id="OptVariableList_104_5" title="Not referenced">OptVariableList</span>         .<span class="cons_Constructor"><span id="FromTerm_104_30" title="Not referenced">FromTerm</span></span> = <span class="cons_Lit">"~*ids:"</span>                <span title="External reference">StrategoLang-Term</span>
    <span id="VariableList_105_5" title="Not referenced">VariableList</span>            .<span class="cons_Constructor"><span id="FromTerm_105_30" title="Not referenced">FromTerm</span></span> = <span class="cons_Lit">"~*"</span>                    <span title="External reference">StrategoLang-Term</span>
    <span id="VariableList_106_5" title="Not referenced">VariableList</span>            .<span class="cons_Constructor"><span id="FromTerm_106_30" title="Not referenced">FromTerm</span></span> = <span class="cons_Lit">"~*ids:"</span>                <span title="External reference">StrategoLang-Term</span>
    <span id="UnaryOperator_107_5" title="Not referenced">UnaryOperator</span>           .<span class="cons_Constructor"><span id="FromTerm_107_30" title="Not referenced">FromTerm</span></span> = <span class="cons_Lit">"~"</span>                     <span title="External reference">StrategoLang-Term</span>
    <span id="UnaryOperator_108_5" title="Not referenced">UnaryOperator</span>           .<span class="cons_Constructor"><span id="FromTerm_108_30" title="Not referenced">FromTerm</span></span> = <span class="cons_Lit">"~unOp:"</span>                <span title="External reference">StrategoLang-Term</span>
    <span id="OperatorBinary_109_5" title="Not referenced">OperatorBinary</span>          .<span class="cons_Constructor"><span id="FromTerm_109_30" title="Not referenced">FromTerm</span></span> = <span class="cons_Lit">"~"</span>                     <span title="External reference">StrategoLang-Term</span>
    <span id="OperatorBinary_110_5" title="Not referenced">OperatorBinary</span>          .<span class="cons_Constructor"><span id="FromTerm_110_30" title="Not referenced">FromTerm</span></span> = <span class="cons_Lit">"~binOp:"</span>               <span title="External reference">StrategoLang-Term</span>

    <a href="#Declaration_47_59" id="Declaration_112_5" title="Referenced at line 47, 48">Declaration</a>             .<span class="cons_Constructor"><span id="FromTerm_112_30" title="Not referenced">FromTerm</span></span> = <span class="cons_Lit">"~"</span>                     <span title="External reference">StrategoLang-Term</span>
    <a href="#Declaration_47_59" id="Declaration_113_5" title="Referenced at line 47, 48">Declaration</a>             .<span class="cons_Constructor"><span id="FromTerm_113_30" title="Not referenced">FromTerm</span></span> = <span class="cons_Lit">"~declaration:"</span>         <span title="External reference">StrategoLang-Term</span>
    <span id="DeclarationOptComma_114_5" title="Not referenced">DeclarationOptComma</span>     .<span class="cons_Constructor"><span id="FromTerm_114_30" title="Not referenced">FromTerm</span></span> = <span class="cons_Lit">"~"</span>                     <span title="External reference">StrategoLang-Term</span>
    <span id="DeclarationOptComma_115_5" title="Not referenced">DeclarationOptComma</span>     .<span class="cons_Constructor"><span id="FromTerm_115_30" title="Not referenced">FromTerm</span></span> = <span class="cons_Lit">"~declaration:"</span>         <span title="External reference">StrategoLang-Term</span>
    <span id="DeclarationOptCommaList_116_5" title="Not referenced">DeclarationOptCommaList</span> .<span class="cons_Constructor"><span id="FromTerm_116_30" title="Not referenced">FromTerm</span></span> = <span class="cons_Lit">"~*"</span>                    <span title="External reference">StrategoLang-Term</span>
    <span id="DeclarationOptCommaList_117_5" title="Not referenced">DeclarationOptCommaList</span> .<span class="cons_Constructor"><span id="FromTerm_117_30" title="Not referenced">FromTerm</span></span> = <span class="cons_Lit">"~*declarations:"</span>       <span title="External reference">StrategoLang-Term</span>
    <span id="ParameterList_118_5" title="Not referenced">ParameterList</span>           .<span class="cons_Constructor"><span id="FromTerm_118_30" title="Not referenced">FromTerm</span></span> = <span class="cons_Lit">"~*"</span>                    <span title="External reference">StrategoLang-Term</span>
    <span id="ParameterList_119_5" title="Not referenced">ParameterList</span>           .<span class="cons_Constructor"><span id="FromTerm_119_30" title="Not referenced">FromTerm</span></span> = <span class="cons_Lit">"~*declarations:"</span>       <span title="External reference">StrategoLang-Term</span>
    <span id="OptParameterList_120_5" title="Not referenced">OptParameterList</span>        .<span class="cons_Constructor"><span id="FromTerm_120_30" title="Not referenced">FromTerm</span></span> = <span class="cons_Lit">"~*"</span>                    <span title="External reference">StrategoLang-Term</span>
    <span id="OptParameterList_121_5" title="Not referenced">OptParameterList</span>        .<span class="cons_Constructor"><span id="FromTerm_121_30" title="Not referenced">FromTerm</span></span> = <span class="cons_Lit">"~*declarations:"</span>       <span title="External reference">StrategoLang-Term</span>
    <span id="OptLocalVariableList_122_5" title="Not referenced">OptLocalVariableList</span>    .<span class="cons_Constructor"><span id="FromTerm_122_30" title="Not referenced">FromTerm</span></span> = <span class="cons_Lit">"~*"</span>                    <span title="External reference">StrategoLang-Term</span>
    <span id="OptLocalVariableList_123_5" title="Not referenced">OptLocalVariableList</span>    .<span class="cons_Constructor"><span id="FromTerm_123_30" title="Not referenced">FromTerm</span></span> = <span class="cons_Lit">"~*declarations:"</span>       <span title="External reference">StrategoLang-Term</span>
    <span id="OptEmptyList_124_5" title="Not referenced">OptEmptyList</span>            .<span class="cons_Constructor"><span id="FromTerm_124_30" title="Not referenced">FromTerm</span></span> = <span class="cons_Lit">"~*"</span>                    <span title="External reference">StrategoLang-Term</span>
    <span id="OptEmptyList_125_5" title="Not referenced">OptEmptyList</span>            .<span class="cons_Constructor"><span id="FromTerm_125_30" title="Not referenced">FromTerm</span></span> = <span class="cons_Lit">"~*declarations:"</span>       <span title="External reference">StrategoLang-Term</span>

    <a href="#Port_37_59" id="Port_127_5" title="Referenced at line 37, 38">Port</a>                    .<span class="cons_Constructor"><span id="FromTerm_127_30" title="Not referenced">FromTerm</span></span> = <span class="cons_Lit">"~"</span>                     <span title="External reference">StrategoLang-Term</span>
    <a href="#Port_37_59" id="Port_128_5" title="Referenced at line 37, 38">Port</a>                    .<span class="cons_Constructor"><span id="FromTerm_128_30" title="Not referenced">FromTerm</span></span> = <span class="cons_Lit">"~port:"</span>                <span title="External reference">StrategoLang-Term</span>
    <span id="PortList_129_5" title="Not referenced">PortList</span>                .<span class="cons_Constructor"><span id="FromTerm_129_30" title="Not referenced">FromTerm</span></span> = <span class="cons_Lit">"~*"</span>                    <span title="External reference">StrategoLang-Term</span>
    <span id="PortList_130_5" title="Not referenced">PortList</span>                .<span class="cons_Constructor"><span id="FromTerm_130_30" title="Not referenced">FromTerm</span></span> = <span class="cons_Lit">"~*ports:"</span>              <span title="External reference">StrategoLang-Term</span>

    <a href="#MessageSignature_39_59" id="MessageSignature_132_5" title="Referenced at line 39, 40">MessageSignature</a>        .<span class="cons_Constructor"><span id="FromTerm_132_30" title="Not referenced">FromTerm</span></span> = <span class="cons_Lit">"~"</span>                     <span title="External reference">StrategoLang-Term</span>
    <a href="#MessageSignature_39_59" id="MessageSignature_133_5" title="Referenced at line 39, 40">MessageSignature</a>        .<span class="cons_Constructor"><span id="FromTerm_133_30" title="Not referenced">FromTerm</span></span> = <span class="cons_Lit">"~message:"</span>             <span title="External reference">StrategoLang-Term</span>
    <span id="MessageSignatureList_134_5" title="Not referenced">MessageSignatureList</span>    .<span class="cons_Constructor"><span id="FromTerm_134_30" title="Not referenced">FromTerm</span></span> = <span class="cons_Lit">"~*"</span>                    <span title="External reference">StrategoLang-Term</span>
    <span id="MessageSignatureList_135_5" title="Not referenced">MessageSignatureList</span>    .<span class="cons_Constructor"><span id="FromTerm_135_30" title="Not referenced">FromTerm</span></span> = <span class="cons_Lit">"~*messages:"</span>           <span title="External reference">StrategoLang-Term</span>

    <a href="#Instance_41_59" id="Instance_137_5" title="Referenced at line 41, 42">Instance</a>                .<span class="cons_Constructor"><span id="FromTerm_137_30" title="Not referenced">FromTerm</span></span> = <span class="cons_Lit">"~"</span>                     <span title="External reference">StrategoLang-Term</span>
    <a href="#Instance_41_59" id="Instance_138_5" title="Referenced at line 41, 42">Instance</a>                .<span class="cons_Constructor"><span id="FromTerm_138_30" title="Not referenced">FromTerm</span></span> = <span class="cons_Lit">"~instance:"</span>            <span title="External reference">StrategoLang-Term</span>
    <span id="InstanceList_139_5" title="Not referenced">InstanceList</span>            .<span class="cons_Constructor"><span id="FromTerm_139_30" title="Not referenced">FromTerm</span></span> = <span class="cons_Lit">"~*"</span>                    <span title="External reference">StrategoLang-Term</span>
    <span id="InstanceList_140_5" title="Not referenced">InstanceList</span>            .<span class="cons_Constructor"><span id="FromTerm_140_30" title="Not referenced">FromTerm</span></span> = <span class="cons_Lit">"~*instances:"</span>          <span title="External reference">StrategoLang-Term</span>

    <a href="#Channel_43_59" id="Channel_142_5" title="Referenced at line 43, 44">Channel</a>                 .<span class="cons_Constructor"><span id="FromTerm_142_30" title="Not referenced">FromTerm</span></span> = <span class="cons_Lit">"~"</span>                     <span title="External reference">StrategoLang-Term</span>
    <a href="#Channel_43_59" id="Channel_143_5" title="Referenced at line 43, 44">Channel</a>                 .<span class="cons_Constructor"><span id="FromTerm_143_30" title="Not referenced">FromTerm</span></span> = <span class="cons_Lit">"~channel:"</span>             <span title="External reference">StrategoLang-Term</span>
    <span id="ChannelList_144_5" title="Not referenced">ChannelList</span>             .<span class="cons_Constructor"><span id="FromTerm_144_30" title="Not referenced">FromTerm</span></span> = <span class="cons_Lit">"~*"</span>                    <span title="External reference">StrategoLang-Term</span>
    <span id="ChannelList_145_5" title="Not referenced">ChannelList</span>             .<span class="cons_Constructor"><span id="FromTerm_145_30" title="Not referenced">FromTerm</span></span> = <span class="cons_Lit">"~*channels:"</span>           <span title="External reference">StrategoLang-Term</span>

    <span id="InstanceParameter_147_5" title="Not referenced">InstanceParameter</span>       .<span class="cons_Constructor"><span id="FromTerm_147_30" title="Not referenced">FromTerm</span></span> = <span class="cons_Lit">"~"</span>                     <span title="External reference">StrategoLang-Term</span>
    <span id="InstanceParameter_148_5" title="Not referenced">InstanceParameter</span>       .<span class="cons_Constructor"><span id="FromTerm_148_30" title="Not referenced">FromTerm</span></span> = <span class="cons_Lit">"~instanceParameter:"</span>   <span title="External reference">StrategoLang-Term</span>
    <span id="OptInstanceParameterList_149_5" title="Not referenced">OptInstanceParameterList</span>.<span class="cons_Constructor"><span id="FromTerm_149_30" title="Not referenced">FromTerm</span></span> = <span class="cons_Lit">"~*"</span>                    <span title="External reference">StrategoLang-Term</span>
    <span id="OptInstanceParameterList_150_5" title="Not referenced">OptInstanceParameterList</span>.<span class="cons_Constructor"><span id="FromTerm_150_30" title="Not referenced">FromTerm</span></span> = <span class="cons_Lit">"~*instanceParameters:"</span> <span title="External reference">StrategoLang-Term</span>
    <a href="#PortInstance_45_59" id="PortInstance_151_5" title="Referenced at line 45, 46">PortInstance</a>            .<span class="cons_Constructor"><span id="FromTerm_151_30" title="Not referenced">FromTerm</span></span> = <span class="cons_Lit">"~"</span>                     <span title="External reference">StrategoLang-Term</span>
    <a href="#PortInstance_45_59" id="PortInstance_152_5" title="Referenced at line 45, 46">PortInstance</a>            .<span class="cons_Constructor"><span id="FromTerm_152_30" title="Not referenced">FromTerm</span></span> = <span class="cons_Lit">"~portInstance:"</span>        <span title="External reference">StrategoLang-Term</span>

    <span class="layout">// --- ExprStat.sdf3 -------</span>
    <a href="#Statement_51_59" id="Statement_155_5" title="Referenced at line 51, 52">Statement</a>               .<span class="cons_Constructor"><span id="FromTerm_155_30" title="Not referenced">FromTerm</span></span> = <span class="cons_Lit">"~*"</span>                    <span title="External reference">StrategoLang-Term</span>
    <a href="#Statement_51_59" id="Statement_156_5" title="Referenced at line 51, 52">Statement</a>               .<span class="cons_Constructor"><span id="FromTerm_156_30" title="Not referenced">FromTerm</span></span> = <span class="cons_Lit">"~*statements:"</span>         <span title="External reference">StrategoLang-Term</span>
    <a href="#SingleStatement_53_59" id="SingleStatement_157_5" title="Referenced at line 53, 54">SingleStatement</a>         .<span class="cons_Constructor"><span id="FromTerm_157_30" title="Not referenced">FromTerm</span></span> = <span class="cons_Lit">"~"</span>                     <span title="External reference">StrategoLang-Term</span>
    <a href="#SingleStatement_53_59" id="SingleStatement_158_5" title="Referenced at line 53, 54">SingleStatement</a>         .<span class="cons_Constructor"><span id="FromTerm_158_30" title="Not referenced">FromTerm</span></span> = <span class="cons_Lit">"~statement:"</span>           <span title="External reference">StrategoLang-Term</span>
    <a href="#CaseStatement_55_59" id="CaseStatement_159_5" title="Referenced at line 55, 56">CaseStatement</a>           .<span class="cons_Constructor"><span id="FromTerm_159_30" title="Not referenced">FromTerm</span></span> = <span class="cons_Lit">"~"</span>                     <span title="External reference">StrategoLang-Term</span>
    <a href="#CaseStatement_55_59" id="CaseStatement_160_5" title="Referenced at line 55, 56">CaseStatement</a>           .<span class="cons_Constructor"><span id="FromTerm_160_30" title="Not referenced">FromTerm</span></span> = <span class="cons_Lit">"~caseStatement:"</span>       <span title="External reference">StrategoLang-Term</span>
    <span id="CaseStatementList_161_5" title="Not referenced">CaseStatementList</span>       .<span class="cons_Constructor"><span id="FromTerm_161_30" title="Not referenced">FromTerm</span></span> = <span class="cons_Lit">"~*"</span>                    <span title="External reference">StrategoLang-Term</span>
    <span id="CaseStatementList_162_5" title="Not referenced">CaseStatementList</span>       .<span class="cons_Constructor"><span id="FromTerm_162_30" title="Not referenced">FromTerm</span></span> = <span class="cons_Lit">"~*caseStatements:"</span>     <span title="External reference">StrategoLang-Term</span>
    <a href="#Expression_57_59" id="Expression_163_5" title="Referenced at line 57, 58">Expression</a>              .<span class="cons_Constructor"><span id="FromTerm_163_30" title="Not referenced">FromTerm</span></span> = <span class="cons_Lit">"~*"</span>                    <span title="External reference">StrategoLang-Term</span>
    <a href="#Expression_57_59" id="Expression_164_5" title="Referenced at line 57, 58">Expression</a>              .<span class="cons_Constructor"><span id="FromTerm_164_30" title="Not referenced">FromTerm</span></span> = <span class="cons_Lit">"~*expressions:"</span>        <span title="External reference">StrategoLang-Term</span>
    <a href="#SingleExpression_59_59" id="SingleExpression_165_5" title="Referenced at line 59, 60">SingleExpression</a>        .<span class="cons_Constructor"><span id="FromTerm_165_30" title="Not referenced">FromTerm</span></span> = <span class="cons_Lit">"~"</span>                     <span title="External reference">StrategoLang-Term</span>
    <a href="#SingleExpression_59_59" id="SingleExpression_166_5" title="Referenced at line 59, 60">SingleExpression</a>        .<span class="cons_Constructor"><span id="FromTerm_166_30" title="Not referenced">FromTerm</span></span> = <span class="cons_Lit">"~expression:"</span>          <span title="External reference">StrategoLang-Term</span>
    <a href="#CaseExpression_61_59" id="CaseExpression_167_5" title="Referenced at line 61, 62">CaseExpression</a>          .<span class="cons_Constructor"><span id="FromTerm_167_30" title="Not referenced">FromTerm</span></span> = <span class="cons_Lit">"~"</span>                     <span title="External reference">StrategoLang-Term</span>
    <a href="#CaseExpression_61_59" id="CaseExpression_168_5" title="Referenced at line 61, 62">CaseExpression</a>          .<span class="cons_Constructor"><span id="FromTerm_168_30" title="Not referenced">FromTerm</span></span> = <span class="cons_Lit">"~caseExpression:"</span>      <span title="External reference">StrategoLang-Term</span>
    <span id="CaseExpressionList_169_5" title="Not referenced">CaseExpressionList</span>      .<span class="cons_Constructor"><span id="FromTerm_169_30" title="Not referenced">FromTerm</span></span> = <span class="cons_Lit">"~*"</span>                    <span title="External reference">StrategoLang-Term</span>
    <span id="CaseExpressionList_170_5" title="Not referenced">CaseExpressionList</span>      .<span class="cons_Constructor"><span id="FromTerm_170_30" title="Not referenced">FromTerm</span></span> = <span class="cons_Lit">"~*caseExpressions:"</span>    <span title="External reference">StrategoLang-Term</span>

    <span class="layout">// --- Common.sdf3 -------</span>
    <span id="BOOL_173_5" title="Not referenced">BOOL</span>                    .<span class="cons_Constructor"><span id="FromTerm_173_30" title="Not referenced">FromTerm</span></span> = <span class="cons_Lit">"~boolean:"</span>             <span title="External reference">StrategoLang-Term</span>
    <span id="CHARACTER_174_5" title="Not referenced">CHARACTER</span>               .<span class="cons_Constructor"><span id="FromTerm_174_30" title="Not referenced">FromTerm</span></span> = <span class="cons_Lit">"~char:"</span>                <span title="External reference">StrategoLang-Term</span>
    <span id="FLOAT_175_5" title="Not referenced">FLOAT</span>                   .<span class="cons_Constructor"><span id="FromTerm_175_30" title="Not referenced">FromTerm</span></span> = <span class="cons_Lit">"~float:"</span>               <span title="External reference">StrategoLang-Term</span>
    <span id="INT_176_5" title="Not referenced">INT</span>                     .<span class="cons_Constructor"><span id="FromTerm_176_30" title="Not referenced">FromTerm</span></span> = <span class="cons_Lit">"~int:"</span>                 <span title="External reference">StrategoLang-Term</span>
    <span id="REAL_177_5" title="Not referenced">REAL</span>                    .<span class="cons_Constructor"><span id="FromTerm_177_30" title="Not referenced">FromTerm</span></span> = <span class="cons_Lit">"~real:"</span>                <span title="External reference">StrategoLang-Term</span>
    <span id="STRING_178_5" title="Not referenced">STRING</span>                  .<span class="cons_Constructor"><span id="FromTerm_178_30" title="Not referenced">FromTerm</span></span> = <span class="cons_Lit">"~string:"</span>              <span title="External reference">StrategoLang-Term</span>

</code></pre></td></tr></tbody></table></div>

<div id="modal">
  <div id="modal-content">
    <span id="modal-close">&times;</span>
    <h2 id="modal-h2"></h2>
    <p  id="modal-p"></p>
    <ul id="modal-ul"></ul>
  </div>
</div>
