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
<td class="code"><pre><code><span class="keyword">module</span> <button class="modal-open" id="Common_1_8" title="a definition with multiple references" data-urls="../ExprStat.sdf3/#Common line 4_5; ../Poosl.sdf3/#Common line 4_5">Common</button>

<span class="layout">// --- ID -------</span>

<span class="keyword">lexical sorts</span>
  <a href="#ID_11_3" id="ID_6_3" title="a definition with a single reference">ID</a> <a href="../ExprStat.sdf3/#ENV_186_53" id="ENV_6_6" title="a definition with a single reference">ENV</a>
<span class="keyword">lexical syntax</span>
  <a href="#ID_11_3" id="ID_8_3" title="a definition with a single reference">ID</a>  = [<span class="cons_Regular">a</span>-<span class="cons_Regular">z</span><span class="cons_Regular">A</span>-<span class="cons_Regular">Z</span>] [<span class="cons_Regular">a</span>-<span class="cons_Regular">z</span><span class="cons_Regular">A</span>-<span class="cons_Regular">Z</span><span class="cons_Regular">0</span>-<span class="cons_Regular">9</span>\_]*
  <a href="../ExprStat.sdf3/#ENV_186_53" id="ENV_9_3" title="a definition with a single reference">ENV</a> = <span class="cons_Lit">"${"</span> [<span class="cons_Regular">a</span>-<span class="cons_Regular">z</span><span class="cons_Regular">A</span>-<span class="cons_Regular">Z</span><span class="cons_Regular">0</span>-<span class="cons_Regular">9</span>\_]+ <span class="cons_Lit">"}"</span>
<span class="keyword">lexical restrictions</span>
  <a href="#ID_6_3" id="ID_11_3" title="a reference to a single-file definition">ID</a>  -/- [<span class="cons_Regular">a</span>-<span class="cons_Regular">z</span><span class="cons_Regular">A</span>-<span class="cons_Regular">Z</span><span class="cons_Regular">0</span>-<span class="cons_Regular">9</span>\_]


<span class="layout">// --- BOOLEANS -------</span>

<span class="keyword">lexical sorts</span>
  <a href="../ExprStat.sdf3/#BOOL_179_53" id="BOOL_17_3" title="a definition with a single reference">BOOL</a>
<span class="keyword">lexical syntax</span>
  <a href="../ExprStat.sdf3/#BOOL_179_53" id="BOOL_19_3" title="a definition with a single reference">BOOL</a> = <span class="cons_Lit">"false"</span>
  <a href="../ExprStat.sdf3/#BOOL_179_53" id="BOOL_20_3" title="a definition with a single reference">BOOL</a> = <span class="cons_Lit">"true"</span>
<span class="keyword">lexical syntax</span>
  <a href="#ID_11_3" id="ID_22_3" title="a definition with a single reference">ID</a>   = <span class="cons_Lit">"false"</span> {<span class="keyword">reject</span>}
  <a href="#ID_11_3" id="ID_23_3" title="a definition with a single reference">ID</a>   = <span class="cons_Lit">"true"</span> {<span class="keyword">reject</span>}


<span class="layout">// --- NUMBERS -------</span>

<span class="keyword">lexical sorts</span>
  <a href="../ExprStat.sdf3/#INT_182_53" id="INT_29_3" title="a definition with a single reference">INT</a> <button class="modal-open" id="REAL_29_7" title="a definition with multiple references" data-urls="#REAL line 51_3; ../ExprStat.sdf3/#REAL line 184_53">REAL</button> <a href="../ExprStat.sdf3/#FLOAT_181_53" id="FLOAT_29_12" title="a definition with a single reference">FLOAT</a>
  <button class="modal-open" id="EXP_30_3" title="a definition with multiple references" data-urls="#EXP line 33_51, 34_53, 35_60">EXP</button> <button class="modal-open" id="REAL_CORE_NE_30_7" title="a definition with multiple references" data-urls="#REAL_CORE_NE line 34_27, 35_28, 52_3">REAL_CORE_NE</button> <button class="modal-open" id="INT_CORE_NE_30_20" title="a definition with multiple references" data-urls="#INT_CORE_NE line 33_27, 53_3">INT_CORE_NE</button>
  <button class="modal-open" id="REAL_CORE_31_3" title="a definition with multiple references" data-urls="#REAL_CORE line 34_43, 35_50, 38_18">REAL_CORE</button> <button class="modal-open" id="INT_CORE_31_13" title="a definition with multiple references" data-urls="#INT_CORE line 33_42, 39_18, 41_18">INT_CORE</button> <a href="#BIN_CORE_33_58" id="BIN_CORE_31_22" title="a definition with a single reference">BIN_CORE</a> <button class="modal-open" id="HEX_CORE_31_31" title="a definition with multiple references" data-urls="#HEX_CORE line 33_69, 54_3">HEX_CORE</button> <button class="modal-open" id="ZERO_31_40" title="a definition with multiple references" data-urls="#ZERO line 43_18, 55_3, 56_3">ZERO</button>
<span class="keyword">lexical syntax</span>
  <a href="../ExprStat.sdf3/#INT_182_53" id="INT_33_3" title="a definition with a single reference">INT</a>          = [\-\+]? (<a href="#INT_CORE_NE_30_20" id="INT_CORE_NE_33_27" title="a reference to a single-file definition">INT_CORE_NE</a> | (<a href="#INT_CORE_31_13" id="INT_CORE_33_42" title="a reference to a single-file definition">INT_CORE</a> <a href="#EXP_30_3" id="EXP_33_51" title="a reference to a single-file definition">EXP</a>) | <a href="#BIN_CORE_31_22" id="BIN_CORE_33_58" title="a reference to a single-file definition">BIN_CORE</a> | <a href="#HEX_CORE_31_31" id="HEX_CORE_33_69" title="a reference to a single-file definition">HEX_CORE</a>)
  <button class="modal-open" id="REAL_34_3" title="a definition with multiple references" data-urls="#REAL line 51_3; ../ExprStat.sdf3/#REAL line 184_53">REAL</button>         = [\-\+]? (<a href="#REAL_CORE_NE_30_7" id="REAL_CORE_NE_34_27" title="a reference to a single-file definition">REAL_CORE_NE</a> | (<a href="#REAL_CORE_31_3" id="REAL_CORE_34_43" title="a reference to a single-file definition">REAL_CORE</a> <a href="#EXP_30_3" id="EXP_34_53" title="a reference to a single-file definition">EXP</a>))
  <a href="../ExprStat.sdf3/#FLOAT_181_53" id="FLOAT_35_3" title="a definition with a single reference">FLOAT</a>        = [\-\+]? ((<a href="#REAL_CORE_NE_30_7" id="REAL_CORE_NE_35_28" title="a reference to a single-file definition">REAL_CORE_NE</a> [<span class="cons_Regular">f</span><span class="cons_Regular">F</span>]) | (<a href="#REAL_CORE_31_3" id="REAL_CORE_35_50" title="a reference to a single-file definition">REAL_CORE</a> <a href="#EXP_30_3" id="EXP_35_60" title="a reference to a single-file definition">EXP</a> [<span class="cons_Regular">f</span><span class="cons_Regular">F</span>]) | <span class="cons_Lit">"nan"</span> | <span class="cons_Lit">"inf"</span>)

  <button class="modal-open" id="EXP_37_3" title="a definition with multiple references" data-urls="#EXP line 33_51, 34_53, 35_60">EXP</button>          = [<span class="cons_Regular">e</span><span class="cons_Regular">E</span>] [\+]? [<span class="cons_Regular">0</span>-<span class="cons_Regular">9</span>]+
  <button class="modal-open" id="REAL_CORE_NE_38_3" title="a definition with multiple references" data-urls="#REAL_CORE_NE line 34_27, 35_28, 52_3">REAL_CORE_NE</button> = <a href="#REAL_CORE_31_3" id="REAL_CORE_38_18" title="a reference to a single-file definition">REAL_CORE</a>
  <button class="modal-open" id="INT_CORE_NE_39_3" title="a definition with multiple references" data-urls="#INT_CORE_NE line 33_27, 53_3">INT_CORE_NE</button>  = <a href="#INT_CORE_31_13" id="INT_CORE_39_18" title="a reference to a single-file definition">INT_CORE</a>

  <button class="modal-open" id="REAL_CORE_41_3" title="a definition with multiple references" data-urls="#REAL_CORE line 34_43, 35_50, 38_18">REAL_CORE</button>    = <a href="#INT_CORE_31_13" id="INT_CORE_41_18" title="a reference to a single-file definition">INT_CORE</a> <span class="cons_Lit">"."</span> [<span class="cons_Regular">0</span>-<span class="cons_Regular">9</span>]* | [<span class="cons_Regular">0</span>-<span class="cons_Regular">9</span>]+
  <button class="modal-open" id="INT_CORE_42_3" title="a definition with multiple references" data-urls="#INT_CORE line 33_42, 39_18, 41_18">INT_CORE</button>     = [<span class="cons_Regular">1</span>-<span class="cons_Regular">9</span>][<span class="cons_Regular">0</span>-<span class="cons_Regular">9</span>]*
  <button class="modal-open" id="INT_CORE_43_3" title="a definition with multiple references" data-urls="#INT_CORE line 33_42, 39_18, 41_18">INT_CORE</button>     = <a href="#ZERO_31_40" id="ZERO_43_18" title="a reference to a single-file definition">ZERO</a>
  <a href="#BIN_CORE_33_58" id="BIN_CORE_44_3" title="a definition with a single reference">BIN_CORE</a>     = <span class="cons_Lit">"0"</span> [<span class="cons_Regular">b</span><span class="cons_Regular">B</span>] [<span class="cons_Regular">0</span>-<span class="cons_Regular">1</span>]+
  <button class="modal-open" id="HEX_CORE_45_3" title="a definition with multiple references" data-urls="#HEX_CORE line 33_69, 54_3">HEX_CORE</button>     = <span class="cons_Lit">"0"</span> [<span class="cons_Regular">x</span><span class="cons_Regular">X</span>] [<span class="cons_Regular">0</span>-<span class="cons_Regular">9</span><span class="cons_Regular">a</span>-<span class="cons_Regular">f</span><span class="cons_Regular">A</span>-<span class="cons_Regular">F</span>]+
  <button class="modal-open" id="ZERO_46_3" title="a definition with multiple references" data-urls="#ZERO line 43_18, 55_3, 56_3">ZERO</button>         = <span class="cons_Lit">"0"</span>
<span class="keyword">lexical syntax</span>
  <a href="#ID_11_3" id="ID_48_3" title="a definition with a single reference">ID</a>           = <span class="cons_Lit">"nan"</span> {<span class="keyword">reject</span>}
  <a href="#ID_11_3" id="ID_49_3" title="a definition with a single reference">ID</a>           = <span class="cons_Lit">"inf"</span> {<span class="keyword">reject</span>}
<span class="keyword">lexical restrictions</span>
  <a href="#REAL_29_7" id="REAL_51_3" title="a reference to a single-file definition">REAL</a>         -/- [<span class="cons_Regular">f</span><span class="cons_Regular">F</span>]
  <a href="#REAL_CORE_NE_30_7" id="REAL_CORE_NE_52_3" title="a reference to a single-file definition">REAL_CORE_NE</a> -/- [<span class="cons_Regular">e</span><span class="cons_Regular">E</span>]
  <a href="#INT_CORE_NE_30_20" id="INT_CORE_NE_53_3" title="a reference to a single-file definition">INT_CORE_NE</a>  -/- [<span class="cons_Regular">e</span><span class="cons_Regular">E</span>]
  <a href="#HEX_CORE_31_31" id="HEX_CORE_54_3" title="a reference to a single-file definition">HEX_CORE</a>     -/- [<span class="cons_Regular">0</span>-<span class="cons_Regular">9</span><span class="cons_Regular">a</span>-<span class="cons_Regular">f</span><span class="cons_Regular">A</span>-<span class="cons_Regular">F</span>]
  <a href="#ZERO_31_40" id="ZERO_55_3" title="a reference to a single-file definition">ZERO</a>         -/- [<span class="cons_Regular">x</span><span class="cons_Regular">X</span>]
  <a href="#ZERO_31_40" id="ZERO_56_3" title="a reference to a single-file definition">ZERO</a>         -/- [<span class="cons_Regular">b</span><span class="cons_Regular">B</span>]


<span class="layout">// --- STRINGS -------</span>

<span class="keyword">lexical sorts</span>
  <button class="modal-open" id="STRING_62_3" title="a definition with multiple references" data-urls="../ExprStat.sdf3/#STRING line 185_53; ../Poosl.sdf3/#STRING line 60_66, 61_69">STRING</button> <a href="../ExprStat.sdf3/#CHARACTER_180_53" id="CHARACTER_62_10" title="a definition with a single reference">CHARACTER</a>
  <a href="#STRING_CHAR_66_26" id="STRING_CHAR_63_3" title="a definition with a single reference">STRING_CHAR</a> <a href="#CHARACTER_CHAR_67_25" id="CHARACTER_CHAR_63_15" title="a definition with a single reference">CHARACTER_CHAR</a>
  <button class="modal-open" id="ESCAPE_SEQUENCE_64_3" title="a definition with multiple references" data-urls="#ESCAPE_SEQUENCE line 70_21, 73_21">ESCAPE_SEQUENCE</button> <a href="#ESCAPE_ZERO_74_21" id="ESCAPE_ZERO_64_19" title="a definition with a single reference">ESCAPE_ZERO</a> <span id="BACKSLASH_CHAR_64_31" title="a definition with no references">BACKSLASH_CHAR</span>
<span class="keyword">lexical syntax</span>
  <button class="modal-open" id="STRING_66_3" title="a definition with multiple references" data-urls="../ExprStat.sdf3/#STRING line 185_53; ../Poosl.sdf3/#STRING line 60_66, 61_69">STRING</button>          = <span class="cons_Lit">"\""</span> <a href="#STRING_CHAR_63_3" id="STRING_CHAR_66_26" title="a reference to a single-file definition">STRING_CHAR</a>* <span class="cons_Lit">"\""</span>
  <a href="../ExprStat.sdf3/#CHARACTER_180_53" id="CHARACTER_67_3" title="a definition with a single reference">CHARACTER</a>       = <span class="cons_Lit">"'"</span> <a href="#CHARACTER_CHAR_63_15" id="CHARACTER_CHAR_67_25" title="a reference to a single-file definition">CHARACTER_CHAR</a> <span class="cons_Lit">"'"</span>

  <a href="#STRING_CHAR_66_26" id="STRING_CHAR_69_3" title="a definition with a single reference">STRING_CHAR</a>     = ~[\\\"\n]
  <a href="#STRING_CHAR_66_26" id="STRING_CHAR_70_3" title="a definition with a single reference">STRING_CHAR</a>     = <a href="#ESCAPE_SEQUENCE_64_3" id="ESCAPE_SEQUENCE_70_21" title="a reference to a single-file definition">ESCAPE_SEQUENCE</a>

  <a href="#CHARACTER_CHAR_67_25" id="CHARACTER_CHAR_72_3" title="a definition with a single reference">CHARACTER_CHAR</a>  = ~[\\\'\n]
  <a href="#CHARACTER_CHAR_67_25" id="CHARACTER_CHAR_73_3" title="a definition with a single reference">CHARACTER_CHAR</a>  = <a href="#ESCAPE_SEQUENCE_64_3" id="ESCAPE_SEQUENCE_73_21" title="a reference to a single-file definition">ESCAPE_SEQUENCE</a>
  <a href="#CHARACTER_CHAR_67_25" id="CHARACTER_CHAR_74_3" title="a definition with a single reference">CHARACTER_CHAR</a>  = <a href="#ESCAPE_ZERO_64_19" id="ESCAPE_ZERO_74_21" title="a reference to a single-file definition">ESCAPE_ZERO</a>

  <button class="modal-open" id="ESCAPE_SEQUENCE_76_3" title="a definition with multiple references" data-urls="#ESCAPE_SEQUENCE line 70_21, 73_21">ESCAPE_SEQUENCE</button> = <span class="cons_Lit">"\\"</span> [<span class="cons_Regular">n</span><span class="cons_Regular">t</span><span class="cons_Regular">v</span><span class="cons_Regular">b</span><span class="cons_Regular">r</span><span class="cons_Regular">f</span><span class="cons_Regular">a</span>\\\?\'\"]
  <button class="modal-open" id="ESCAPE_SEQUENCE_77_3" title="a definition with multiple references" data-urls="#ESCAPE_SEQUENCE line 70_21, 73_21">ESCAPE_SEQUENCE</button> = <span class="cons_Lit">"\\x"</span> [<span class="cons_Regular">0</span>-<span class="cons_Regular">9</span><span class="cons_Regular">a</span>-<span class="cons_Regular">f</span><span class="cons_Regular">A</span>-<span class="cons_Regular">F</span>][<span class="cons_Regular">0</span>-<span class="cons_Regular">9</span><span class="cons_Regular">a</span>-<span class="cons_Regular">f</span><span class="cons_Regular">A</span>-<span class="cons_Regular">F</span>]?
  <button class="modal-open" id="ESCAPE_SEQUENCE_78_3" title="a definition with multiple references" data-urls="#ESCAPE_SEQUENCE line 70_21, 73_21">ESCAPE_SEQUENCE</button> = <span class="cons_Lit">"\\x0"</span> {<span class="keyword">reject</span>}
  <button class="modal-open" id="ESCAPE_SEQUENCE_79_3" title="a definition with multiple references" data-urls="#ESCAPE_SEQUENCE line 70_21, 73_21">ESCAPE_SEQUENCE</button> = <span class="cons_Lit">"\\x00"</span> {<span class="keyword">reject</span>}
  <a href="#ESCAPE_ZERO_74_21" id="ESCAPE_ZERO_80_3" title="a definition with a single reference">ESCAPE_ZERO</a>     = <span class="cons_Lit">"\\x0"</span> | <span class="cons_Lit">"\\x00"</span>


<span class="layout">// --- LAYOUT -------</span>

<span class="keyword">lexical sorts</span>
  <button class="modal-open" id="ML_COM_86_3" title="a definition with multiple references" data-urls="#ML_COM line 91_14, 93_36">ML_COM</button>
  <button class="modal-open" id="LONESTAR_87_3" title="a definition with multiple references" data-urls="#LONESTAR line 93_25, 99_3">LONESTAR</button>
  <button class="modal-open" id="EOF_88_3" title="a definition with multiple references" data-urls="#EOF line 95_38, 100_3">EOF</button>
<span class="keyword">lexical syntax</span>
  <span class="keyword">LAYOUT</span>   = [\ \t\n\r]
  <span class="keyword">LAYOUT</span>   = <a href="#ML_COM_86_3" id="ML_COM_91_14" title="a reference to a single-file definition">ML_COM</a>
  <button class="modal-open" id="ML_COM_92_3" title="a definition with multiple references" data-urls="#ML_COM line 91_14, 93_36">ML_COM</button>   = <span class="cons_Lit">"/*"</span>
               (~[\*] | <a href="#LONESTAR_87_3" id="LONESTAR_93_25" title="a reference to a single-file definition">LONESTAR</a> | <a href="#ML_COM_86_3" id="ML_COM_93_36" title="a reference to a single-file definition">ML_COM</a>)*
             <span class="cons_Lit">"*/"</span>
  <span class="keyword">LAYOUT</span>   = <span class="cons_Lit">"//"</span> ~[\n\r]* ([\n\r] | <a href="#EOF_88_3" id="EOF_95_38" title="a reference to a single-file definition">EOF</a>)
  <button class="modal-open" id="LONESTAR_96_3" title="a definition with multiple references" data-urls="#LONESTAR line 93_25, 99_3">LONESTAR</button> = [\*]
  <button class="modal-open" id="EOF_97_3" title="a definition with multiple references" data-urls="#EOF line 95_38, 100_3">EOF</button>      =
<span class="keyword">lexical restrictions</span>
  <a href="#LONESTAR_87_3" id="LONESTAR_99_3" title="a reference to a single-file definition">LONESTAR</a> -/- [\/] 
  <a href="#EOF_88_3" id="EOF_100_3" title="a reference to a single-file definition">EOF</a>      -/- ~[]
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
