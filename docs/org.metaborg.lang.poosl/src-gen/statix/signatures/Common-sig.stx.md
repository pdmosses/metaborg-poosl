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
<td class="code"><pre><code><span class="keyword">module</span> <button class="modal-open" id="signatures/Common-sig_1_8" title="Multi-file references" data-urls="../ExprStat-sig.stx/#signatures/Common-sig_4_3 line 4; ../Poosl-sig.stx/#signatures/Common-sig_4_3 line 4; ../../../../trans/statics-comm.stx/#signatures/Common-sig_5_5 line 5; ../../../../trans/statics-expr-stat.stx/#signatures/Common-sig_5_5 line 5; ../../../../trans/statics-names.stx/#signatures/Common-sig_5_5 line 5; ../../../../trans/statics-opt.stx/#signatures/Common-sig_5_5 line 5; ../../../../trans/statics-typing.stx/#signatures/Common-sig_5_5 line 5; ../../../../trans/statics.stx/#signatures/Common-sig_5_5 line 5"><span class="token sort_Id">signatures/Common-sig</span></button>

<span class="keyword">imports</span>

<span class="keyword">signature</span>

  <span class="keyword">sorts</span>
    <span class="cons_SortAlias"><button class="modal-open" id="ID_8_5" title="Multi-file references" data-urls="../ExprStat-sig.stx/#ID_74_21 line 74, 75, 83, 94, 96, 98, 103, 112, 113; ../Poosl-sig.stx/#ID_96_18 line 96, 99, 101, 102, 103, 104, 105, 106, 114, 116, 117, 118, 119, 126, 128, 130, 132, 133, 134, 137, 139, 142, 146, 147; ../Stratego-Poosl-sig.stx/#ID_80_37 line 80, 81"><span class="token sort_Id">ID</span></button> <span class="operator">=</span> <span class="cons_StringSort">string</span></span>
    <span class="cons_SortAlias"><a href="../ExprStat-sig.stx/#ENV_122_27" id="ENV_9_5" title="Referenced at ../ExprStat-sig.stx line 122"><span class="token sort_Id">ENV</span></a> <span class="operator">=</span> <span class="cons_StringSort">string</span></span>
    <span class="cons_SortAlias"><button class="modal-open" id="BOOL_10_5" title="Multi-file references" data-urls="../ExprStat-sig.stx/#BOOL_115_23 line 115; ../Stratego-Poosl-sig.stx/#BOOL_146_37 line 146"><span class="token sort_Id">BOOL</span></button> <span class="operator">=</span> <span class="cons_StringSort">string</span></span>
    <span class="cons_SortAlias"><button class="modal-open" id="INT_11_5" title="Multi-file references" data-urls="../ExprStat-sig.stx/#INT_118_23 line 118; ../Stratego-Poosl-sig.stx/#INT_149_37 line 149"><span class="token sort_Id">INT</span></button> <span class="operator">=</span> <span class="cons_StringSort">string</span></span>
    <span class="cons_SortAlias"><button class="modal-open" id="REAL_12_5" title="Multi-file references" data-urls="../ExprStat-sig.stx/#REAL_120_20 line 120; ../Stratego-Poosl-sig.stx/#REAL_150_37 line 150"><span class="token sort_Id">REAL</span></button> <span class="operator">=</span> <span class="cons_StringSort">string</span></span>
    <span class="cons_SortAlias"><button class="modal-open" id="FLOAT_13_5" title="Multi-file references" data-urls="../ExprStat-sig.stx/#FLOAT_117_21 line 117; ../Stratego-Poosl-sig.stx/#FLOAT_148_37 line 148"><span class="token sort_Id">FLOAT</span></button> <span class="operator">=</span> <span class="cons_StringSort">string</span></span>
    <span class="cons_SortAlias"><span id="EXP_14_5" title="Not referenced"><span class="token sort_Id">EXP</span></span> <span class="operator">=</span> <span class="cons_StringSort">string</span></span>
    <span class="cons_SortAlias"><span id="REAL_CORE_NE_15_5" title="Not referenced"><span class="token sort_Id">REAL_CORE_NE</span></span> <span class="operator">=</span> <span class="cons_StringSort">string</span></span>
    <span class="cons_SortAlias"><span id="INT_CORE_NE_16_5" title="Not referenced"><span class="token sort_Id">INT_CORE_NE</span></span> <span class="operator">=</span> <span class="cons_StringSort">string</span></span>
    <span class="cons_SortAlias"><span id="REAL_CORE_17_5" title="Not referenced"><span class="token sort_Id">REAL_CORE</span></span> <span class="operator">=</span> <span class="cons_StringSort">string</span></span>
    <span class="cons_SortAlias"><span id="INT_CORE_18_5" title="Not referenced"><span class="token sort_Id">INT_CORE</span></span> <span class="operator">=</span> <span class="cons_StringSort">string</span></span>
    <span class="cons_SortAlias"><span id="BIN_CORE_19_5" title="Not referenced"><span class="token sort_Id">BIN_CORE</span></span> <span class="operator">=</span> <span class="cons_StringSort">string</span></span>
    <span class="cons_SortAlias"><span id="HEX_CORE_20_5" title="Not referenced"><span class="token sort_Id">HEX_CORE</span></span> <span class="operator">=</span> <span class="cons_StringSort">string</span></span>
    <span class="cons_SortAlias"><span id="ZERO_21_5" title="Not referenced"><span class="token sort_Id">ZERO</span></span> <span class="operator">=</span> <span class="cons_StringSort">string</span></span>
    <span class="cons_SortAlias"><button class="modal-open" id="STRING_22_5" title="Multi-file references" data-urls="../ExprStat-sig.stx/#STRING_121_22 line 121; ../Poosl-sig.stx/#STRING_93_14 line 93, 94; ../Stratego-Poosl-sig.stx/#STRING_151_37 line 151"><span class="token sort_Id">STRING</span></button> <span class="operator">=</span> <span class="cons_StringSort">string</span></span>
    <span class="cons_SortAlias"><button class="modal-open" id="CHARACTER_23_5" title="Multi-file references" data-urls="../ExprStat-sig.stx/#CHARACTER_116_25 line 116; ../Stratego-Poosl-sig.stx/#CHARACTER_147_37 line 147"><span class="token sort_Id">CHARACTER</span></button> <span class="operator">=</span> <span class="cons_StringSort">string</span></span>
    <span class="cons_SortAlias"><span id="STRING_CHAR_24_5" title="Not referenced"><span class="token sort_Id">STRING_CHAR</span></span> <span class="operator">=</span> <span class="cons_StringSort">string</span></span>
    <span class="cons_SortAlias"><span id="CHARACTER_CHAR_25_5" title="Not referenced"><span class="token sort_Id">CHARACTER_CHAR</span></span> <span class="operator">=</span> <span class="cons_StringSort">string</span></span>
    <span class="cons_SortAlias"><span id="ESCAPE_SEQUENCE_26_5" title="Not referenced"><span class="token sort_Id">ESCAPE_SEQUENCE</span></span> <span class="operator">=</span> <span class="cons_StringSort">string</span></span>
    <span class="cons_SortAlias"><span id="ESCAPE_ZERO_27_5" title="Not referenced"><span class="token sort_Id">ESCAPE_ZERO</span></span> <span class="operator">=</span> <span class="cons_StringSort">string</span></span>
    <span class="cons_SortAlias"><span id="BACKSLASH_CHAR_28_5" title="Not referenced"><span class="token sort_Id">BACKSLASH_CHAR</span></span> <span class="operator">=</span> <span class="cons_StringSort">string</span></span>
    <span class="cons_SortAlias"><span id="ML_COM_29_5" title="Not referenced"><span class="token sort_Id">ML_COM</span></span> <span class="operator">=</span> <span class="cons_StringSort">string</span></span>
    <span class="cons_SortAlias"><span id="LONESTAR_30_5" title="Not referenced"><span class="token sort_Id">LONESTAR</span></span> <span class="operator">=</span> <span class="cons_StringSort">string</span></span>
    <span class="cons_SortAlias"><span id="EOF_31_5" title="Not referenced"><span class="token sort_Id">EOF</span></span> <span class="operator">=</span> <span class="cons_StringSort">string</span></span>

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
