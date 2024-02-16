---
title: Common-sig.stx
hide:
  - toc
---

# `Common-sig.stx`



[pdmosses/metaborg-poosl/org.metaborg.lang.poosl/src-gen/statix/signatures/Common-sig.stx]: https://github.com/pdmosses/metaborg-poosl/blob/master/org.metaborg.lang.poosl/src-gen/statix/signatures/Common-sig.stx "The source file on GitHub"

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
</pre></div></td>
<td class="code"><pre><code><span class="keyword">module</span> <button class="modal-open" id="signatures/Common-sig_1_8" title="a definition with multiple references" data-urls="../ExprStat-sig.stx/#signatures/Common-sig line 4_3; ../Poosl-sig.stx/#signatures/Common-sig line 4_3; ../../../../trans/statics-comm.stx/#signatures/Common-sig line 5_5; ../../../../trans/statics-expr-stat.stx/#signatures/Common-sig line 5_5; ../../../../trans/statics-names.stx/#signatures/Common-sig line 5_5; ../../../../trans/statics-opt.stx/#signatures/Common-sig line 5_5; ../../../../trans/statics-typing.stx/#signatures/Common-sig line 5_5; ../../../../trans/statics.stx/#signatures/Common-sig line 5_5"><span class="token sort_Id">signatures/Common-sig</span></button>

<span class="keyword">imports</span>

<span class="keyword">signature</span>

  <span class="keyword">sorts</span>
    <span class="cons_SortAlias"><button class="modal-open" id="ID_8_5" title="a definition with multiple references" data-urls="../ExprStat-sig.stx/#ID line 74_21, 74_26, 75_24, 75_29, 83_25, 94_22, 96_25, 98_28, 103_66, 112_21, 113_26; ../Poosl-sig.stx/#ID line 96_18, 99_49, 101_40, 101_64, 102_71, 103_72, 104_29, 104_53, 105_60, 106_61, 114_15, 116_19, 117_28, 118_37, 119_40, 126_37, 128_38, 130_12, 132_31, 132_36, 133_28, 133_33, 134_30, 137_37, 139_33, 139_38, 142_25, 146_20, 146_25, 147_20; ../Stratego-Poosl-sig.stx/#ID line 80_37, 81_37"><span class="token sort_Id">ID</span></button> <span class="operator">=</span> <span class="cons_StringSort"><span class="keyword">string</span></span></span>
    <span class="cons_SortAlias"><a href="../ExprStat-sig.stx/#ENV_122_27" id="ENV_9_5" title="a definition with a single reference"><span class="token sort_Id">ENV</span></a> <span class="operator">=</span> <span class="cons_StringSort"><span class="keyword">string</span></span></span>
    <span class="cons_SortAlias"><button class="modal-open" id="BOOL_10_5" title="a definition with multiple references" data-urls="../ExprStat-sig.stx/#BOOL line 115_23; ../Stratego-Poosl-sig.stx/#BOOL line 146_37"><span class="token sort_Id">BOOL</span></button> <span class="operator">=</span> <span class="cons_StringSort"><span class="keyword">string</span></span></span>
    <span class="cons_SortAlias"><button class="modal-open" id="INT_11_5" title="a definition with multiple references" data-urls="../ExprStat-sig.stx/#INT line 118_23; ../Stratego-Poosl-sig.stx/#INT line 149_37"><span class="token sort_Id">INT</span></button> <span class="operator">=</span> <span class="cons_StringSort"><span class="keyword">string</span></span></span>
    <span class="cons_SortAlias"><button class="modal-open" id="REAL_12_5" title="a definition with multiple references" data-urls="../ExprStat-sig.stx/#REAL line 120_20; ../Stratego-Poosl-sig.stx/#REAL line 150_37"><span class="token sort_Id">REAL</span></button> <span class="operator">=</span> <span class="cons_StringSort"><span class="keyword">string</span></span></span>
    <span class="cons_SortAlias"><button class="modal-open" id="FLOAT_13_5" title="a definition with multiple references" data-urls="../ExprStat-sig.stx/#FLOAT line 117_21; ../Stratego-Poosl-sig.stx/#FLOAT line 148_37"><span class="token sort_Id">FLOAT</span></button> <span class="operator">=</span> <span class="cons_StringSort"><span class="keyword">string</span></span></span>
    <span class="cons_SortAlias"><span id="EXP_14_5" title="a definition with no references"><span class="token sort_Id">EXP</span></span> <span class="operator">=</span> <span class="cons_StringSort"><span class="keyword">string</span></span></span>
    <span class="cons_SortAlias"><span id="REAL_CORE_NE_15_5" title="a definition with no references"><span class="token sort_Id">REAL_CORE_NE</span></span> <span class="operator">=</span> <span class="cons_StringSort"><span class="keyword">string</span></span></span>
    <span class="cons_SortAlias"><span id="INT_CORE_NE_16_5" title="a definition with no references"><span class="token sort_Id">INT_CORE_NE</span></span> <span class="operator">=</span> <span class="cons_StringSort"><span class="keyword">string</span></span></span>
    <span class="cons_SortAlias"><span id="REAL_CORE_17_5" title="a definition with no references"><span class="token sort_Id">REAL_CORE</span></span> <span class="operator">=</span> <span class="cons_StringSort"><span class="keyword">string</span></span></span>
    <span class="cons_SortAlias"><span id="INT_CORE_18_5" title="a definition with no references"><span class="token sort_Id">INT_CORE</span></span> <span class="operator">=</span> <span class="cons_StringSort"><span class="keyword">string</span></span></span>
    <span class="cons_SortAlias"><span id="BIN_CORE_19_5" title="a definition with no references"><span class="token sort_Id">BIN_CORE</span></span> <span class="operator">=</span> <span class="cons_StringSort"><span class="keyword">string</span></span></span>
    <span class="cons_SortAlias"><span id="HEX_CORE_20_5" title="a definition with no references"><span class="token sort_Id">HEX_CORE</span></span> <span class="operator">=</span> <span class="cons_StringSort"><span class="keyword">string</span></span></span>
    <span class="cons_SortAlias"><span id="ZERO_21_5" title="a definition with no references"><span class="token sort_Id">ZERO</span></span> <span class="operator">=</span> <span class="cons_StringSort"><span class="keyword">string</span></span></span>
    <span class="cons_SortAlias"><button class="modal-open" id="STRING_22_5" title="a definition with multiple references" data-urls="../ExprStat-sig.stx/#STRING line 121_22; ../Poosl-sig.stx/#STRING line 93_14, 94_17; ../Stratego-Poosl-sig.stx/#STRING line 151_37"><span class="token sort_Id">STRING</span></button> <span class="operator">=</span> <span class="cons_StringSort"><span class="keyword">string</span></span></span>
    <span class="cons_SortAlias"><button class="modal-open" id="CHARACTER_23_5" title="a definition with multiple references" data-urls="../ExprStat-sig.stx/#CHARACTER line 116_25; ../Stratego-Poosl-sig.stx/#CHARACTER line 147_37"><span class="token sort_Id">CHARACTER</span></button> <span class="operator">=</span> <span class="cons_StringSort"><span class="keyword">string</span></span></span>
    <span class="cons_SortAlias"><span id="STRING_CHAR_24_5" title="a definition with no references"><span class="token sort_Id">STRING_CHAR</span></span> <span class="operator">=</span> <span class="cons_StringSort"><span class="keyword">string</span></span></span>
    <span class="cons_SortAlias"><span id="CHARACTER_CHAR_25_5" title="a definition with no references"><span class="token sort_Id">CHARACTER_CHAR</span></span> <span class="operator">=</span> <span class="cons_StringSort"><span class="keyword">string</span></span></span>
    <span class="cons_SortAlias"><span id="ESCAPE_SEQUENCE_26_5" title="a definition with no references"><span class="token sort_Id">ESCAPE_SEQUENCE</span></span> <span class="operator">=</span> <span class="cons_StringSort"><span class="keyword">string</span></span></span>
    <span class="cons_SortAlias"><span id="ESCAPE_ZERO_27_5" title="a definition with no references"><span class="token sort_Id">ESCAPE_ZERO</span></span> <span class="operator">=</span> <span class="cons_StringSort"><span class="keyword">string</span></span></span>
    <span class="cons_SortAlias"><span id="BACKSLASH_CHAR_28_5" title="a definition with no references"><span class="token sort_Id">BACKSLASH_CHAR</span></span> <span class="operator">=</span> <span class="cons_StringSort"><span class="keyword">string</span></span></span>
    <span class="cons_SortAlias"><span id="ML_COM_29_5" title="a definition with no references"><span class="token sort_Id">ML_COM</span></span> <span class="operator">=</span> <span class="cons_StringSort"><span class="keyword">string</span></span></span>
    <span class="cons_SortAlias"><span id="LONESTAR_30_5" title="a definition with no references"><span class="token sort_Id">LONESTAR</span></span> <span class="operator">=</span> <span class="cons_StringSort"><span class="keyword">string</span></span></span>
    <span class="cons_SortAlias"><span id="EOF_31_5" title="a definition with no references"><span class="token sort_Id">EOF</span></span> <span class="operator">=</span> <span class="cons_StringSort"><span class="keyword">string</span></span></span>

  <span class="keyword">constructors</span>

<span class="keyword">signature</span>

  <span class="keyword">constructors</span>
</code></pre></td></tr></tbody></table></div>

<div id="modal">
  <div id="modal-content">
    <span id="modal-close">&times;</span>
    <h2 id="modal-h2"></h2>
    <p  id="modal-p"></p>
    <ul id="modal-ul"></ul>
  </div>
</div>
