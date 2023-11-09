---
title: Common.sdf3
hide:
  - toc
---

# `Common.sdf3`

:simple-github: [pdmosses/metaborg-poosl/org.metaborg.lang.poosl/syntax/Common.sdf3]

[pdmosses/metaborg-poosl/org.metaborg.lang.poosl/syntax/Common.sdf3]: https://github.com/pdmosses/metaborg-poosl/blob/master/org.metaborg.lang.poosl/syntax/Common.sdf3 "The source file on GitHub"

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
</pre></div></td>
<td class="code"><pre><code><span class="keyword">module</span> <button class="modal-open" id="Common_1_8" title="Multi-file references" data-urls="../ExprStat.sdf3/#Common_4_5 line 4; ../Poosl.sdf3/#Common_4_5 line 4">Common</button>

<span class="layout">// --- ID -------</span>

<span class="keyword">lexical sorts</span>
  <a href="#ID_11_3" id="ID_6_3" title="Referenced at line 11">ID</a> <a href="../ExprStat.sdf3/#ENV_186_53" id="ENV_6_6" title="Referenced at ../ExprStat.sdf3 line 186">ENV</a>
<span class="keyword">lexical syntax</span>
  <a href="#ID_11_3" id="ID_8_3" title="Referenced at line 11">ID</a>  = [<span class="cons_Regular">a</span>-<span class="cons_Regular">z</span><span class="cons_Regular">A</span>-<span class="cons_Regular">Z</span>] [<span class="cons_Regular">a</span>-<span class="cons_Regular">z</span><span class="cons_Regular">A</span>-<span class="cons_Regular">Z</span><span class="cons_Regular">0</span>-<span class="cons_Regular">9</span>\_]*
  <a href="../ExprStat.sdf3/#ENV_186_53" id="ENV_9_3" title="Referenced at ../ExprStat.sdf3 line 186">ENV</a> = <span class="cons_Lit">"${"</span> [<span class="cons_Regular">a</span>-<span class="cons_Regular">z</span><span class="cons_Regular">A</span>-<span class="cons_Regular">Z</span><span class="cons_Regular">0</span>-<span class="cons_Regular">9</span>\_]+ <span class="cons_Lit">"}"</span>
<span class="keyword">lexical restrictions</span>
  <a href="#ID_6_3" id="ID_11_3" title="Defined at line 6, 8, 22, 23, 48, 49">ID</a>  -/- [<span class="cons_Regular">a</span>-<span class="cons_Regular">z</span><span class="cons_Regular">A</span>-<span class="cons_Regular">Z</span><span class="cons_Regular">0</span>-<span class="cons_Regular">9</span>\_]


<span class="layout">// --- BOOLEANS -------</span>

<span class="keyword">lexical sorts</span>
  <a href="../ExprStat.sdf3/#BOOL_179_53" id="BOOL_17_3" title="Referenced at ../ExprStat.sdf3 line 179">BOOL</a>
<span class="keyword">lexical syntax</span>
  <a href="../ExprStat.sdf3/#BOOL_179_53" id="BOOL_19_3" title="Referenced at ../ExprStat.sdf3 line 179">BOOL</a> = <span class="cons_Lit">"false"</span>
  <a href="../ExprStat.sdf3/#BOOL_179_53" id="BOOL_20_3" title="Referenced at ../ExprStat.sdf3 line 179">BOOL</a> = <span class="cons_Lit">"true"</span>
<span class="keyword">lexical syntax</span>
  <a href="#ID_11_3" id="ID_22_3" title="Referenced at line 11">ID</a>   = <span class="cons_Lit">"false"</span> {<span class="keyword">reject</span>}
  <a href="#ID_11_3" id="ID_23_3" title="Referenced at line 11">ID</a>   = <span class="cons_Lit">"true"</span> {<span class="keyword">reject</span>}


<span class="layout">// --- NUMBERS -------</span>

<span class="keyword">lexical sorts</span>
  <a href="../ExprStat.sdf3/#INT_182_53" id="INT_29_3" title="Referenced at ../ExprStat.sdf3 line 182">INT</a> <button class="modal-open" id="REAL_29_7" title="Multi-file references" data-urls="#REAL_51_3 line 51; ../ExprStat.sdf3/#REAL_184_53 line 184">REAL</button> <a href="../ExprStat.sdf3/#FLOAT_181_53" id="FLOAT_29_12" title="Referenced at ../ExprStat.sdf3 line 181">FLOAT</a>
  <a href="#EXP_33_51" id="EXP_30_3" title="Referenced at line 33, 34, 35">EXP</a> <a href="#REAL_CORE_NE_34_27" id="REAL_CORE_NE_30_7" title="Referenced at line 34, 35, 52">REAL_CORE_NE</a> <a href="#INT_CORE_NE_33_27" id="INT_CORE_NE_30_20" title="Referenced at line 33, 53">INT_CORE_NE</a>
  <a href="#REAL_CORE_34_43" id="REAL_CORE_31_3" title="Referenced at line 34, 35, 38">REAL_CORE</a> <a href="#INT_CORE_33_42" id="INT_CORE_31_13" title="Referenced at line 33, 39, 41">INT_CORE</a> <a href="#BIN_CORE_33_58" id="BIN_CORE_31_22" title="Referenced at line 33">BIN_CORE</a> <a href="#HEX_CORE_33_69" id="HEX_CORE_31_31" title="Referenced at line 33, 54">HEX_CORE</a> <a href="#ZERO_43_18" id="ZERO_31_40" title="Referenced at line 43, 55, 56">ZERO</a>
<span class="keyword">lexical syntax</span>
  <a href="../ExprStat.sdf3/#INT_182_53" id="INT_33_3" title="Referenced at ../ExprStat.sdf3 line 182">INT</a>          = [\-\+]? (<a href="#INT_CORE_NE_30_20" id="INT_CORE_NE_33_27" title="Defined at line 30, 39">INT_CORE_NE</a> | (<a href="#INT_CORE_31_13" id="INT_CORE_33_42" title="Defined at line 31, 42, 43">INT_CORE</a> <a href="#EXP_30_3" id="EXP_33_51" title="Defined at line 30, 37">EXP</a>) | <a href="#BIN_CORE_31_22" id="BIN_CORE_33_58" title="Defined at line 31, 44">BIN_CORE</a> | <a href="#HEX_CORE_31_31" id="HEX_CORE_33_69" title="Defined at line 31, 45">HEX_CORE</a>)
  <button class="modal-open" id="REAL_34_3" title="Multi-file references" data-urls="#REAL_51_3 line 51; ../ExprStat.sdf3/#REAL_184_53 line 184">REAL</button>         = [\-\+]? (<a href="#REAL_CORE_NE_30_7" id="REAL_CORE_NE_34_27" title="Defined at line 30, 38">REAL_CORE_NE</a> | (<a href="#REAL_CORE_31_3" id="REAL_CORE_34_43" title="Defined at line 31, 41">REAL_CORE</a> <a href="#EXP_30_3" id="EXP_34_53" title="Defined at line 30, 37">EXP</a>))
  <a href="../ExprStat.sdf3/#FLOAT_181_53" id="FLOAT_35_3" title="Referenced at ../ExprStat.sdf3 line 181">FLOAT</a>        = [\-\+]? ((<a href="#REAL_CORE_NE_30_7" id="REAL_CORE_NE_35_28" title="Defined at line 30, 38">REAL_CORE_NE</a> [<span class="cons_Regular">f</span><span class="cons_Regular">F</span>]) | (<a href="#REAL_CORE_31_3" id="REAL_CORE_35_50" title="Defined at line 31, 41">REAL_CORE</a> <a href="#EXP_30_3" id="EXP_35_60" title="Defined at line 30, 37">EXP</a> [<span class="cons_Regular">f</span><span class="cons_Regular">F</span>]) | <span class="cons_Lit">"nan"</span> | <span class="cons_Lit">"inf"</span>)

  <a href="#EXP_33_51" id="EXP_37_3" title="Referenced at line 33, 34, 35">EXP</a>          = [<span class="cons_Regular">e</span><span class="cons_Regular">E</span>] [\+]? [<span class="cons_Regular">0</span>-<span class="cons_Regular">9</span>]+
  <a href="#REAL_CORE_NE_34_27" id="REAL_CORE_NE_38_3" title="Referenced at line 34, 35, 52">REAL_CORE_NE</a> = <a href="#REAL_CORE_31_3" id="REAL_CORE_38_18" title="Defined at line 31, 41">REAL_CORE</a>
  <a href="#INT_CORE_NE_33_27" id="INT_CORE_NE_39_3" title="Referenced at line 33, 53">INT_CORE_NE</a>  = <a href="#INT_CORE_31_13" id="INT_CORE_39_18" title="Defined at line 31, 42, 43">INT_CORE</a>

  <a href="#REAL_CORE_34_43" id="REAL_CORE_41_3" title="Referenced at line 34, 35, 38">REAL_CORE</a>    = <a href="#INT_CORE_31_13" id="INT_CORE_41_18" title="Defined at line 31, 42, 43">INT_CORE</a> <span class="cons_Lit">"."</span> [<span class="cons_Regular">0</span>-<span class="cons_Regular">9</span>]* | [<span class="cons_Regular">0</span>-<span class="cons_Regular">9</span>]+
  <a href="#INT_CORE_33_42" id="INT_CORE_42_3" title="Referenced at line 33, 39, 41">INT_CORE</a>     = [<span class="cons_Regular">1</span>-<span class="cons_Regular">9</span>][<span class="cons_Regular">0</span>-<span class="cons_Regular">9</span>]*
  <a href="#INT_CORE_33_42" id="INT_CORE_43_3" title="Referenced at line 33, 39, 41">INT_CORE</a>     = <a href="#ZERO_31_40" id="ZERO_43_18" title="Defined at line 31, 46">ZERO</a>
  <a href="#BIN_CORE_33_58" id="BIN_CORE_44_3" title="Referenced at line 33">BIN_CORE</a>     = <span class="cons_Lit">"0"</span> [<span class="cons_Regular">b</span><span class="cons_Regular">B</span>] [<span class="cons_Regular">0</span>-<span class="cons_Regular">1</span>]+
  <a href="#HEX_CORE_33_69" id="HEX_CORE_45_3" title="Referenced at line 33, 54">HEX_CORE</a>     = <span class="cons_Lit">"0"</span> [<span class="cons_Regular">x</span><span class="cons_Regular">X</span>] [<span class="cons_Regular">0</span>-<span class="cons_Regular">9</span><span class="cons_Regular">a</span>-<span class="cons_Regular">f</span><span class="cons_Regular">A</span>-<span class="cons_Regular">F</span>]+
  <a href="#ZERO_43_18" id="ZERO_46_3" title="Referenced at line 43, 55, 56">ZERO</a>         = <span class="cons_Lit">"0"</span>
<span class="keyword">lexical syntax</span>
  <a href="#ID_11_3" id="ID_48_3" title="Referenced at line 11">ID</a>           = <span class="cons_Lit">"nan"</span> {<span class="keyword">reject</span>}
  <a href="#ID_11_3" id="ID_49_3" title="Referenced at line 11">ID</a>           = <span class="cons_Lit">"inf"</span> {<span class="keyword">reject</span>}
<span class="keyword">lexical restrictions</span>
  <a href="#REAL_29_7" id="REAL_51_3" title="Defined at line 29, 34">REAL</a>         -/- [<span class="cons_Regular">f</span><span class="cons_Regular">F</span>]
  <a href="#REAL_CORE_NE_30_7" id="REAL_CORE_NE_52_3" title="Defined at line 30, 38">REAL_CORE_NE</a> -/- [<span class="cons_Regular">e</span><span class="cons_Regular">E</span>]
  <a href="#INT_CORE_NE_30_20" id="INT_CORE_NE_53_3" title="Defined at line 30, 39">INT_CORE_NE</a>  -/- [<span class="cons_Regular">e</span><span class="cons_Regular">E</span>]
  <a href="#HEX_CORE_31_31" id="HEX_CORE_54_3" title="Defined at line 31, 45">HEX_CORE</a>     -/- [<span class="cons_Regular">0</span>-<span class="cons_Regular">9</span><span class="cons_Regular">a</span>-<span class="cons_Regular">f</span><span class="cons_Regular">A</span>-<span class="cons_Regular">F</span>]
  <a href="#ZERO_31_40" id="ZERO_55_3" title="Defined at line 31, 46">ZERO</a>         -/- [<span class="cons_Regular">x</span><span class="cons_Regular">X</span>]
  <a href="#ZERO_31_40" id="ZERO_56_3" title="Defined at line 31, 46">ZERO</a>         -/- [<span class="cons_Regular">b</span><span class="cons_Regular">B</span>]


<span class="layout">// --- STRINGS -------</span>

<span class="keyword">lexical sorts</span>
  <button class="modal-open" id="STRING_62_3" title="Multi-file references" data-urls="../ExprStat.sdf3/#STRING_185_53 line 185; ../Poosl.sdf3/#STRING_60_66 line 60, 61">STRING</button> <a href="../ExprStat.sdf3/#CHARACTER_180_53" id="CHARACTER_62_10" title="Referenced at ../ExprStat.sdf3 line 180">CHARACTER</a>
  <a href="#STRING_CHAR_66_26" id="STRING_CHAR_63_3" title="Referenced at line 66">STRING_CHAR</a> <a href="#CHARACTER_CHAR_67_25" id="CHARACTER_CHAR_63_15" title="Referenced at line 67">CHARACTER_CHAR</a>
  <a href="#ESCAPE_SEQUENCE_70_21" id="ESCAPE_SEQUENCE_64_3" title="Referenced at line 70, 73">ESCAPE_SEQUENCE</a> <a href="#ESCAPE_ZERO_74_21" id="ESCAPE_ZERO_64_19" title="Referenced at line 74">ESCAPE_ZERO</a> <span id="BACKSLASH_CHAR_64_31" title="Not referenced">BACKSLASH_CHAR</span>
<span class="keyword">lexical syntax</span>
  <button class="modal-open" id="STRING_66_3" title="Multi-file references" data-urls="../ExprStat.sdf3/#STRING_185_53 line 185; ../Poosl.sdf3/#STRING_60_66 line 60, 61">STRING</button>          = <span class="cons_Lit">"\""</span> <a href="#STRING_CHAR_63_3" id="STRING_CHAR_66_26" title="Defined at line 63, 69, 70">STRING_CHAR</a>* <span class="cons_Lit">"\""</span>
  <a href="../ExprStat.sdf3/#CHARACTER_180_53" id="CHARACTER_67_3" title="Referenced at ../ExprStat.sdf3 line 180">CHARACTER</a>       = <span class="cons_Lit">"'"</span> <a href="#CHARACTER_CHAR_63_15" id="CHARACTER_CHAR_67_25" title="Defined at line 63, 72, 73, 74">CHARACTER_CHAR</a> <span class="cons_Lit">"'"</span>

  <a href="#STRING_CHAR_66_26" id="STRING_CHAR_69_3" title="Referenced at line 66">STRING_CHAR</a>     = ~[\\\"\n]
  <a href="#STRING_CHAR_66_26" id="STRING_CHAR_70_3" title="Referenced at line 66">STRING_CHAR</a>     = <a href="#ESCAPE_SEQUENCE_64_3" id="ESCAPE_SEQUENCE_70_21" title="Defined at line 64, 76, 77, 78, 79">ESCAPE_SEQUENCE</a>

  <a href="#CHARACTER_CHAR_67_25" id="CHARACTER_CHAR_72_3" title="Referenced at line 67">CHARACTER_CHAR</a>  = ~[\\\'\n]
  <a href="#CHARACTER_CHAR_67_25" id="CHARACTER_CHAR_73_3" title="Referenced at line 67">CHARACTER_CHAR</a>  = <a href="#ESCAPE_SEQUENCE_64_3" id="ESCAPE_SEQUENCE_73_21" title="Defined at line 64, 76, 77, 78, 79">ESCAPE_SEQUENCE</a>
  <a href="#CHARACTER_CHAR_67_25" id="CHARACTER_CHAR_74_3" title="Referenced at line 67">CHARACTER_CHAR</a>  = <a href="#ESCAPE_ZERO_64_19" id="ESCAPE_ZERO_74_21" title="Defined at line 64, 80">ESCAPE_ZERO</a>

  <a href="#ESCAPE_SEQUENCE_70_21" id="ESCAPE_SEQUENCE_76_3" title="Referenced at line 70, 73">ESCAPE_SEQUENCE</a> = <span class="cons_Lit">"\\"</span> [<span class="cons_Regular">n</span><span class="cons_Regular">t</span><span class="cons_Regular">v</span><span class="cons_Regular">b</span><span class="cons_Regular">r</span><span class="cons_Regular">f</span><span class="cons_Regular">a</span>\\\?\'\"]
  <a href="#ESCAPE_SEQUENCE_70_21" id="ESCAPE_SEQUENCE_77_3" title="Referenced at line 70, 73">ESCAPE_SEQUENCE</a> = <span class="cons_Lit">"\\x"</span> [<span class="cons_Regular">0</span>-<span class="cons_Regular">9</span><span class="cons_Regular">a</span>-<span class="cons_Regular">f</span><span class="cons_Regular">A</span>-<span class="cons_Regular">F</span>][<span class="cons_Regular">0</span>-<span class="cons_Regular">9</span><span class="cons_Regular">a</span>-<span class="cons_Regular">f</span><span class="cons_Regular">A</span>-<span class="cons_Regular">F</span>]?
  <a href="#ESCAPE_SEQUENCE_70_21" id="ESCAPE_SEQUENCE_78_3" title="Referenced at line 70, 73">ESCAPE_SEQUENCE</a> = <span class="cons_Lit">"\\x0"</span> {<span class="keyword">reject</span>}
  <a href="#ESCAPE_SEQUENCE_70_21" id="ESCAPE_SEQUENCE_79_3" title="Referenced at line 70, 73">ESCAPE_SEQUENCE</a> = <span class="cons_Lit">"\\x00"</span> {<span class="keyword">reject</span>}
  <a href="#ESCAPE_ZERO_74_21" id="ESCAPE_ZERO_80_3" title="Referenced at line 74">ESCAPE_ZERO</a>     = <span class="cons_Lit">"\\x0"</span> | <span class="cons_Lit">"\\x00"</span>


<span class="layout">// --- LAYOUT -------</span>

<span class="keyword">lexical sorts</span>
  <a href="#ML_COM_91_14" id="ML_COM_86_3" title="Referenced at line 91, 93">ML_COM</a>
  <a href="#LONESTAR_93_25" id="LONESTAR_87_3" title="Referenced at line 93, 99">LONESTAR</a>
  <a href="#EOF_95_38" id="EOF_88_3" title="Referenced at line 95, 100">EOF</a>
<span class="keyword">lexical syntax</span>
  <span class="keyword">LAYOUT</span>   = [\ \t\n\r]
  <span class="keyword">LAYOUT</span>   = <a href="#ML_COM_86_3" id="ML_COM_91_14" title="Defined at line 86, 92">ML_COM</a>
  <a href="#ML_COM_91_14" id="ML_COM_92_3" title="Referenced at line 91, 93">ML_COM</a>   = <span class="cons_Lit">"/*"</span>
               (~[\*] | <a href="#LONESTAR_87_3" id="LONESTAR_93_25" title="Defined at line 87, 96">LONESTAR</a> | <a href="#ML_COM_86_3" id="ML_COM_93_36" title="Defined at line 86, 92">ML_COM</a>)*
             <span class="cons_Lit">"*/"</span>
  <span class="keyword">LAYOUT</span>   = <span class="cons_Lit">"//"</span> ~[\n\r]* ([\n\r] | <a href="#EOF_88_3" id="EOF_95_38" title="Defined at line 88, 97">EOF</a>)
  <a href="#LONESTAR_93_25" id="LONESTAR_96_3" title="Referenced at line 93, 99">LONESTAR</a> = [\*]
  <a href="#EOF_95_38" id="EOF_97_3" title="Referenced at line 95, 100">EOF</a>      =
<span class="keyword">lexical restrictions</span>
  <a href="#LONESTAR_87_3" id="LONESTAR_99_3" title="Defined at line 87, 96">LONESTAR</a> -/- [\/] 
  <a href="#EOF_88_3" id="EOF_100_3" title="Defined at line 88, 97">EOF</a>      -/- ~[]
<span class="keyword">context-free restrictions</span>
  <span class="keyword">LAYOUT</span>? -/- [\ \t\n\r]
  <span class="keyword">LAYOUT</span>? -/- [\/].[\/]
  <span class="keyword">LAYOUT</span>? -/- [\/].[\*]

</code></pre></td></tr></tbody></table></div>

<div id="modal">
  <div id="modal-content">
    <span id="modal-close">&times;</span>
    <h2 id="modal-h2"></h2>
    <p  id="modal-p"></p>
    <ul id="modal-ul"></ul>
  </div>
</div>
