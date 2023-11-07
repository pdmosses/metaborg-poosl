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
<td class="code"><pre><code><span class="keyword">module</span> <button class="modal-open" id="signatures/Common-sig_0_7" title="Multi-file references" data-urls="../ExprStat-sig.stx/#signatures/Common-sig_3_2 ../Poosl-sig.stx/#signatures/Common-sig_3_2 ../../../../trans/statics-comm.stx/#signatures/Common-sig_4_4 ../../../../trans/statics-expr-stat.stx/#signatures/Common-sig_4_4 ../../../../trans/statics-names.stx/#signatures/Common-sig_4_4 ../../../../trans/statics-opt.stx/#signatures/Common-sig_4_4 ../../../../trans/statics-typing.stx/#signatures/Common-sig_4_4 ../../../../trans/statics.stx/#signatures/Common-sig_4_4"><span class="token sort_Id">signatures/Common-sig</span></button>

<span class="keyword">imports</span>

<span class="keyword">signature</span>

  <span class="keyword">sorts</span>
    <span class="cons_SortAlias"><button class="modal-open" id="ID_7_4" title="Multi-file references" data-urls="../ExprStat-sig.stx/#ID_73_20 ../Poosl-sig.stx/#ID_95_17 ../Stratego-Poosl-sig.stx/#ID_79_36"><span class="token sort_Id">ID</span></button> <span class="operator">=</span> <span class="cons_StringSort">string</span></span>
    <span class="cons_SortAlias"><a href="../ExprStat-sig.stx/#ENV_121_26" id="ENV_8_4" title="Referenced at ../ExprStat-sig.stx line 122"><span class="token sort_Id">ENV</span></a> <span class="operator">=</span> <span class="cons_StringSort">string</span></span>
    <span class="cons_SortAlias"><button class="modal-open" id="BOOL_9_4" title="Multi-file references" data-urls="../ExprStat-sig.stx/#BOOL_114_22 ../Stratego-Poosl-sig.stx/#BOOL_145_36"><span class="token sort_Id">BOOL</span></button> <span class="operator">=</span> <span class="cons_StringSort">string</span></span>
    <span class="cons_SortAlias"><button class="modal-open" id="INT_10_4" title="Multi-file references" data-urls="../ExprStat-sig.stx/#INT_117_22 ../Stratego-Poosl-sig.stx/#INT_148_36"><span class="token sort_Id">INT</span></button> <span class="operator">=</span> <span class="cons_StringSort">string</span></span>
    <span class="cons_SortAlias"><button class="modal-open" id="REAL_11_4" title="Multi-file references" data-urls="../ExprStat-sig.stx/#REAL_119_19 ../Stratego-Poosl-sig.stx/#REAL_149_36"><span class="token sort_Id">REAL</span></button> <span class="operator">=</span> <span class="cons_StringSort">string</span></span>
    <span class="cons_SortAlias"><button class="modal-open" id="FLOAT_12_4" title="Multi-file references" data-urls="../ExprStat-sig.stx/#FLOAT_116_20 ../Stratego-Poosl-sig.stx/#FLOAT_147_36"><span class="token sort_Id">FLOAT</span></button> <span class="operator">=</span> <span class="cons_StringSort">string</span></span>
    <span class="cons_SortAlias"><span id="EXP_13_4" title="Not referenced locally, nor via imports"><span class="token sort_Id">EXP</span></span> <span class="operator">=</span> <span class="cons_StringSort">string</span></span>
    <span class="cons_SortAlias"><span id="REAL_CORE_NE_14_4" title="Not referenced locally, nor via imports"><span class="token sort_Id">REAL_CORE_NE</span></span> <span class="operator">=</span> <span class="cons_StringSort">string</span></span>
    <span class="cons_SortAlias"><span id="INT_CORE_NE_15_4" title="Not referenced locally, nor via imports"><span class="token sort_Id">INT_CORE_NE</span></span> <span class="operator">=</span> <span class="cons_StringSort">string</span></span>
    <span class="cons_SortAlias"><span id="REAL_CORE_16_4" title="Not referenced locally, nor via imports"><span class="token sort_Id">REAL_CORE</span></span> <span class="operator">=</span> <span class="cons_StringSort">string</span></span>
    <span class="cons_SortAlias"><span id="INT_CORE_17_4" title="Not referenced locally, nor via imports"><span class="token sort_Id">INT_CORE</span></span> <span class="operator">=</span> <span class="cons_StringSort">string</span></span>
    <span class="cons_SortAlias"><span id="BIN_CORE_18_4" title="Not referenced locally, nor via imports"><span class="token sort_Id">BIN_CORE</span></span> <span class="operator">=</span> <span class="cons_StringSort">string</span></span>
    <span class="cons_SortAlias"><span id="HEX_CORE_19_4" title="Not referenced locally, nor via imports"><span class="token sort_Id">HEX_CORE</span></span> <span class="operator">=</span> <span class="cons_StringSort">string</span></span>
    <span class="cons_SortAlias"><span id="ZERO_20_4" title="Not referenced locally, nor via imports"><span class="token sort_Id">ZERO</span></span> <span class="operator">=</span> <span class="cons_StringSort">string</span></span>
    <span class="cons_SortAlias"><button class="modal-open" id="STRING_21_4" title="Multi-file references" data-urls="../ExprStat-sig.stx/#STRING_120_21 ../Poosl-sig.stx/#STRING_92_13 ../Stratego-Poosl-sig.stx/#STRING_150_36"><span class="token sort_Id">STRING</span></button> <span class="operator">=</span> <span class="cons_StringSort">string</span></span>
    <span class="cons_SortAlias"><button class="modal-open" id="CHARACTER_22_4" title="Multi-file references" data-urls="../ExprStat-sig.stx/#CHARACTER_115_24 ../Stratego-Poosl-sig.stx/#CHARACTER_146_36"><span class="token sort_Id">CHARACTER</span></button> <span class="operator">=</span> <span class="cons_StringSort">string</span></span>
    <span class="cons_SortAlias"><span id="STRING_CHAR_23_4" title="Not referenced locally, nor via imports"><span class="token sort_Id">STRING_CHAR</span></span> <span class="operator">=</span> <span class="cons_StringSort">string</span></span>
    <span class="cons_SortAlias"><span id="CHARACTER_CHAR_24_4" title="Not referenced locally, nor via imports"><span class="token sort_Id">CHARACTER_CHAR</span></span> <span class="operator">=</span> <span class="cons_StringSort">string</span></span>
    <span class="cons_SortAlias"><span id="ESCAPE_SEQUENCE_25_4" title="Not referenced locally, nor via imports"><span class="token sort_Id">ESCAPE_SEQUENCE</span></span> <span class="operator">=</span> <span class="cons_StringSort">string</span></span>
    <span class="cons_SortAlias"><span id="ESCAPE_ZERO_26_4" title="Not referenced locally, nor via imports"><span class="token sort_Id">ESCAPE_ZERO</span></span> <span class="operator">=</span> <span class="cons_StringSort">string</span></span>
    <span class="cons_SortAlias"><span id="BACKSLASH_CHAR_27_4" title="Not referenced locally, nor via imports"><span class="token sort_Id">BACKSLASH_CHAR</span></span> <span class="operator">=</span> <span class="cons_StringSort">string</span></span>
    <span class="cons_SortAlias"><span id="ML_COM_28_4" title="Not referenced locally, nor via imports"><span class="token sort_Id">ML_COM</span></span> <span class="operator">=</span> <span class="cons_StringSort">string</span></span>
    <span class="cons_SortAlias"><span id="LONESTAR_29_4" title="Not referenced locally, nor via imports"><span class="token sort_Id">LONESTAR</span></span> <span class="operator">=</span> <span class="cons_StringSort">string</span></span>
    <span class="cons_SortAlias"><span id="EOF_30_4" title="Not referenced locally, nor via imports"><span class="token sort_Id">EOF</span></span> <span class="operator">=</span> <span class="cons_StringSort">string</span></span>

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
