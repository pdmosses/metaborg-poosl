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
<td class="code"><pre><code><span class="keyword">module</span> <a href="../ExprStat.sdf3/#Common_29_35" id="Common_7_13" title="Referenced at ../ExprStat.sdf3 line 4; ../Poosl.sdf3 line 4">Common</a>

<span class="layout">// --- ID -------</span>

<span class="keyword">lexical sorts</span>
  <a href="#ID_159_161" id="ID_50_52" title="Referenced at line 11">ID</a> <a href="../ExprStat.sdf3/#ENV_5903_5906" id="ENV_53_56" title="Referenced at ../ExprStat.sdf3 line 186">ENV</a>
<span class="keyword">lexical syntax</span>
  <a href="#ID_159_161" id="ID_74_76" title="Referenced at line 11">ID</a>  = [<span class="cons_Regular">a</span>-<span class="cons_Regular">z</span><span class="cons_Regular">A</span>-<span class="cons_Regular">Z</span>] [<span class="cons_Regular">a</span>-<span class="cons_Regular">z</span><span class="cons_Regular">A</span>-<span class="cons_Regular">Z</span><span class="cons_Regular">0</span>-<span class="cons_Regular">9</span>\_]*
  <a href="../ExprStat.sdf3/#ENV_5903_5906" id="ENV_106_109" title="Referenced at ../ExprStat.sdf3 line 186">ENV</a> = <span class="cons_Lit">"${"</span> [<span class="cons_Regular">a</span>-<span class="cons_Regular">z</span><span class="cons_Regular">A</span>-<span class="cons_Regular">Z</span><span class="cons_Regular">0</span>-<span class="cons_Regular">9</span>\_]+ <span class="cons_Lit">"}"</span>
<span class="keyword">lexical restrictions</span>
  <a href="#ID_50_52" id="ID_159_161" title="Defined at line 6, 8, 22, 23, 48, 49">ID</a>  -/- [<span class="cons_Regular">a</span>-<span class="cons_Regular">z</span><span class="cons_Regular">A</span>-<span class="cons_Regular">Z</span><span class="cons_Regular">0</span>-<span class="cons_Regular">9</span>\_]


<span class="layout">// --- BOOLEANS -------</span>

<span class="keyword">lexical sorts</span>
  <a href="../ExprStat.sdf3/#BOOL_5496_5500" id="BOOL_224_228" title="Referenced at ../ExprStat.sdf3 line 179">BOOL</a>
<span class="keyword">lexical syntax</span>
  <a href="../ExprStat.sdf3/#BOOL_5496_5500" id="BOOL_246_250" title="Referenced at ../ExprStat.sdf3 line 179">BOOL</a> = <span class="cons_Lit">"false"</span>
  <a href="../ExprStat.sdf3/#BOOL_5496_5500" id="BOOL_263_267" title="Referenced at ../ExprStat.sdf3 line 179">BOOL</a> = <span class="cons_Lit">"true"</span>
<span class="keyword">lexical syntax</span>
  <a href="#ID_159_161" id="ID_294_296" title="Referenced at line 11">ID</a>   = <span class="cons_Lit">"false"</span> {<span class="keyword">reject</span>}
  <a href="#ID_159_161" id="ID_320_322" title="Referenced at line 11">ID</a>   = <span class="cons_Lit">"true"</span> {<span class="keyword">reject</span>}


<span class="layout">// --- NUMBERS -------</span>

<span class="keyword">lexical sorts</span>
  <a href="../ExprStat.sdf3/#INT_5673_5676" id="INT_385_388" title="Referenced at ../ExprStat.sdf3 line 182">INT</a> <a href="#REAL_1094_1098" id="REAL_389_393" title="Referenced at line 51; ../ExprStat.sdf3 line 184">REAL</a> <a href="../ExprStat.sdf3/#FLOAT_5615_5620" id="FLOAT_394_399" title="Referenced at ../ExprStat.sdf3 line 181">FLOAT</a>
  <a href="#EXP_540_543" id="EXP_402_405" title="Referenced at line 33, 34, 35">EXP</a> <a href="#REAL_CORE_NE_594_606" id="REAL_CORE_NE_406_418" title="Referenced at line 34, 35, 52">REAL_CORE_NE</a> <a href="#INT_CORE_NE_516_527" id="INT_CORE_NE_419_430" title="Referenced at line 33, 53">INT_CORE_NE</a>
  <a href="#REAL_CORE_610_619" id="REAL_CORE_433_442" title="Referenced at line 34, 35, 38">REAL_CORE</a> <a href="#INT_CORE_531_539" id="INT_CORE_443_451" title="Referenced at line 33, 39, 41">INT_CORE</a> <a href="#BIN_CORE_547_555" id="BIN_CORE_452_460" title="Referenced at line 33">BIN_CORE</a> <a href="#HEX_CORE_558_566" id="HEX_CORE_461_469" title="Referenced at line 33, 54">HEX_CORE</a> <a href="#ZERO_894_898" id="ZERO_470_474" title="Referenced at line 43, 55, 56">ZERO</a>
<span class="keyword">lexical syntax</span>
  <a href="../ExprStat.sdf3/#INT_5673_5676" id="INT_492_495" title="Referenced at ../ExprStat.sdf3 line 182">INT</a>          = [\-\+]? (<a href="#INT_CORE_NE_419_430" id="INT_CORE_NE_516_527" title="Defined at line 30, 39">INT_CORE_NE</a> | (<a href="#INT_CORE_443_451" id="INT_CORE_531_539" title="Defined at line 31, 42, 43">INT_CORE</a> <a href="#EXP_402_405" id="EXP_540_543" title="Defined at line 30, 37">EXP</a>) | <a href="#BIN_CORE_452_460" id="BIN_CORE_547_555" title="Defined at line 31, 44">BIN_CORE</a> | <a href="#HEX_CORE_461_469" id="HEX_CORE_558_566" title="Defined at line 31, 45">HEX_CORE</a>)
  <a href="#REAL_1094_1098" id="REAL_570_574" title="Referenced at line 51; ../ExprStat.sdf3 line 184">REAL</a>         = [\-\+]? (<a href="#REAL_CORE_NE_406_418" id="REAL_CORE_NE_594_606" title="Defined at line 30, 38">REAL_CORE_NE</a> | (<a href="#REAL_CORE_433_442" id="REAL_CORE_610_619" title="Defined at line 31, 41">REAL_CORE</a> <a href="#EXP_402_405" id="EXP_620_623" title="Defined at line 30, 37">EXP</a>))
  <a href="../ExprStat.sdf3/#FLOAT_5615_5620" id="FLOAT_628_633" title="Referenced at ../ExprStat.sdf3 line 181">FLOAT</a>        = [\-\+]? ((<a href="#REAL_CORE_NE_406_418" id="REAL_CORE_NE_653_665" title="Defined at line 30, 38">REAL_CORE_NE</a> [<span class="cons_Regular">f</span><span class="cons_Regular">F</span>]) | (<a href="#REAL_CORE_433_442" id="REAL_CORE_675_684" title="Defined at line 31, 41">REAL_CORE</a> <a href="#EXP_402_405" id="EXP_685_688" title="Defined at line 30, 37">EXP</a> [<span class="cons_Regular">f</span><span class="cons_Regular">F</span>]) | <span class="cons_Lit">"nan"</span> | <span class="cons_Lit">"inf"</span>)

  <a href="#EXP_540_543" id="EXP_715_718" title="Referenced at line 33, 34, 35">EXP</a>          = [<span class="cons_Regular">e</span><span class="cons_Regular">E</span>] [\+]? [<span class="cons_Regular">0</span>-<span class="cons_Regular">9</span>]+
  <a href="#REAL_CORE_NE_594_606" id="REAL_CORE_NE_750_762" title="Referenced at line 34, 35, 52">REAL_CORE_NE</a> = <a href="#REAL_CORE_433_442" id="REAL_CORE_765_774" title="Defined at line 31, 41">REAL_CORE</a>
  <a href="#INT_CORE_NE_516_527" id="INT_CORE_NE_777_788" title="Referenced at line 33, 53">INT_CORE_NE</a>  = <a href="#INT_CORE_443_451" id="INT_CORE_792_800" title="Defined at line 31, 42, 43">INT_CORE</a>

  <a href="#REAL_CORE_610_619" id="REAL_CORE_804_813" title="Referenced at line 34, 35, 38">REAL_CORE</a>    = <a href="#INT_CORE_443_451" id="INT_CORE_819_827" title="Defined at line 31, 42, 43">INT_CORE</a> <span class="cons_Lit">"."</span> [<span class="cons_Regular">0</span>-<span class="cons_Regular">9</span>]* | [<span class="cons_Regular">0</span>-<span class="cons_Regular">9</span>]+
  <a href="#INT_CORE_531_539" id="INT_CORE_850_858" title="Referenced at line 33, 39, 41">INT_CORE</a>     = [<span class="cons_Regular">1</span>-<span class="cons_Regular">9</span>][<span class="cons_Regular">0</span>-<span class="cons_Regular">9</span>]*
  <a href="#INT_CORE_531_539" id="INT_CORE_879_887" title="Referenced at line 33, 39, 41">INT_CORE</a>     = <a href="#ZERO_470_474" id="ZERO_894_898" title="Defined at line 31, 46">ZERO</a>
  <a href="#BIN_CORE_547_555" id="BIN_CORE_901_909" title="Referenced at line 33">BIN_CORE</a>     = <span class="cons_Lit">"0"</span> [<span class="cons_Regular">b</span><span class="cons_Regular">B</span>] [<span class="cons_Regular">0</span>-<span class="cons_Regular">1</span>]+
  <a href="#HEX_CORE_558_566" id="HEX_CORE_934_942" title="Referenced at line 33, 54">HEX_CORE</a>     = <span class="cons_Lit">"0"</span> [<span class="cons_Regular">x</span><span class="cons_Regular">X</span>] [<span class="cons_Regular">0</span>-<span class="cons_Regular">9</span><span class="cons_Regular">a</span>-<span class="cons_Regular">f</span><span class="cons_Regular">A</span>-<span class="cons_Regular">F</span>]+
  <a href="#ZERO_894_898" id="ZERO_973_977" title="Referenced at line 43, 55, 56">ZERO</a>         = <span class="cons_Lit">"0"</span>
<span class="keyword">lexical syntax</span>
  <a href="#ID_159_161" id="ID_1009_1011" title="Referenced at line 11">ID</a>           = <span class="cons_Lit">"nan"</span> {<span class="keyword">reject</span>}
  <a href="#ID_159_161" id="ID_1041_1043" title="Referenced at line 11">ID</a>           = <span class="cons_Lit">"inf"</span> {<span class="keyword">reject</span>}
<span class="keyword">lexical restrictions</span>
  <a href="#REAL_389_393" id="REAL_1094_1098" title="Defined at line 29, 34">REAL</a>         -/- [<span class="cons_Regular">f</span><span class="cons_Regular">F</span>]
  <a href="#REAL_CORE_NE_406_418" id="REAL_CORE_NE_1118_1130" title="Defined at line 30, 38">REAL_CORE_NE</a> -/- [<span class="cons_Regular">e</span><span class="cons_Regular">E</span>]
  <a href="#INT_CORE_NE_419_430" id="INT_CORE_NE_1142_1153" title="Defined at line 30, 39">INT_CORE_NE</a>  -/- [<span class="cons_Regular">e</span><span class="cons_Regular">E</span>]
  <a href="#HEX_CORE_461_469" id="HEX_CORE_1166_1174" title="Defined at line 31, 45">HEX_CORE</a>     -/- [<span class="cons_Regular">0</span>-<span class="cons_Regular">9</span><span class="cons_Regular">a</span>-<span class="cons_Regular">f</span><span class="cons_Regular">A</span>-<span class="cons_Regular">F</span>]
  <a href="#ZERO_470_474" id="ZERO_1197_1201" title="Defined at line 31, 46">ZERO</a>         -/- [<span class="cons_Regular">x</span><span class="cons_Regular">X</span>]
  <a href="#ZERO_470_474" id="ZERO_1221_1225" title="Defined at line 31, 46">ZERO</a>         -/- [<span class="cons_Regular">b</span><span class="cons_Regular">B</span>]


<span class="layout">// --- STRINGS -------</span>

<span class="keyword">lexical sorts</span>
  <a href="../ExprStat.sdf3/#STRING_5844_5850" id="STRING_1285_1291" title="Referenced at ../ExprStat.sdf3 line 185; ../Poosl.sdf3 line 60, 61">STRING</a> <a href="../ExprStat.sdf3/#CHARACTER_5553_5562" id="CHARACTER_1292_1301" title="Referenced at ../ExprStat.sdf3 line 180">CHARACTER</a>
  <a href="#STRING_CHAR_1416_1427" id="STRING_CHAR_1304_1315" title="Referenced at line 66">STRING_CHAR</a> <a href="#CHARACTER_CHAR_1458_1472" id="CHARACTER_CHAR_1316_1330" title="Referenced at line 67">CHARACTER_CHAR</a>
  <a href="#ESCAPE_SEQUENCE_1528_1543" id="ESCAPE_SEQUENCE_1333_1348" title="Referenced at line 70, 73">ESCAPE_SEQUENCE</a> <a href="#ESCAPE_ZERO_1631_1642" id="ESCAPE_ZERO_1349_1360" title="Referenced at line 74">ESCAPE_ZERO</a> <span id="BACKSLASH_CHAR_1361_1375" title="Not referenced locally, nor via imports">BACKSLASH_CHAR</span>
<span class="keyword">lexical syntax</span>
  <a href="../ExprStat.sdf3/#STRING_5844_5850" id="STRING_1393_1399" title="Referenced at ../ExprStat.sdf3 line 185; ../Poosl.sdf3 line 60, 61">STRING</a>          = <span class="cons_Lit">"\""</span> <a href="#STRING_CHAR_1304_1315" id="STRING_CHAR_1416_1427" title="Defined at line 63, 69, 70">STRING_CHAR</a>* <span class="cons_Lit">"\""</span>
  <a href="../ExprStat.sdf3/#CHARACTER_5553_5562" id="CHARACTER_1436_1445" title="Referenced at ../ExprStat.sdf3 line 180">CHARACTER</a>       = <span class="cons_Lit">"'"</span> <a href="#CHARACTER_CHAR_1316_1330" id="CHARACTER_CHAR_1458_1472" title="Defined at line 63, 72, 73, 74">CHARACTER_CHAR</a> <span class="cons_Lit">"'"</span>

  <a href="#STRING_CHAR_1416_1427" id="STRING_CHAR_1480_1491" title="Referenced at line 66">STRING_CHAR</a>     = ~[\\\"\n]
  <a href="#STRING_CHAR_1416_1427" id="STRING_CHAR_1510_1521" title="Referenced at line 66">STRING_CHAR</a>     = <a href="#ESCAPE_SEQUENCE_1333_1348" id="ESCAPE_SEQUENCE_1528_1543" title="Defined at line 64, 76, 77, 78, 79">ESCAPE_SEQUENCE</a>

  <a href="#CHARACTER_CHAR_1458_1472" id="CHARACTER_CHAR_1547_1561" title="Referenced at line 67">CHARACTER_CHAR</a>  = ~[\\\'\n]
  <a href="#CHARACTER_CHAR_1458_1472" id="CHARACTER_CHAR_1577_1591" title="Referenced at line 67">CHARACTER_CHAR</a>  = <a href="#ESCAPE_SEQUENCE_1333_1348" id="ESCAPE_SEQUENCE_1595_1610" title="Defined at line 64, 76, 77, 78, 79">ESCAPE_SEQUENCE</a>
  <a href="#CHARACTER_CHAR_1458_1472" id="CHARACTER_CHAR_1613_1627" title="Referenced at line 67">CHARACTER_CHAR</a>  = <a href="#ESCAPE_ZERO_1349_1360" id="ESCAPE_ZERO_1631_1642" title="Defined at line 64, 80">ESCAPE_ZERO</a>

  <a href="#ESCAPE_SEQUENCE_1528_1543" id="ESCAPE_SEQUENCE_1646_1661" title="Referenced at line 70, 73">ESCAPE_SEQUENCE</a> = <span class="cons_Lit">"\\"</span> [<span class="cons_Regular">n</span><span class="cons_Regular">t</span><span class="cons_Regular">v</span><span class="cons_Regular">b</span><span class="cons_Regular">r</span><span class="cons_Regular">f</span><span class="cons_Regular">a</span>\\\?\'\"]
  <a href="#ESCAPE_SEQUENCE_1528_1543" id="ESCAPE_SEQUENCE_1689_1704" title="Referenced at line 70, 73">ESCAPE_SEQUENCE</a> = <span class="cons_Lit">"\\x"</span> [<span class="cons_Regular">0</span>-<span class="cons_Regular">9</span><span class="cons_Regular">a</span>-<span class="cons_Regular">f</span><span class="cons_Regular">A</span>-<span class="cons_Regular">F</span>][<span class="cons_Regular">0</span>-<span class="cons_Regular">9</span><span class="cons_Regular">a</span>-<span class="cons_Regular">f</span><span class="cons_Regular">A</span>-<span class="cons_Regular">F</span>]?
  <a href="#ESCAPE_SEQUENCE_1528_1543" id="ESCAPE_SEQUENCE_1739_1754" title="Referenced at line 70, 73">ESCAPE_SEQUENCE</a> = <span class="cons_Lit">"\\x0"</span> {<span class="keyword">reject</span>}
  <a href="#ESCAPE_SEQUENCE_1528_1543" id="ESCAPE_SEQUENCE_1775_1790" title="Referenced at line 70, 73">ESCAPE_SEQUENCE</a> = <span class="cons_Lit">"\\x00"</span> {<span class="keyword">reject</span>}
  <a href="#ESCAPE_ZERO_1631_1642" id="ESCAPE_ZERO_1812_1823" title="Referenced at line 74">ESCAPE_ZERO</a>     = <span class="cons_Lit">"\\x0"</span> | <span class="cons_Lit">"\\x00"</span>


<span class="layout">// --- LAYOUT -------</span>

<span class="keyword">lexical sorts</span>
  <a href="#ML_COM_1964_1970" id="ML_COM_1888_1894" title="Referenced at line 91, 93">ML_COM</a>
  <a href="#LONESTAR_2013_2021" id="LONESTAR_1897_1905" title="Referenced at line 93, 99">LONESTAR</a>
  <a href="#EOF_2088_2091" id="EOF_1908_1911" title="Referenced at line 95, 100">EOF</a>
<span class="keyword">lexical syntax</span>
  <span class="keyword">LAYOUT</span>   = [\ \t\n\r]
  <span class="keyword">LAYOUT</span>   = <a href="#ML_COM_1888_1894" id="ML_COM_1964_1970" title="Defined at line 86, 92">ML_COM</a>
  <a href="#ML_COM_1964_1970" id="ML_COM_1973_1979" title="Referenced at line 91, 93">ML_COM</a>   = <span class="cons_Lit">"/*"</span>
               (~[\*] | <a href="#LONESTAR_1897_1905" id="LONESTAR_2013_2021" title="Defined at line 87, 96">LONESTAR</a> | <a href="#ML_COM_1888_1894" id="ML_COM_2024_2030" title="Defined at line 86, 92">ML_COM</a>)*
             <span class="cons_Lit">"*/"</span>
  <span class="keyword">LAYOUT</span>   = <span class="cons_Lit">"//"</span> ~[\n\r]* ([\n\r] | <a href="#EOF_1908_1911" id="EOF_2088_2091" title="Defined at line 88, 97">EOF</a>)
  <a href="#LONESTAR_2013_2021" id="LONESTAR_2095_2103" title="Referenced at line 93, 99">LONESTAR</a> = [\*]
  <a href="#EOF_2088_2091" id="EOF_2113_2116" title="Referenced at line 95, 100">EOF</a>      =
<span class="keyword">lexical restrictions</span>
  <a href="#LONESTAR_1897_1905" id="LONESTAR_2147_2155" title="Defined at line 87, 96">LONESTAR</a> -/- [\/] 
  <a href="#EOF_1908_1911" id="EOF_2168_2171" title="Defined at line 88, 97">EOF</a>      -/- ~[]
<span class="keyword">context-free restrictions</span>
  <span class="keyword">LAYOUT</span>? -/- [\ \t\n\r]
  <span class="keyword">LAYOUT</span>? -/- [\/].[\/]
  <span class="keyword">LAYOUT</span>? -/- [\/].[\*]

</code></pre></td></tr></tbody></table></div>