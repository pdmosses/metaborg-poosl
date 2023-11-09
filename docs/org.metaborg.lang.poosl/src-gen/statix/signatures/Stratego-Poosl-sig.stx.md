---
title: Stratego-Poosl-sig.stx
hide:
  - toc
---

# `Stratego-Poosl-sig.stx`



[pdmosses/metaborg-poosl/org.metaborg.lang.poosl/src-gen/statix/signatures/Stratego-Poosl-sig.stx]: https://github.com/pdmosses/metaborg-poosl/blob/master/org.metaborg.lang.poosl/src-gen/statix/signatures/Stratego-Poosl-sig.stx "The source file on GitHub"

<div class="stx"><table class="highlighttable"><tbody><tr><td class="linenos"><div class="linenodiv"><pre><span></span>1
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
</pre></div></td>
<td class="code"><pre><code><span class="keyword">module</span> <span id="signatures/Stratego-Poosl-sig_1_8" title="Not referenced"><span class="token sort_Id">signatures/Stratego-Poosl-sig</span></span>

<span class="keyword">imports</span>
  signatures/StrategoLang/import-namespaced-sig
  signatures/StrategoLang/sugar/terms-namespaced-sig
  signatures/StrategoLang/core/modules-namespaced-sig
  <a href="../Poosl-sig.stx/#signatures/Poosl-sig_1_8" id="signatures/Poosl-sig_7_3" title="Defined at ../Poosl-sig.stx line 1"><span class="token sort_Id">signatures/Poosl-sig</span></a>
  <a href="../ExprStat-sig.stx/#signatures/ExprStat-sig_1_8" id="signatures/ExprStat-sig_8_3" title="Defined at ../ExprStat-sig.stx line 1"><span class="token sort_Id">signatures/ExprStat-sig</span></a>

<span class="keyword">signature</span>

  <span class="keyword">sorts</span>

  <span class="keyword">constructors</span>

<span class="keyword">signature</span>

  <span class="keyword">constructors</span>
    <span class="cons_OpDecl"><span id="StrategoLang-Module2Start_19_5" title="Not referenced"><span class="token sort_Id">StrategoLang-Module2Start</span></span> <span class="operator">:</span> <span class="cons_SimpleSort">StrategoLang-Module</span> <span class="operator">-&gt;</span> <span class="cons_SimpleSort">Start</span></span>
    <span class="cons_OpDecl"><span id="ToTerm_20_5" title="Not referenced"><span class="token sort_Id">ToTerm</span></span> <span class="operator">:</span> <span class="cons_SimpleSort"><a href="../Poosl-sig.stx/#Poosl_10_5" id="Poosl_20_14" title="Defined at ../Poosl-sig.stx line 10"><span class="token sort_Id">Poosl</span></a></span> <span class="operator">-&gt;</span> <span class="cons_SimpleSort">StrategoLang-PreTerm</span></span>
    <span class="cons_OpDecl"><span id="ToTerm_21_5" title="Not referenced"><span class="token sort_Id">ToTerm</span></span> <span class="operator">:</span> <span class="cons_SimpleSort"><a href="../Poosl-sig.stx/#Poosl_10_5" id="Poosl_21_14" title="Defined at ../Poosl-sig.stx line 10"><span class="token sort_Id">Poosl</span></a></span> <span class="operator">-&gt;</span> <span class="cons_SimpleSort">StrategoLang-PreTerm</span></span>
    <span class="cons_OpDecl"><span id="ToTerm_22_5" title="Not referenced"><span class="token sort_Id">ToTerm</span></span> <span class="operator">:</span> <span class="cons_SimpleSort"><a href="../Poosl-sig.stx/#Import_12_5" id="Import_22_14" title="Defined at ../Poosl-sig.stx line 12"><span class="token sort_Id">Import</span></a></span> <span class="operator">-&gt;</span> <span class="cons_SimpleSort">StrategoLang-PreTerm</span></span>
    <span class="cons_OpDecl"><span id="ToTerm_23_5" title="Not referenced"><span class="token sort_Id">ToTerm</span></span> <span class="operator">:</span> <span class="cons_SimpleSort"><a href="../Poosl-sig.stx/#Import_12_5" id="Import_23_14" title="Defined at ../Poosl-sig.stx line 12"><span class="token sort_Id">Import</span></a></span> <span class="operator">-&gt;</span> <span class="cons_SimpleSort">StrategoLang-PreTerm</span></span>
    <span class="cons_OpDecl"><span id="ToTerm_24_5" title="Not referenced"><span class="token sort_Id">ToTerm</span></span> <span class="operator">:</span> <span class="cons_SimpleSort"><a href="../Poosl-sig.stx/#Annotation_14_5" id="Annotation_24_14" title="Defined at ../Poosl-sig.stx line 14"><span class="token sort_Id">Annotation</span></a></span> <span class="operator">-&gt;</span> <span class="cons_SimpleSort">StrategoLang-PreTerm</span></span>
    <span class="cons_OpDecl"><span id="ToTerm_25_5" title="Not referenced"><span class="token sort_Id">ToTerm</span></span> <span class="operator">:</span> <span class="cons_SimpleSort"><a href="../Poosl-sig.stx/#Annotation_14_5" id="Annotation_25_14" title="Defined at ../Poosl-sig.stx line 14"><span class="token sort_Id">Annotation</span></a></span> <span class="operator">-&gt;</span> <span class="cons_SimpleSort">StrategoLang-PreTerm</span></span>
    <span class="cons_OpDecl"><span id="ToTerm_26_5" title="Not referenced"><span class="token sort_Id">ToTerm</span></span> <span class="operator">:</span> <span class="cons_SimpleSort"><a href="../Poosl-sig.stx/#Class_16_5" id="Class_26_14" title="Defined at ../Poosl-sig.stx line 16"><span class="token sort_Id">Class</span></a></span> <span class="operator">-&gt;</span> <span class="cons_SimpleSort">StrategoLang-PreTerm</span></span>
    <span class="cons_OpDecl"><span id="ToTerm_27_5" title="Not referenced"><span class="token sort_Id">ToTerm</span></span> <span class="operator">:</span> <span class="cons_SimpleSort"><a href="../Poosl-sig.stx/#Class_16_5" id="Class_27_14" title="Defined at ../Poosl-sig.stx line 16"><span class="token sort_Id">Class</span></a></span> <span class="operator">-&gt;</span> <span class="cons_SimpleSort">StrategoLang-PreTerm</span></span>
    <span class="cons_OpDecl"><span id="ToTerm_28_5" title="Not referenced"><span class="token sort_Id">ToTerm</span></span> <span class="operator">:</span> <span class="cons_SimpleSort"><a href="../Poosl-sig.stx/#DataMethod_19_5" id="DataMethod_28_14" title="Defined at ../Poosl-sig.stx line 19"><span class="token sort_Id">DataMethod</span></a></span> <span class="operator">-&gt;</span> <span class="cons_SimpleSort">StrategoLang-PreTerm</span></span>
    <span class="cons_OpDecl"><span id="ToTerm_29_5" title="Not referenced"><span class="token sort_Id">ToTerm</span></span> <span class="operator">:</span> <span class="cons_SimpleSort"><a href="../Poosl-sig.stx/#DataMethod_19_5" id="DataMethod_29_14" title="Defined at ../Poosl-sig.stx line 19"><span class="token sort_Id">DataMethod</span></a></span> <span class="operator">-&gt;</span> <span class="cons_SimpleSort">StrategoLang-PreTerm</span></span>
    <span class="cons_OpDecl"><span id="ToTerm_30_5" title="Not referenced"><span class="token sort_Id">ToTerm</span></span> <span class="operator">:</span> <span class="cons_SimpleSort"><a href="../Poosl-sig.stx/#ProcessMethod_32_5" id="ProcessMethod_30_14" title="Defined at ../Poosl-sig.stx line 32"><span class="token sort_Id">ProcessMethod</span></a></span> <span class="operator">-&gt;</span> <span class="cons_SimpleSort">StrategoLang-PreTerm</span></span>
    <span class="cons_OpDecl"><span id="ToTerm_31_5" title="Not referenced"><span class="token sort_Id">ToTerm</span></span> <span class="operator">:</span> <span class="cons_SimpleSort"><a href="../Poosl-sig.stx/#ProcessMethod_32_5" id="ProcessMethod_31_14" title="Defined at ../Poosl-sig.stx line 32"><span class="token sort_Id">ProcessMethod</span></a></span> <span class="operator">-&gt;</span> <span class="cons_SimpleSort">StrategoLang-PreTerm</span></span>
    <span class="cons_OpDecl"><span id="ToTerm_32_5" title="Not referenced"><span class="token sort_Id">ToTerm</span></span> <span class="operator">:</span> <span class="cons_SimpleSort"><a href="../Poosl-sig.stx/#Port_34_5" id="Port_32_14" title="Defined at ../Poosl-sig.stx line 34"><span class="token sort_Id">Port</span></a></span> <span class="operator">-&gt;</span> <span class="cons_SimpleSort">StrategoLang-PreTerm</span></span>
    <span class="cons_OpDecl"><span id="ToTerm_33_5" title="Not referenced"><span class="token sort_Id">ToTerm</span></span> <span class="operator">:</span> <span class="cons_SimpleSort"><a href="../Poosl-sig.stx/#Port_34_5" id="Port_33_14" title="Defined at ../Poosl-sig.stx line 34"><span class="token sort_Id">Port</span></a></span> <span class="operator">-&gt;</span> <span class="cons_SimpleSort">StrategoLang-PreTerm</span></span>
    <span class="cons_OpDecl"><span id="ToTerm_34_5" title="Not referenced"><span class="token sort_Id">ToTerm</span></span> <span class="operator">:</span> <span class="cons_SimpleSort"><a href="../Poosl-sig.stx/#MessageSignature_36_5" id="MessageSignature_34_14" title="Defined at ../Poosl-sig.stx line 36"><span class="token sort_Id">MessageSignature</span></a></span> <span class="operator">-&gt;</span> <span class="cons_SimpleSort">StrategoLang-PreTerm</span></span>
    <span class="cons_OpDecl"><span id="ToTerm_35_5" title="Not referenced"><span class="token sort_Id">ToTerm</span></span> <span class="operator">:</span> <span class="cons_SimpleSort"><a href="../Poosl-sig.stx/#MessageSignature_36_5" id="MessageSignature_35_14" title="Defined at ../Poosl-sig.stx line 36"><span class="token sort_Id">MessageSignature</span></a></span> <span class="operator">-&gt;</span> <span class="cons_SimpleSort">StrategoLang-PreTerm</span></span>
    <span class="cons_OpDecl"><span id="ToTerm_36_5" title="Not referenced"><span class="token sort_Id">ToTerm</span></span> <span class="operator">:</span> <span class="cons_SimpleSort"><a href="../Poosl-sig.stx/#Instance_39_5" id="Instance_36_14" title="Defined at ../Poosl-sig.stx line 39"><span class="token sort_Id">Instance</span></a></span> <span class="operator">-&gt;</span> <span class="cons_SimpleSort">StrategoLang-PreTerm</span></span>
    <span class="cons_OpDecl"><span id="ToTerm_37_5" title="Not referenced"><span class="token sort_Id">ToTerm</span></span> <span class="operator">:</span> <span class="cons_SimpleSort"><a href="../Poosl-sig.stx/#Instance_39_5" id="Instance_37_14" title="Defined at ../Poosl-sig.stx line 39"><span class="token sort_Id">Instance</span></a></span> <span class="operator">-&gt;</span> <span class="cons_SimpleSort">StrategoLang-PreTerm</span></span>
    <span class="cons_OpDecl"><span id="ToTerm_38_5" title="Not referenced"><span class="token sort_Id">ToTerm</span></span> <span class="operator">:</span> <span class="cons_SimpleSort"><a href="../Poosl-sig.stx/#Channel_43_5" id="Channel_38_14" title="Defined at ../Poosl-sig.stx line 43"><span class="token sort_Id">Channel</span></a></span> <span class="operator">-&gt;</span> <span class="cons_SimpleSort">StrategoLang-PreTerm</span></span>
    <span class="cons_OpDecl"><span id="ToTerm_39_5" title="Not referenced"><span class="token sort_Id">ToTerm</span></span> <span class="operator">:</span> <span class="cons_SimpleSort"><a href="../Poosl-sig.stx/#Channel_43_5" id="Channel_39_14" title="Defined at ../Poosl-sig.stx line 43"><span class="token sort_Id">Channel</span></a></span> <span class="operator">-&gt;</span> <span class="cons_SimpleSort">StrategoLang-PreTerm</span></span>
    <span class="cons_OpDecl"><span id="ToTerm_40_5" title="Not referenced"><span class="token sort_Id">ToTerm</span></span> <span class="operator">:</span> <span class="cons_SimpleSort"><a href="../Poosl-sig.stx/#PortInstance_44_5" id="PortInstance_40_14" title="Defined at ../Poosl-sig.stx line 44"><span class="token sort_Id">PortInstance</span></a></span> <span class="operator">-&gt;</span> <span class="cons_SimpleSort">StrategoLang-PreTerm</span></span>
    <span class="cons_OpDecl"><span id="ToTerm_41_5" title="Not referenced"><span class="token sort_Id">ToTerm</span></span> <span class="operator">:</span> <span class="cons_SimpleSort"><a href="../Poosl-sig.stx/#PortInstance_44_5" id="PortInstance_41_14" title="Defined at ../Poosl-sig.stx line 44"><span class="token sort_Id">PortInstance</span></a></span> <span class="operator">-&gt;</span> <span class="cons_SimpleSort">StrategoLang-PreTerm</span></span>
    <span class="cons_OpDecl"><span id="ToTerm_42_5" title="Not referenced"><span class="token sort_Id">ToTerm</span></span> <span class="operator">:</span> <span class="cons_SimpleSort"><a href="../Poosl-sig.stx/#Declaration_24_5" id="Declaration_42_14" title="Defined at ../Poosl-sig.stx line 24"><span class="token sort_Id">Declaration</span></a></span> <span class="operator">-&gt;</span> <span class="cons_SimpleSort">StrategoLang-PreTerm</span></span>
    <span class="cons_OpDecl"><span id="ToTerm_43_5" title="Not referenced"><span class="token sort_Id">ToTerm</span></span> <span class="operator">:</span> <span class="cons_SimpleSort"><a href="../Poosl-sig.stx/#Declaration_24_5" id="Declaration_43_14" title="Defined at ../Poosl-sig.stx line 24"><span class="token sort_Id">Declaration</span></a></span> <span class="operator">-&gt;</span> <span class="cons_SimpleSort">StrategoLang-PreTerm</span></span>
    <span class="cons_OpDecl"><span id="ToTerm_44_5" title="Not referenced"><span class="token sort_Id">ToTerm</span></span> <span class="operator">:</span> <span class="cons_SimpleSort"><a href="../ExprStat-sig.stx/#Statement_9_5" id="Statement_44_14" title="Defined at ../ExprStat-sig.stx line 9"><span class="token sort_Id">Statement</span></a></span> <span class="operator">-&gt;</span> <span class="cons_SimpleSort">StrategoLang-PreTerm</span></span>
    <span class="cons_OpDecl"><span id="ToTerm_45_5" title="Not referenced"><span class="token sort_Id">ToTerm</span></span> <span class="operator">:</span> <span class="cons_SimpleSort"><a href="../ExprStat-sig.stx/#Statement_9_5" id="Statement_45_14" title="Defined at ../ExprStat-sig.stx line 9"><span class="token sort_Id">Statement</span></a></span> <span class="operator">-&gt;</span> <span class="cons_SimpleSort">StrategoLang-PreTerm</span></span>
    <span class="cons_OpDecl"><span id="ToTerm_46_5" title="Not referenced"><span class="token sort_Id">ToTerm</span></span> <span class="operator">:</span> <span class="cons_SimpleSort"><a href="../ExprStat-sig.stx/#SingleStatement_10_5" id="SingleStatement_46_14" title="Defined at ../ExprStat-sig.stx line 10"><span class="token sort_Id">SingleStatement</span></a></span> <span class="operator">-&gt;</span> <span class="cons_SimpleSort">StrategoLang-PreTerm</span></span>
    <span class="cons_OpDecl"><span id="ToTerm_47_5" title="Not referenced"><span class="token sort_Id">ToTerm</span></span> <span class="operator">:</span> <span class="cons_SimpleSort"><a href="../ExprStat-sig.stx/#SingleStatement_10_5" id="SingleStatement_47_14" title="Defined at ../ExprStat-sig.stx line 10"><span class="token sort_Id">SingleStatement</span></a></span> <span class="operator">-&gt;</span> <span class="cons_SimpleSort">StrategoLang-PreTerm</span></span>
    <span class="cons_OpDecl"><span id="ToTerm_48_5" title="Not referenced"><span class="token sort_Id">ToTerm</span></span> <span class="operator">:</span> <span class="cons_SimpleSort"><a href="../ExprStat-sig.stx/#CaseStatement_15_5" id="CaseStatement_48_14" title="Defined at ../ExprStat-sig.stx line 15"><span class="token sort_Id">CaseStatement</span></a></span> <span class="operator">-&gt;</span> <span class="cons_SimpleSort">StrategoLang-PreTerm</span></span>
    <span class="cons_OpDecl"><span id="ToTerm_49_5" title="Not referenced"><span class="token sort_Id">ToTerm</span></span> <span class="operator">:</span> <span class="cons_SimpleSort"><a href="../ExprStat-sig.stx/#CaseStatement_15_5" id="CaseStatement_49_14" title="Defined at ../ExprStat-sig.stx line 15"><span class="token sort_Id">CaseStatement</span></a></span> <span class="operator">-&gt;</span> <span class="cons_SimpleSort">StrategoLang-PreTerm</span></span>
    <span class="cons_OpDecl"><span id="ToTerm_50_5" title="Not referenced"><span class="token sort_Id">ToTerm</span></span> <span class="operator">:</span> <span class="cons_SimpleSort"><a href="../ExprStat-sig.stx/#Expression_17_5" id="Expression_50_14" title="Defined at ../ExprStat-sig.stx line 17"><span class="token sort_Id">Expression</span></a></span> <span class="operator">-&gt;</span> <span class="cons_SimpleSort">StrategoLang-PreTerm</span></span>
    <span class="cons_OpDecl"><span id="ToTerm_51_5" title="Not referenced"><span class="token sort_Id">ToTerm</span></span> <span class="operator">:</span> <span class="cons_SimpleSort"><a href="../ExprStat-sig.stx/#Expression_17_5" id="Expression_51_14" title="Defined at ../ExprStat-sig.stx line 17"><span class="token sort_Id">Expression</span></a></span> <span class="operator">-&gt;</span> <span class="cons_SimpleSort">StrategoLang-PreTerm</span></span>
    <span class="cons_OpDecl"><span id="ToTerm_52_5" title="Not referenced"><span class="token sort_Id">ToTerm</span></span> <span class="operator">:</span> <span class="cons_SimpleSort"><a href="../ExprStat-sig.stx/#SingleExpression_18_5" id="SingleExpression_52_14" title="Defined at ../ExprStat-sig.stx line 18"><span class="token sort_Id">SingleExpression</span></a></span> <span class="operator">-&gt;</span> <span class="cons_SimpleSort">StrategoLang-PreTerm</span></span>
    <span class="cons_OpDecl"><span id="ToTerm_53_5" title="Not referenced"><span class="token sort_Id">ToTerm</span></span> <span class="operator">:</span> <span class="cons_SimpleSort"><a href="../ExprStat-sig.stx/#SingleExpression_18_5" id="SingleExpression_53_14" title="Defined at ../ExprStat-sig.stx line 18"><span class="token sort_Id">SingleExpression</span></a></span> <span class="operator">-&gt;</span> <span class="cons_SimpleSort">StrategoLang-PreTerm</span></span>
    <span class="cons_OpDecl"><span id="ToTerm_54_5" title="Not referenced"><span class="token sort_Id">ToTerm</span></span> <span class="operator">:</span> <span class="cons_SimpleSort"><a href="../ExprStat-sig.stx/#CaseExpression_24_5" id="CaseExpression_54_14" title="Defined at ../ExprStat-sig.stx line 24"><span class="token sort_Id">CaseExpression</span></a></span> <span class="operator">-&gt;</span> <span class="cons_SimpleSort">StrategoLang-PreTerm</span></span>
    <span class="cons_OpDecl"><span id="ToTerm_55_5" title="Not referenced"><span class="token sort_Id">ToTerm</span></span> <span class="operator">:</span> <span class="cons_SimpleSort"><a href="../ExprStat-sig.stx/#CaseExpression_24_5" id="CaseExpression_55_14" title="Defined at ../ExprStat-sig.stx line 24"><span class="token sort_Id">CaseExpression</span></a></span> <span class="operator">-&gt;</span> <span class="cons_SimpleSort">StrategoLang-PreTerm</span></span>
    <span class="cons_OpDecl"><span id="FromTerm_56_5" title="Not referenced"><span class="token sort_Id">FromTerm</span></span> <span class="operator">:</span> <span class="cons_SimpleSort">StrategoLang-Term</span> <span class="operator">-&gt;</span> <span class="cons_SimpleSort"><a href="../Poosl-sig.stx/#Poosl_10_5" id="Poosl_56_37" title="Defined at ../Poosl-sig.stx line 10"><span class="token sort_Id">Poosl</span></a></span></span>
    <span class="cons_OpDecl"><span id="FromTerm_57_5" title="Not referenced"><span class="token sort_Id">FromTerm</span></span> <span class="operator">:</span> <span class="cons_SimpleSort">StrategoLang-Term</span> <span class="operator">-&gt;</span> <span class="cons_SimpleSort"><a href="../Poosl-sig.stx/#Poosl_10_5" id="Poosl_57_37" title="Defined at ../Poosl-sig.stx line 10"><span class="token sort_Id">Poosl</span></a></span></span>
    <span class="cons_OpDecl"><span id="FromTerm_58_5" title="Not referenced"><span class="token sort_Id">FromTerm</span></span> <span class="operator">:</span> <span class="cons_SimpleSort">StrategoLang-Term</span> <span class="operator">-&gt;</span> <span class="cons_SimpleSort"><a href="../Poosl-sig.stx/#Import_12_5" id="Import_58_37" title="Defined at ../Poosl-sig.stx line 12"><span class="token sort_Id">Import</span></a></span></span>
    <span class="cons_OpDecl"><span id="FromTerm_59_5" title="Not referenced"><span class="token sort_Id">FromTerm</span></span> <span class="operator">:</span> <span class="cons_SimpleSort">StrategoLang-Term</span> <span class="operator">-&gt;</span> <span class="cons_SimpleSort"><a href="../Poosl-sig.stx/#Import_12_5" id="Import_59_37" title="Defined at ../Poosl-sig.stx line 12"><span class="token sort_Id">Import</span></a></span></span>
    <span class="cons_OpDecl"><span id="FromTerm_60_5" title="Not referenced"><span class="token sort_Id">FromTerm</span></span> <span class="operator">:</span> <span class="cons_SimpleSort">StrategoLang-Term</span> <span class="operator">-&gt;</span> <span class="cons_SimpleSort"><a href="../Poosl-sig.stx/#ImportList_11_5" id="ImportList_60_37" title="Defined at ../Poosl-sig.stx line 11"><span class="token sort_Id">ImportList</span></a></span></span>
    <span class="cons_OpDecl"><span id="FromTerm_61_5" title="Not referenced"><span class="token sort_Id">FromTerm</span></span> <span class="operator">:</span> <span class="cons_SimpleSort">StrategoLang-Term</span> <span class="operator">-&gt;</span> <span class="cons_SimpleSort"><a href="../Poosl-sig.stx/#ImportList_11_5" id="ImportList_61_37" title="Defined at ../Poosl-sig.stx line 11"><span class="token sort_Id">ImportList</span></a></span></span>
    <span class="cons_OpDecl"><span id="FromTerm_62_5" title="Not referenced"><span class="token sort_Id">FromTerm</span></span> <span class="operator">:</span> <span class="cons_SimpleSort">StrategoLang-Term</span> <span class="operator">-&gt;</span> <span class="cons_SimpleSort"><a href="../Poosl-sig.stx/#Annotation_14_5" id="Annotation_62_37" title="Defined at ../Poosl-sig.stx line 14"><span class="token sort_Id">Annotation</span></a></span></span>
    <span class="cons_OpDecl"><span id="FromTerm_63_5" title="Not referenced"><span class="token sort_Id">FromTerm</span></span> <span class="operator">:</span> <span class="cons_SimpleSort">StrategoLang-Term</span> <span class="operator">-&gt;</span> <span class="cons_SimpleSort"><a href="../Poosl-sig.stx/#Annotation_14_5" id="Annotation_63_37" title="Defined at ../Poosl-sig.stx line 14"><span class="token sort_Id">Annotation</span></a></span></span>
    <span class="cons_OpDecl"><span id="FromTerm_64_5" title="Not referenced"><span class="token sort_Id">FromTerm</span></span> <span class="operator">:</span> <span class="cons_SimpleSort">StrategoLang-Term</span> <span class="operator">-&gt;</span> <span class="cons_SimpleSort"><a href="../Poosl-sig.stx/#AnnotationList_13_5" id="AnnotationList_64_37" title="Defined at ../Poosl-sig.stx line 13"><span class="token sort_Id">AnnotationList</span></a></span></span>
    <span class="cons_OpDecl"><span id="FromTerm_65_5" title="Not referenced"><span class="token sort_Id">FromTerm</span></span> <span class="operator">:</span> <span class="cons_SimpleSort">StrategoLang-Term</span> <span class="operator">-&gt;</span> <span class="cons_SimpleSort"><a href="../Poosl-sig.stx/#AnnotationList_13_5" id="AnnotationList_65_37" title="Defined at ../Poosl-sig.stx line 13"><span class="token sort_Id">AnnotationList</span></a></span></span>
    <span class="cons_OpDecl"><span id="FromTerm_66_5" title="Not referenced"><span class="token sort_Id">FromTerm</span></span> <span class="operator">:</span> <span class="cons_SimpleSort">StrategoLang-Term</span> <span class="operator">-&gt;</span> <span class="cons_SimpleSort"><a href="../Poosl-sig.stx/#Class_16_5" id="Class_66_37" title="Defined at ../Poosl-sig.stx line 16"><span class="token sort_Id">Class</span></a></span></span>
    <span class="cons_OpDecl"><span id="FromTerm_67_5" title="Not referenced"><span class="token sort_Id">FromTerm</span></span> <span class="operator">:</span> <span class="cons_SimpleSort">StrategoLang-Term</span> <span class="operator">-&gt;</span> <span class="cons_SimpleSort"><a href="../Poosl-sig.stx/#Class_16_5" id="Class_67_37" title="Defined at ../Poosl-sig.stx line 16"><span class="token sort_Id">Class</span></a></span></span>
    <span class="cons_OpDecl"><span id="FromTerm_68_5" title="Not referenced"><span class="token sort_Id">FromTerm</span></span> <span class="operator">:</span> <span class="cons_SimpleSort">StrategoLang-Term</span> <span class="operator">-&gt;</span> <span class="cons_SimpleSort"><a href="../Poosl-sig.stx/#ClassList_17_5" id="ClassList_68_37" title="Defined at ../Poosl-sig.stx line 17"><span class="token sort_Id">ClassList</span></a></span></span>
    <span class="cons_OpDecl"><span id="FromTerm_69_5" title="Not referenced"><span class="token sort_Id">FromTerm</span></span> <span class="operator">:</span> <span class="cons_SimpleSort">StrategoLang-Term</span> <span class="operator">-&gt;</span> <span class="cons_SimpleSort"><a href="../Poosl-sig.stx/#ClassList_17_5" id="ClassList_69_37" title="Defined at ../Poosl-sig.stx line 17"><span class="token sort_Id">ClassList</span></a></span></span>
    <span class="cons_OpDecl"><span id="FromTerm_70_5" title="Not referenced"><span class="token sort_Id">FromTerm</span></span> <span class="operator">:</span> <span class="cons_SimpleSort">StrategoLang-Term</span> <span class="operator">-&gt;</span> <span class="cons_SimpleSort"><a href="../Poosl-sig.stx/#ExtendsClause_22_5" id="ExtendsClause_70_37" title="Defined at ../Poosl-sig.stx line 22"><span class="token sort_Id">ExtendsClause</span></a></span></span>
    <span class="cons_OpDecl"><span id="FromTerm_71_5" title="Not referenced"><span class="token sort_Id">FromTerm</span></span> <span class="operator">:</span> <span class="cons_SimpleSort">StrategoLang-Term</span> <span class="operator">-&gt;</span> <span class="cons_SimpleSort"><a href="../Poosl-sig.stx/#ExtendsClause_22_5" id="ExtendsClause_71_37" title="Defined at ../Poosl-sig.stx line 22"><span class="token sort_Id">ExtendsClause</span></a></span></span>
    <span class="cons_OpDecl"><span id="FromTerm_72_5" title="Not referenced"><span class="token sort_Id">FromTerm</span></span> <span class="operator">:</span> <span class="cons_SimpleSort">StrategoLang-Term</span> <span class="operator">-&gt;</span> <span class="cons_SimpleSort"><a href="../Poosl-sig.stx/#DataMethod_19_5" id="DataMethod_72_37" title="Defined at ../Poosl-sig.stx line 19"><span class="token sort_Id">DataMethod</span></a></span></span>
    <span class="cons_OpDecl"><span id="FromTerm_73_5" title="Not referenced"><span class="token sort_Id">FromTerm</span></span> <span class="operator">:</span> <span class="cons_SimpleSort">StrategoLang-Term</span> <span class="operator">-&gt;</span> <span class="cons_SimpleSort"><a href="../Poosl-sig.stx/#DataMethod_19_5" id="DataMethod_73_37" title="Defined at ../Poosl-sig.stx line 19"><span class="token sort_Id">DataMethod</span></a></span></span>
    <span class="cons_OpDecl"><span id="FromTerm_74_5" title="Not referenced"><span class="token sort_Id">FromTerm</span></span> <span class="operator">:</span> <span class="cons_SimpleSort">StrategoLang-Term</span> <span class="operator">-&gt;</span> <span class="cons_SimpleSort"><a href="../Poosl-sig.stx/#DataMethodList_18_5" id="DataMethodList_74_37" title="Defined at ../Poosl-sig.stx line 18"><span class="token sort_Id">DataMethodList</span></a></span></span>
    <span class="cons_OpDecl"><span id="FromTerm_75_5" title="Not referenced"><span class="token sort_Id">FromTerm</span></span> <span class="operator">:</span> <span class="cons_SimpleSort">StrategoLang-Term</span> <span class="operator">-&gt;</span> <span class="cons_SimpleSort"><a href="../Poosl-sig.stx/#DataMethodList_18_5" id="DataMethodList_75_37" title="Defined at ../Poosl-sig.stx line 18"><span class="token sort_Id">DataMethodList</span></a></span></span>
    <span class="cons_OpDecl"><span id="FromTerm_76_5" title="Not referenced"><span class="token sort_Id">FromTerm</span></span> <span class="operator">:</span> <span class="cons_SimpleSort">StrategoLang-Term</span> <span class="operator">-&gt;</span> <span class="cons_SimpleSort"><a href="../Poosl-sig.stx/#ProcessMethod_32_5" id="ProcessMethod_76_37" title="Defined at ../Poosl-sig.stx line 32"><span class="token sort_Id">ProcessMethod</span></a></span></span>
    <span class="cons_OpDecl"><span id="FromTerm_77_5" title="Not referenced"><span class="token sort_Id">FromTerm</span></span> <span class="operator">:</span> <span class="cons_SimpleSort">StrategoLang-Term</span> <span class="operator">-&gt;</span> <span class="cons_SimpleSort"><a href="../Poosl-sig.stx/#ProcessMethod_32_5" id="ProcessMethod_77_37" title="Defined at ../Poosl-sig.stx line 32"><span class="token sort_Id">ProcessMethod</span></a></span></span>
    <span class="cons_OpDecl"><span id="FromTerm_78_5" title="Not referenced"><span class="token sort_Id">FromTerm</span></span> <span class="operator">:</span> <span class="cons_SimpleSort">StrategoLang-Term</span> <span class="operator">-&gt;</span> <span class="cons_SimpleSort"><a href="../Poosl-sig.stx/#ProcessMethodList_31_5" id="ProcessMethodList_78_37" title="Defined at ../Poosl-sig.stx line 31"><span class="token sort_Id">ProcessMethodList</span></a></span></span>
    <span class="cons_OpDecl"><span id="FromTerm_79_5" title="Not referenced"><span class="token sort_Id">FromTerm</span></span> <span class="operator">:</span> <span class="cons_SimpleSort">StrategoLang-Term</span> <span class="operator">-&gt;</span> <span class="cons_SimpleSort"><a href="../Poosl-sig.stx/#ProcessMethodList_31_5" id="ProcessMethodList_79_37" title="Defined at ../Poosl-sig.stx line 31"><span class="token sort_Id">ProcessMethodList</span></a></span></span>
    <span class="cons_OpDecl"><span id="FromTerm_80_5" title="Not referenced"><span class="token sort_Id">FromTerm</span></span> <span class="operator">:</span> <span class="cons_SimpleSort">StrategoLang-Term</span> <span class="operator">-&gt;</span> <span class="cons_SimpleSort"><a href="../Common-sig.stx/#ID_8_5" id="ID_80_37" title="Defined at ../Common-sig.stx line 8"><span class="token sort_Id">ID</span></a></span></span>
    <span class="cons_OpDecl"><span id="FromTerm_81_5" title="Not referenced"><span class="token sort_Id">FromTerm</span></span> <span class="operator">:</span> <span class="cons_SimpleSort">StrategoLang-Term</span> <span class="operator">-&gt;</span> <span class="cons_SimpleSort"><a href="../Common-sig.stx/#ID_8_5" id="ID_81_37" title="Defined at ../Common-sig.stx line 8"><span class="token sort_Id">ID</span></a></span></span>
    <span class="cons_OpDecl"><span id="FromTerm_82_5" title="Not referenced"><span class="token sort_Id">FromTerm</span></span> <span class="operator">:</span> <span class="cons_SimpleSort">StrategoLang-Term</span> <span class="operator">-&gt;</span> <span class="cons_SimpleSort"><a href="../Poosl-sig.stx/#IDList_23_5" id="IDList_82_37" title="Defined at ../Poosl-sig.stx line 23"><span class="token sort_Id">IDList</span></a></span></span>
    <span class="cons_OpDecl"><span id="FromTerm_83_5" title="Not referenced"><span class="token sort_Id">FromTerm</span></span> <span class="operator">:</span> <span class="cons_SimpleSort">StrategoLang-Term</span> <span class="operator">-&gt;</span> <span class="cons_SimpleSort"><a href="../Poosl-sig.stx/#IDList_23_5" id="IDList_83_37" title="Defined at ../Poosl-sig.stx line 23"><span class="token sort_Id">IDList</span></a></span></span>
    <span class="cons_OpDecl"><span id="FromTerm_84_5" title="Not referenced"><span class="token sort_Id">FromTerm</span></span> <span class="operator">:</span> <span class="cons_SimpleSort">StrategoLang-Term</span> <span class="operator">-&gt;</span> <span class="cons_SimpleSort"><a href="../Poosl-sig.stx/#OptMessageParameterList_37_5" id="OptMessageParameterList_84_37" title="Defined at ../Poosl-sig.stx line 37"><span class="token sort_Id">OptMessageParameterList</span></a></span></span>
    <span class="cons_OpDecl"><span id="FromTerm_85_5" title="Not referenced"><span class="token sort_Id">FromTerm</span></span> <span class="operator">:</span> <span class="cons_SimpleSort">StrategoLang-Term</span> <span class="operator">-&gt;</span> <span class="cons_SimpleSort"><a href="../Poosl-sig.stx/#OptMessageParameterList_37_5" id="OptMessageParameterList_85_37" title="Defined at ../Poosl-sig.stx line 37"><span class="token sort_Id">OptMessageParameterList</span></a></span></span>
    <span class="cons_OpDecl"><span id="FromTerm_86_5" title="Not referenced"><span class="token sort_Id">FromTerm</span></span> <span class="operator">:</span> <span class="cons_SimpleSort">StrategoLang-Term</span> <span class="operator">-&gt;</span> <span class="cons_SimpleSort"><a href="../ExprStat-sig.stx/#OptVariableList_21_5" id="OptVariableList_86_37" title="Defined at ../ExprStat-sig.stx line 21"><span class="token sort_Id">OptVariableList</span></a></span></span>
    <span class="cons_OpDecl"><span id="FromTerm_87_5" title="Not referenced"><span class="token sort_Id">FromTerm</span></span> <span class="operator">:</span> <span class="cons_SimpleSort">StrategoLang-Term</span> <span class="operator">-&gt;</span> <span class="cons_SimpleSort"><a href="../ExprStat-sig.stx/#OptVariableList_21_5" id="OptVariableList_87_37" title="Defined at ../ExprStat-sig.stx line 21"><span class="token sort_Id">OptVariableList</span></a></span></span>
    <span class="cons_OpDecl"><span id="FromTerm_88_5" title="Not referenced"><span class="token sort_Id">FromTerm</span></span> <span class="operator">:</span> <span class="cons_SimpleSort">StrategoLang-Term</span> <span class="operator">-&gt;</span> <span class="cons_SimpleSort"><a href="../ExprStat-sig.stx/#VariableList_31_5" id="VariableList_88_37" title="Defined at ../ExprStat-sig.stx line 31"><span class="token sort_Id">VariableList</span></a></span></span>
    <span class="cons_OpDecl"><span id="FromTerm_89_5" title="Not referenced"><span class="token sort_Id">FromTerm</span></span> <span class="operator">:</span> <span class="cons_SimpleSort">StrategoLang-Term</span> <span class="operator">-&gt;</span> <span class="cons_SimpleSort"><a href="../ExprStat-sig.stx/#VariableList_31_5" id="VariableList_89_37" title="Defined at ../ExprStat-sig.stx line 31"><span class="token sort_Id">VariableList</span></a></span></span>
    <span class="cons_OpDecl"><span id="FromTerm_90_5" title="Not referenced"><span class="token sort_Id">FromTerm</span></span> <span class="operator">:</span> <span class="cons_SimpleSort">StrategoLang-Term</span> <span class="operator">-&gt;</span> <span class="cons_SimpleSort"><a href="../ExprStat-sig.stx/#UnaryOperator_27_5" id="UnaryOperator_90_37" title="Defined at ../ExprStat-sig.stx line 27"><span class="token sort_Id">UnaryOperator</span></a></span></span>
    <span class="cons_OpDecl"><span id="FromTerm_91_5" title="Not referenced"><span class="token sort_Id">FromTerm</span></span> <span class="operator">:</span> <span class="cons_SimpleSort">StrategoLang-Term</span> <span class="operator">-&gt;</span> <span class="cons_SimpleSort"><a href="../ExprStat-sig.stx/#UnaryOperator_27_5" id="UnaryOperator_91_37" title="Defined at ../ExprStat-sig.stx line 27"><span class="token sort_Id">UnaryOperator</span></a></span></span>
    <span class="cons_OpDecl"><span id="FromTerm_92_5" title="Not referenced"><span class="token sort_Id">FromTerm</span></span> <span class="operator">:</span> <span class="cons_SimpleSort">StrategoLang-Term</span> <span class="operator">-&gt;</span> <span class="cons_SimpleSort"><a href="../Poosl-sig.stx/#OperatorBinary_20_5" id="OperatorBinary_92_37" title="Defined at ../Poosl-sig.stx line 20"><span class="token sort_Id">OperatorBinary</span></a></span></span>
    <span class="cons_OpDecl"><span id="FromTerm_93_5" title="Not referenced"><span class="token sort_Id">FromTerm</span></span> <span class="operator">:</span> <span class="cons_SimpleSort">StrategoLang-Term</span> <span class="operator">-&gt;</span> <span class="cons_SimpleSort"><a href="../Poosl-sig.stx/#OperatorBinary_20_5" id="OperatorBinary_93_37" title="Defined at ../Poosl-sig.stx line 20"><span class="token sort_Id">OperatorBinary</span></a></span></span>
    <span class="cons_OpDecl"><span id="FromTerm_94_5" title="Not referenced"><span class="token sort_Id">FromTerm</span></span> <span class="operator">:</span> <span class="cons_SimpleSort">StrategoLang-Term</span> <span class="operator">-&gt;</span> <span class="cons_SimpleSort"><a href="../Poosl-sig.stx/#Declaration_24_5" id="Declaration_94_37" title="Defined at ../Poosl-sig.stx line 24"><span class="token sort_Id">Declaration</span></a></span></span>
    <span class="cons_OpDecl"><span id="FromTerm_95_5" title="Not referenced"><span class="token sort_Id">FromTerm</span></span> <span class="operator">:</span> <span class="cons_SimpleSort">StrategoLang-Term</span> <span class="operator">-&gt;</span> <span class="cons_SimpleSort"><a href="../Poosl-sig.stx/#Declaration_24_5" id="Declaration_95_37" title="Defined at ../Poosl-sig.stx line 24"><span class="token sort_Id">Declaration</span></a></span></span>
    <span class="cons_OpDecl"><span id="FromTerm_96_5" title="Not referenced"><span class="token sort_Id">FromTerm</span></span> <span class="operator">:</span> <span class="cons_SimpleSort">StrategoLang-Term</span> <span class="operator">-&gt;</span> <span class="cons_SimpleSort"><a href="../Poosl-sig.stx/#DeclarationOptComma_26_5" id="DeclarationOptComma_96_37" title="Defined at ../Poosl-sig.stx line 26"><span class="token sort_Id">DeclarationOptComma</span></a></span></span>
    <span class="cons_OpDecl"><span id="FromTerm_97_5" title="Not referenced"><span class="token sort_Id">FromTerm</span></span> <span class="operator">:</span> <span class="cons_SimpleSort">StrategoLang-Term</span> <span class="operator">-&gt;</span> <span class="cons_SimpleSort"><a href="../Poosl-sig.stx/#DeclarationOptComma_26_5" id="DeclarationOptComma_97_37" title="Defined at ../Poosl-sig.stx line 26"><span class="token sort_Id">DeclarationOptComma</span></a></span></span>
    <span class="cons_OpDecl"><span id="FromTerm_98_5" title="Not referenced"><span class="token sort_Id">FromTerm</span></span> <span class="operator">:</span> <span class="cons_SimpleSort">StrategoLang-Term</span> <span class="operator">-&gt;</span> <span class="cons_SimpleSort"><a href="../Poosl-sig.stx/#DeclarationOptCommaList_25_5" id="DeclarationOptCommaList_98_37" title="Defined at ../Poosl-sig.stx line 25"><span class="token sort_Id">DeclarationOptCommaList</span></a></span></span>
    <span class="cons_OpDecl"><span id="FromTerm_99_5" title="Not referenced"><span class="token sort_Id">FromTerm</span></span> <span class="operator">:</span> <span class="cons_SimpleSort">StrategoLang-Term</span> <span class="operator">-&gt;</span> <span class="cons_SimpleSort"><a href="../Poosl-sig.stx/#DeclarationOptCommaList_25_5" id="DeclarationOptCommaList_99_37" title="Defined at ../Poosl-sig.stx line 25"><span class="token sort_Id">DeclarationOptCommaList</span></a></span></span>
    <span class="cons_OpDecl"><span id="FromTerm_100_5" title="Not referenced"><span class="token sort_Id">FromTerm</span></span> <span class="operator">:</span> <span class="cons_SimpleSort">StrategoLang-Term</span> <span class="operator">-&gt;</span> <span class="cons_SimpleSort"><a href="../Poosl-sig.stx/#ParameterList_27_5" id="ParameterList_100_37" title="Defined at ../Poosl-sig.stx line 27"><span class="token sort_Id">ParameterList</span></a></span></span>
    <span class="cons_OpDecl"><span id="FromTerm_101_5" title="Not referenced"><span class="token sort_Id">FromTerm</span></span> <span class="operator">:</span> <span class="cons_SimpleSort">StrategoLang-Term</span> <span class="operator">-&gt;</span> <span class="cons_SimpleSort"><a href="../Poosl-sig.stx/#ParameterList_27_5" id="ParameterList_101_37" title="Defined at ../Poosl-sig.stx line 27"><span class="token sort_Id">ParameterList</span></a></span></span>
    <span class="cons_OpDecl"><span id="FromTerm_102_5" title="Not referenced"><span class="token sort_Id">FromTerm</span></span> <span class="operator">:</span> <span class="cons_SimpleSort">StrategoLang-Term</span> <span class="operator">-&gt;</span> <span class="cons_SimpleSort"><a href="../Poosl-sig.stx/#OptParameterList_29_5" id="OptParameterList_102_37" title="Defined at ../Poosl-sig.stx line 29"><span class="token sort_Id">OptParameterList</span></a></span></span>
    <span class="cons_OpDecl"><span id="FromTerm_103_5" title="Not referenced"><span class="token sort_Id">FromTerm</span></span> <span class="operator">:</span> <span class="cons_SimpleSort">StrategoLang-Term</span> <span class="operator">-&gt;</span> <span class="cons_SimpleSort"><a href="../Poosl-sig.stx/#OptParameterList_29_5" id="OptParameterList_103_37" title="Defined at ../Poosl-sig.stx line 29"><span class="token sort_Id">OptParameterList</span></a></span></span>
    <span class="cons_OpDecl"><span id="FromTerm_104_5" title="Not referenced"><span class="token sort_Id">FromTerm</span></span> <span class="operator">:</span> <span class="cons_SimpleSort">StrategoLang-Term</span> <span class="operator">-&gt;</span> <span class="cons_SimpleSort"><a href="../Poosl-sig.stx/#OptLocalVariableList_30_5" id="OptLocalVariableList_104_37" title="Defined at ../Poosl-sig.stx line 30"><span class="token sort_Id">OptLocalVariableList</span></a></span></span>
    <span class="cons_OpDecl"><span id="FromTerm_105_5" title="Not referenced"><span class="token sort_Id">FromTerm</span></span> <span class="operator">:</span> <span class="cons_SimpleSort">StrategoLang-Term</span> <span class="operator">-&gt;</span> <span class="cons_SimpleSort"><a href="../Poosl-sig.stx/#OptLocalVariableList_30_5" id="OptLocalVariableList_105_37" title="Defined at ../Poosl-sig.stx line 30"><span class="token sort_Id">OptLocalVariableList</span></a></span></span>
    <span class="cons_OpDecl"><span id="FromTerm_106_5" title="Not referenced"><span class="token sort_Id">FromTerm</span></span> <span class="operator">:</span> <span class="cons_SimpleSort">StrategoLang-Term</span> <span class="operator">-&gt;</span> <span class="cons_SimpleSort"><a href="../Poosl-sig.stx/#OptEmptyList_28_5" id="OptEmptyList_106_37" title="Defined at ../Poosl-sig.stx line 28"><span class="token sort_Id">OptEmptyList</span></a></span></span>
    <span class="cons_OpDecl"><span id="FromTerm_107_5" title="Not referenced"><span class="token sort_Id">FromTerm</span></span> <span class="operator">:</span> <span class="cons_SimpleSort">StrategoLang-Term</span> <span class="operator">-&gt;</span> <span class="cons_SimpleSort"><a href="../Poosl-sig.stx/#OptEmptyList_28_5" id="OptEmptyList_107_37" title="Defined at ../Poosl-sig.stx line 28"><span class="token sort_Id">OptEmptyList</span></a></span></span>
    <span class="cons_OpDecl"><span id="FromTerm_108_5" title="Not referenced"><span class="token sort_Id">FromTerm</span></span> <span class="operator">:</span> <span class="cons_SimpleSort">StrategoLang-Term</span> <span class="operator">-&gt;</span> <span class="cons_SimpleSort"><a href="../Poosl-sig.stx/#Port_34_5" id="Port_108_37" title="Defined at ../Poosl-sig.stx line 34"><span class="token sort_Id">Port</span></a></span></span>
    <span class="cons_OpDecl"><span id="FromTerm_109_5" title="Not referenced"><span class="token sort_Id">FromTerm</span></span> <span class="operator">:</span> <span class="cons_SimpleSort">StrategoLang-Term</span> <span class="operator">-&gt;</span> <span class="cons_SimpleSort"><a href="../Poosl-sig.stx/#Port_34_5" id="Port_109_37" title="Defined at ../Poosl-sig.stx line 34"><span class="token sort_Id">Port</span></a></span></span>
    <span class="cons_OpDecl"><span id="FromTerm_110_5" title="Not referenced"><span class="token sort_Id">FromTerm</span></span> <span class="operator">:</span> <span class="cons_SimpleSort">StrategoLang-Term</span> <span class="operator">-&gt;</span> <span class="cons_SimpleSort"><a href="../Poosl-sig.stx/#PortList_33_5" id="PortList_110_37" title="Defined at ../Poosl-sig.stx line 33"><span class="token sort_Id">PortList</span></a></span></span>
    <span class="cons_OpDecl"><span id="FromTerm_111_5" title="Not referenced"><span class="token sort_Id">FromTerm</span></span> <span class="operator">:</span> <span class="cons_SimpleSort">StrategoLang-Term</span> <span class="operator">-&gt;</span> <span class="cons_SimpleSort"><a href="../Poosl-sig.stx/#PortList_33_5" id="PortList_111_37" title="Defined at ../Poosl-sig.stx line 33"><span class="token sort_Id">PortList</span></a></span></span>
    <span class="cons_OpDecl"><span id="FromTerm_112_5" title="Not referenced"><span class="token sort_Id">FromTerm</span></span> <span class="operator">:</span> <span class="cons_SimpleSort">StrategoLang-Term</span> <span class="operator">-&gt;</span> <span class="cons_SimpleSort"><a href="../Poosl-sig.stx/#MessageSignature_36_5" id="MessageSignature_112_37" title="Defined at ../Poosl-sig.stx line 36"><span class="token sort_Id">MessageSignature</span></a></span></span>
    <span class="cons_OpDecl"><span id="FromTerm_113_5" title="Not referenced"><span class="token sort_Id">FromTerm</span></span> <span class="operator">:</span> <span class="cons_SimpleSort">StrategoLang-Term</span> <span class="operator">-&gt;</span> <span class="cons_SimpleSort"><a href="../Poosl-sig.stx/#MessageSignature_36_5" id="MessageSignature_113_37" title="Defined at ../Poosl-sig.stx line 36"><span class="token sort_Id">MessageSignature</span></a></span></span>
    <span class="cons_OpDecl"><span id="FromTerm_114_5" title="Not referenced"><span class="token sort_Id">FromTerm</span></span> <span class="operator">:</span> <span class="cons_SimpleSort">StrategoLang-Term</span> <span class="operator">-&gt;</span> <span class="cons_SimpleSort"><a href="../Poosl-sig.stx/#MessageSignatureList_35_5" id="MessageSignatureList_114_37" title="Defined at ../Poosl-sig.stx line 35"><span class="token sort_Id">MessageSignatureList</span></a></span></span>
    <span class="cons_OpDecl"><span id="FromTerm_115_5" title="Not referenced"><span class="token sort_Id">FromTerm</span></span> <span class="operator">:</span> <span class="cons_SimpleSort">StrategoLang-Term</span> <span class="operator">-&gt;</span> <span class="cons_SimpleSort"><a href="../Poosl-sig.stx/#MessageSignatureList_35_5" id="MessageSignatureList_115_37" title="Defined at ../Poosl-sig.stx line 35"><span class="token sort_Id">MessageSignatureList</span></a></span></span>
    <span class="cons_OpDecl"><span id="FromTerm_116_5" title="Not referenced"><span class="token sort_Id">FromTerm</span></span> <span class="operator">:</span> <span class="cons_SimpleSort">StrategoLang-Term</span> <span class="operator">-&gt;</span> <span class="cons_SimpleSort"><a href="../Poosl-sig.stx/#Instance_39_5" id="Instance_116_37" title="Defined at ../Poosl-sig.stx line 39"><span class="token sort_Id">Instance</span></a></span></span>
    <span class="cons_OpDecl"><span id="FromTerm_117_5" title="Not referenced"><span class="token sort_Id">FromTerm</span></span> <span class="operator">:</span> <span class="cons_SimpleSort">StrategoLang-Term</span> <span class="operator">-&gt;</span> <span class="cons_SimpleSort"><a href="../Poosl-sig.stx/#Instance_39_5" id="Instance_117_37" title="Defined at ../Poosl-sig.stx line 39"><span class="token sort_Id">Instance</span></a></span></span>
    <span class="cons_OpDecl"><span id="FromTerm_118_5" title="Not referenced"><span class="token sort_Id">FromTerm</span></span> <span class="operator">:</span> <span class="cons_SimpleSort">StrategoLang-Term</span> <span class="operator">-&gt;</span> <span class="cons_SimpleSort"><a href="../Poosl-sig.stx/#InstanceList_38_5" id="InstanceList_118_37" title="Defined at ../Poosl-sig.stx line 38"><span class="token sort_Id">InstanceList</span></a></span></span>
    <span class="cons_OpDecl"><span id="FromTerm_119_5" title="Not referenced"><span class="token sort_Id">FromTerm</span></span> <span class="operator">:</span> <span class="cons_SimpleSort">StrategoLang-Term</span> <span class="operator">-&gt;</span> <span class="cons_SimpleSort"><a href="../Poosl-sig.stx/#InstanceList_38_5" id="InstanceList_119_37" title="Defined at ../Poosl-sig.stx line 38"><span class="token sort_Id">InstanceList</span></a></span></span>
    <span class="cons_OpDecl"><span id="FromTerm_120_5" title="Not referenced"><span class="token sort_Id">FromTerm</span></span> <span class="operator">:</span> <span class="cons_SimpleSort">StrategoLang-Term</span> <span class="operator">-&gt;</span> <span class="cons_SimpleSort"><a href="../Poosl-sig.stx/#Channel_43_5" id="Channel_120_37" title="Defined at ../Poosl-sig.stx line 43"><span class="token sort_Id">Channel</span></a></span></span>
    <span class="cons_OpDecl"><span id="FromTerm_121_5" title="Not referenced"><span class="token sort_Id">FromTerm</span></span> <span class="operator">:</span> <span class="cons_SimpleSort">StrategoLang-Term</span> <span class="operator">-&gt;</span> <span class="cons_SimpleSort"><a href="../Poosl-sig.stx/#Channel_43_5" id="Channel_121_37" title="Defined at ../Poosl-sig.stx line 43"><span class="token sort_Id">Channel</span></a></span></span>
    <span class="cons_OpDecl"><span id="FromTerm_122_5" title="Not referenced"><span class="token sort_Id">FromTerm</span></span> <span class="operator">:</span> <span class="cons_SimpleSort">StrategoLang-Term</span> <span class="operator">-&gt;</span> <span class="cons_SimpleSort"><a href="../Poosl-sig.stx/#ChannelList_42_5" id="ChannelList_122_37" title="Defined at ../Poosl-sig.stx line 42"><span class="token sort_Id">ChannelList</span></a></span></span>
    <span class="cons_OpDecl"><span id="FromTerm_123_5" title="Not referenced"><span class="token sort_Id">FromTerm</span></span> <span class="operator">:</span> <span class="cons_SimpleSort">StrategoLang-Term</span> <span class="operator">-&gt;</span> <span class="cons_SimpleSort"><a href="../Poosl-sig.stx/#ChannelList_42_5" id="ChannelList_123_37" title="Defined at ../Poosl-sig.stx line 42"><span class="token sort_Id">ChannelList</span></a></span></span>
    <span class="cons_OpDecl"><span id="FromTerm_124_5" title="Not referenced"><span class="token sort_Id">FromTerm</span></span> <span class="operator">:</span> <span class="cons_SimpleSort">StrategoLang-Term</span> <span class="operator">-&gt;</span> <span class="cons_SimpleSort"><a href="../Poosl-sig.stx/#InstanceParameter_41_5" id="InstanceParameter_124_37" title="Defined at ../Poosl-sig.stx line 41"><span class="token sort_Id">InstanceParameter</span></a></span></span>
    <span class="cons_OpDecl"><span id="FromTerm_125_5" title="Not referenced"><span class="token sort_Id">FromTerm</span></span> <span class="operator">:</span> <span class="cons_SimpleSort">StrategoLang-Term</span> <span class="operator">-&gt;</span> <span class="cons_SimpleSort"><a href="../Poosl-sig.stx/#InstanceParameter_41_5" id="InstanceParameter_125_37" title="Defined at ../Poosl-sig.stx line 41"><span class="token sort_Id">InstanceParameter</span></a></span></span>
    <span class="cons_OpDecl"><span id="FromTerm_126_5" title="Not referenced"><span class="token sort_Id">FromTerm</span></span> <span class="operator">:</span> <span class="cons_SimpleSort">StrategoLang-Term</span> <span class="operator">-&gt;</span> <span class="cons_SimpleSort"><a href="../Poosl-sig.stx/#OptInstanceParameterList_40_5" id="OptInstanceParameterList_126_37" title="Defined at ../Poosl-sig.stx line 40"><span class="token sort_Id">OptInstanceParameterList</span></a></span></span>
    <span class="cons_OpDecl"><span id="FromTerm_127_5" title="Not referenced"><span class="token sort_Id">FromTerm</span></span> <span class="operator">:</span> <span class="cons_SimpleSort">StrategoLang-Term</span> <span class="operator">-&gt;</span> <span class="cons_SimpleSort"><a href="../Poosl-sig.stx/#OptInstanceParameterList_40_5" id="OptInstanceParameterList_127_37" title="Defined at ../Poosl-sig.stx line 40"><span class="token sort_Id">OptInstanceParameterList</span></a></span></span>
    <span class="cons_OpDecl"><span id="FromTerm_128_5" title="Not referenced"><span class="token sort_Id">FromTerm</span></span> <span class="operator">:</span> <span class="cons_SimpleSort">StrategoLang-Term</span> <span class="operator">-&gt;</span> <span class="cons_SimpleSort"><a href="../Poosl-sig.stx/#PortInstance_44_5" id="PortInstance_128_37" title="Defined at ../Poosl-sig.stx line 44"><span class="token sort_Id">PortInstance</span></a></span></span>
    <span class="cons_OpDecl"><span id="FromTerm_129_5" title="Not referenced"><span class="token sort_Id">FromTerm</span></span> <span class="operator">:</span> <span class="cons_SimpleSort">StrategoLang-Term</span> <span class="operator">-&gt;</span> <span class="cons_SimpleSort"><a href="../Poosl-sig.stx/#PortInstance_44_5" id="PortInstance_129_37" title="Defined at ../Poosl-sig.stx line 44"><span class="token sort_Id">PortInstance</span></a></span></span>
    <span class="cons_OpDecl"><span id="FromTerm_130_5" title="Not referenced"><span class="token sort_Id">FromTerm</span></span> <span class="operator">:</span> <span class="cons_SimpleSort">StrategoLang-Term</span> <span class="operator">-&gt;</span> <span class="cons_SimpleSort"><a href="../ExprStat-sig.stx/#Statement_9_5" id="Statement_130_37" title="Defined at ../ExprStat-sig.stx line 9"><span class="token sort_Id">Statement</span></a></span></span>
    <span class="cons_OpDecl"><span id="FromTerm_131_5" title="Not referenced"><span class="token sort_Id">FromTerm</span></span> <span class="operator">:</span> <span class="cons_SimpleSort">StrategoLang-Term</span> <span class="operator">-&gt;</span> <span class="cons_SimpleSort"><a href="../ExprStat-sig.stx/#Statement_9_5" id="Statement_131_37" title="Defined at ../ExprStat-sig.stx line 9"><span class="token sort_Id">Statement</span></a></span></span>
    <span class="cons_OpDecl"><span id="FromTerm_132_5" title="Not referenced"><span class="token sort_Id">FromTerm</span></span> <span class="operator">:</span> <span class="cons_SimpleSort">StrategoLang-Term</span> <span class="operator">-&gt;</span> <span class="cons_SimpleSort"><a href="../ExprStat-sig.stx/#SingleStatement_10_5" id="SingleStatement_132_37" title="Defined at ../ExprStat-sig.stx line 10"><span class="token sort_Id">SingleStatement</span></a></span></span>
    <span class="cons_OpDecl"><span id="FromTerm_133_5" title="Not referenced"><span class="token sort_Id">FromTerm</span></span> <span class="operator">:</span> <span class="cons_SimpleSort">StrategoLang-Term</span> <span class="operator">-&gt;</span> <span class="cons_SimpleSort"><a href="../ExprStat-sig.stx/#SingleStatement_10_5" id="SingleStatement_133_37" title="Defined at ../ExprStat-sig.stx line 10"><span class="token sort_Id">SingleStatement</span></a></span></span>
    <span class="cons_OpDecl"><span id="FromTerm_134_5" title="Not referenced"><span class="token sort_Id">FromTerm</span></span> <span class="operator">:</span> <span class="cons_SimpleSort">StrategoLang-Term</span> <span class="operator">-&gt;</span> <span class="cons_SimpleSort"><a href="../ExprStat-sig.stx/#CaseStatement_15_5" id="CaseStatement_134_37" title="Defined at ../ExprStat-sig.stx line 15"><span class="token sort_Id">CaseStatement</span></a></span></span>
    <span class="cons_OpDecl"><span id="FromTerm_135_5" title="Not referenced"><span class="token sort_Id">FromTerm</span></span> <span class="operator">:</span> <span class="cons_SimpleSort">StrategoLang-Term</span> <span class="operator">-&gt;</span> <span class="cons_SimpleSort"><a href="../ExprStat-sig.stx/#CaseStatement_15_5" id="CaseStatement_135_37" title="Defined at ../ExprStat-sig.stx line 15"><span class="token sort_Id">CaseStatement</span></a></span></span>
    <span class="cons_OpDecl"><span id="FromTerm_136_5" title="Not referenced"><span class="token sort_Id">FromTerm</span></span> <span class="operator">:</span> <span class="cons_SimpleSort">StrategoLang-Term</span> <span class="operator">-&gt;</span> <span class="cons_SimpleSort"><a href="../ExprStat-sig.stx/#CaseStatementList_14_5" id="CaseStatementList_136_37" title="Defined at ../ExprStat-sig.stx line 14"><span class="token sort_Id">CaseStatementList</span></a></span></span>
    <span class="cons_OpDecl"><span id="FromTerm_137_5" title="Not referenced"><span class="token sort_Id">FromTerm</span></span> <span class="operator">:</span> <span class="cons_SimpleSort">StrategoLang-Term</span> <span class="operator">-&gt;</span> <span class="cons_SimpleSort"><a href="../ExprStat-sig.stx/#CaseStatementList_14_5" id="CaseStatementList_137_37" title="Defined at ../ExprStat-sig.stx line 14"><span class="token sort_Id">CaseStatementList</span></a></span></span>
    <span class="cons_OpDecl"><span id="FromTerm_138_5" title="Not referenced"><span class="token sort_Id">FromTerm</span></span> <span class="operator">:</span> <span class="cons_SimpleSort">StrategoLang-Term</span> <span class="operator">-&gt;</span> <span class="cons_SimpleSort"><a href="../ExprStat-sig.stx/#Expression_17_5" id="Expression_138_37" title="Defined at ../ExprStat-sig.stx line 17"><span class="token sort_Id">Expression</span></a></span></span>
    <span class="cons_OpDecl"><span id="FromTerm_139_5" title="Not referenced"><span class="token sort_Id">FromTerm</span></span> <span class="operator">:</span> <span class="cons_SimpleSort">StrategoLang-Term</span> <span class="operator">-&gt;</span> <span class="cons_SimpleSort"><a href="../ExprStat-sig.stx/#Expression_17_5" id="Expression_139_37" title="Defined at ../ExprStat-sig.stx line 17"><span class="token sort_Id">Expression</span></a></span></span>
    <span class="cons_OpDecl"><span id="FromTerm_140_5" title="Not referenced"><span class="token sort_Id">FromTerm</span></span> <span class="operator">:</span> <span class="cons_SimpleSort">StrategoLang-Term</span> <span class="operator">-&gt;</span> <span class="cons_SimpleSort"><a href="../ExprStat-sig.stx/#SingleExpression_18_5" id="SingleExpression_140_37" title="Defined at ../ExprStat-sig.stx line 18"><span class="token sort_Id">SingleExpression</span></a></span></span>
    <span class="cons_OpDecl"><span id="FromTerm_141_5" title="Not referenced"><span class="token sort_Id">FromTerm</span></span> <span class="operator">:</span> <span class="cons_SimpleSort">StrategoLang-Term</span> <span class="operator">-&gt;</span> <span class="cons_SimpleSort"><a href="../ExprStat-sig.stx/#SingleExpression_18_5" id="SingleExpression_141_37" title="Defined at ../ExprStat-sig.stx line 18"><span class="token sort_Id">SingleExpression</span></a></span></span>
    <span class="cons_OpDecl"><span id="FromTerm_142_5" title="Not referenced"><span class="token sort_Id">FromTerm</span></span> <span class="operator">:</span> <span class="cons_SimpleSort">StrategoLang-Term</span> <span class="operator">-&gt;</span> <span class="cons_SimpleSort"><a href="../ExprStat-sig.stx/#CaseExpression_24_5" id="CaseExpression_142_37" title="Defined at ../ExprStat-sig.stx line 24"><span class="token sort_Id">CaseExpression</span></a></span></span>
    <span class="cons_OpDecl"><span id="FromTerm_143_5" title="Not referenced"><span class="token sort_Id">FromTerm</span></span> <span class="operator">:</span> <span class="cons_SimpleSort">StrategoLang-Term</span> <span class="operator">-&gt;</span> <span class="cons_SimpleSort"><a href="../ExprStat-sig.stx/#CaseExpression_24_5" id="CaseExpression_143_37" title="Defined at ../ExprStat-sig.stx line 24"><span class="token sort_Id">CaseExpression</span></a></span></span>
    <span class="cons_OpDecl"><span id="FromTerm_144_5" title="Not referenced"><span class="token sort_Id">FromTerm</span></span> <span class="operator">:</span> <span class="cons_SimpleSort">StrategoLang-Term</span> <span class="operator">-&gt;</span> <span class="cons_SimpleSort"><a href="../ExprStat-sig.stx/#CaseExpressionList_23_5" id="CaseExpressionList_144_37" title="Defined at ../ExprStat-sig.stx line 23"><span class="token sort_Id">CaseExpressionList</span></a></span></span>
    <span class="cons_OpDecl"><span id="FromTerm_145_5" title="Not referenced"><span class="token sort_Id">FromTerm</span></span> <span class="operator">:</span> <span class="cons_SimpleSort">StrategoLang-Term</span> <span class="operator">-&gt;</span> <span class="cons_SimpleSort"><a href="../ExprStat-sig.stx/#CaseExpressionList_23_5" id="CaseExpressionList_145_37" title="Defined at ../ExprStat-sig.stx line 23"><span class="token sort_Id">CaseExpressionList</span></a></span></span>
    <span class="cons_OpDecl"><span id="FromTerm_146_5" title="Not referenced"><span class="token sort_Id">FromTerm</span></span> <span class="operator">:</span> <span class="cons_SimpleSort">StrategoLang-Term</span> <span class="operator">-&gt;</span> <span class="cons_SimpleSort"><a href="../Common-sig.stx/#BOOL_10_5" id="BOOL_146_37" title="Defined at ../Common-sig.stx line 10"><span class="token sort_Id">BOOL</span></a></span></span>
    <span class="cons_OpDecl"><span id="FromTerm_147_5" title="Not referenced"><span class="token sort_Id">FromTerm</span></span> <span class="operator">:</span> <span class="cons_SimpleSort">StrategoLang-Term</span> <span class="operator">-&gt;</span> <span class="cons_SimpleSort"><a href="../Common-sig.stx/#CHARACTER_23_5" id="CHARACTER_147_37" title="Defined at ../Common-sig.stx line 23"><span class="token sort_Id">CHARACTER</span></a></span></span>
    <span class="cons_OpDecl"><span id="FromTerm_148_5" title="Not referenced"><span class="token sort_Id">FromTerm</span></span> <span class="operator">:</span> <span class="cons_SimpleSort">StrategoLang-Term</span> <span class="operator">-&gt;</span> <span class="cons_SimpleSort"><a href="../Common-sig.stx/#FLOAT_13_5" id="FLOAT_148_37" title="Defined at ../Common-sig.stx line 13"><span class="token sort_Id">FLOAT</span></a></span></span>
    <span class="cons_OpDecl"><span id="FromTerm_149_5" title="Not referenced"><span class="token sort_Id">FromTerm</span></span> <span class="operator">:</span> <span class="cons_SimpleSort">StrategoLang-Term</span> <span class="operator">-&gt;</span> <span class="cons_SimpleSort"><a href="../Common-sig.stx/#INT_11_5" id="INT_149_37" title="Defined at ../Common-sig.stx line 11"><span class="token sort_Id">INT</span></a></span></span>
    <span class="cons_OpDecl"><span id="FromTerm_150_5" title="Not referenced"><span class="token sort_Id">FromTerm</span></span> <span class="operator">:</span> <span class="cons_SimpleSort">StrategoLang-Term</span> <span class="operator">-&gt;</span> <span class="cons_SimpleSort"><a href="../Common-sig.stx/#REAL_12_5" id="REAL_150_37" title="Defined at ../Common-sig.stx line 12"><span class="token sort_Id">REAL</span></a></span></span>
    <span class="cons_OpDecl"><span id="FromTerm_151_5" title="Not referenced"><span class="token sort_Id">FromTerm</span></span> <span class="operator">:</span> <span class="cons_SimpleSort">StrategoLang-Term</span> <span class="operator">-&gt;</span> <span class="cons_SimpleSort"><a href="../Common-sig.stx/#STRING_22_5" id="STRING_151_37" title="Defined at ../Common-sig.stx line 22"><span class="token sort_Id">STRING</span></a></span></span>
</code></pre></td></tr></tbody></table></div>

<div id="modal">
  <div id="modal-content">
    <span id="modal-close">&times;</span>
    <h2 id="modal-h2"></h2>
    <p  id="modal-p"></p>
    <ul id="modal-ul"></ul>
  </div>
</div>
