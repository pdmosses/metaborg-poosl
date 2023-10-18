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
<td class="code"><pre><code><span class="keyword">module</span> <a href="../ExprStat-sig.stx/#signatures/Common-sig_42_63" id="signatures/Common-sig_7_28" title="Referenced at ../ExprStat-sig.stx line 4; ../Poosl-sig.stx line 4; ../../../../trans/statics-comm.stx line 5; ../../../../trans/statics-expr-stat.stx line 5; ../../../../trans/statics-names.stx line 5; ../../../../trans/statics-opt.stx line 5; ../../../../trans/statics-typing.stx line 5; ../../../../trans/statics.stx line 5"><span class="token sort_Id">signatures/Common-sig</span></a>

<span class="keyword">imports</span>

<span class="keyword">signature</span>

  <span class="keyword">sorts</span>
    <span class="cons_SortAlias"><a href="../ExprStat-sig.stx/#ID_2362_2364" id="ID_62_64" title="Referenced at ../ExprStat-sig.stx line 74, 74, 75, 75, 83, 94, 96, 98, 103, 112, 113; ../Poosl-sig.stx line 96, 99, 101, 101, 102, 103, 104, 104, 105, 106, 114, 116, 117, 118, 119, 126, 128, 130, 132, 132, 133, 133, 134, 137, 139, 139, 142, 146, 146, 147; ../Stratego-Poosl-sig.stx line 79, 80"><span class="token sort_Id">ID</span></a> <span class="operator">=</span> <span class="cons_StringSort">string</span></span>
    <span class="cons_SortAlias"><a href="../ExprStat-sig.stx/#ENV_5430_5433" id="ENV_78_81" title="Referenced at ../ExprStat-sig.stx line 122"><span class="token sort_Id">ENV</span></a> <span class="operator">=</span> <span class="cons_StringSort">string</span></span>
    <span class="cons_SortAlias"><a href="../ExprStat-sig.stx/#BOOL_5092_5096" id="BOOL_95_99" title="Referenced at ../ExprStat-sig.stx line 115; ../Stratego-Poosl-sig.stx line 145"><span class="token sort_Id">BOOL</span></a> <span class="operator">=</span> <span class="cons_StringSort">string</span></span>
    <span class="cons_SortAlias"><a href="../ExprStat-sig.stx/#INT_5245_5248" id="INT_113_116" title="Referenced at ../ExprStat-sig.stx line 118; ../Stratego-Poosl-sig.stx line 148"><span class="token sort_Id">INT</span></a> <span class="operator">=</span> <span class="cons_StringSort">string</span></span>
    <span class="cons_SortAlias"><a href="../ExprStat-sig.stx/#REAL_5327_5331" id="REAL_130_134" title="Referenced at ../ExprStat-sig.stx line 120; ../Stratego-Poosl-sig.stx line 149"><span class="token sort_Id">REAL</span></a> <span class="operator">=</span> <span class="cons_StringSort">string</span></span>
    <span class="cons_SortAlias"><a href="../ExprStat-sig.stx/#FLOAT_5195_5200" id="FLOAT_148_153" title="Referenced at ../ExprStat-sig.stx line 117; ../Stratego-Poosl-sig.stx line 147"><span class="token sort_Id">FLOAT</span></a> <span class="operator">=</span> <span class="cons_StringSort">string</span></span>
    <span class="cons_SortAlias"><span id="EXP_167_170" title="Not referenced locally, nor via imports"><span class="token sort_Id">EXP</span></span> <span class="operator">=</span> <span class="cons_StringSort">string</span></span>
    <span class="cons_SortAlias"><span id="REAL_CORE_NE_184_196" title="Not referenced locally, nor via imports"><span class="token sort_Id">REAL_CORE_NE</span></span> <span class="operator">=</span> <span class="cons_StringSort">string</span></span>
    <span class="cons_SortAlias"><span id="INT_CORE_NE_210_221" title="Not referenced locally, nor via imports"><span class="token sort_Id">INT_CORE_NE</span></span> <span class="operator">=</span> <span class="cons_StringSort">string</span></span>
    <span class="cons_SortAlias"><span id="REAL_CORE_235_244" title="Not referenced locally, nor via imports"><span class="token sort_Id">REAL_CORE</span></span> <span class="operator">=</span> <span class="cons_StringSort">string</span></span>
    <span class="cons_SortAlias"><span id="INT_CORE_258_266" title="Not referenced locally, nor via imports"><span class="token sort_Id">INT_CORE</span></span> <span class="operator">=</span> <span class="cons_StringSort">string</span></span>
    <span class="cons_SortAlias"><span id="BIN_CORE_280_288" title="Not referenced locally, nor via imports"><span class="token sort_Id">BIN_CORE</span></span> <span class="operator">=</span> <span class="cons_StringSort">string</span></span>
    <span class="cons_SortAlias"><span id="HEX_CORE_302_310" title="Not referenced locally, nor via imports"><span class="token sort_Id">HEX_CORE</span></span> <span class="operator">=</span> <span class="cons_StringSort">string</span></span>
    <span class="cons_SortAlias"><span id="ZERO_324_328" title="Not referenced locally, nor via imports"><span class="token sort_Id">ZERO</span></span> <span class="operator">=</span> <span class="cons_StringSort">string</span></span>
    <span class="cons_SortAlias"><a href="../ExprStat-sig.stx/#STRING_5375_5381" id="STRING_342_348" title="Referenced at ../ExprStat-sig.stx line 121; ../Poosl-sig.stx line 93, 94; ../Stratego-Poosl-sig.stx line 150"><span class="token sort_Id">STRING</span></a> <span class="operator">=</span> <span class="cons_StringSort">string</span></span>
    <span class="cons_SortAlias"><a href="../ExprStat-sig.stx/#CHARACTER_5143_5152" id="CHARACTER_362_371" title="Referenced at ../ExprStat-sig.stx line 116; ../Stratego-Poosl-sig.stx line 146"><span class="token sort_Id">CHARACTER</span></a> <span class="operator">=</span> <span class="cons_StringSort">string</span></span>
    <span class="cons_SortAlias"><span id="STRING_CHAR_385_396" title="Not referenced locally, nor via imports"><span class="token sort_Id">STRING_CHAR</span></span> <span class="operator">=</span> <span class="cons_StringSort">string</span></span>
    <span class="cons_SortAlias"><span id="CHARACTER_CHAR_410_424" title="Not referenced locally, nor via imports"><span class="token sort_Id">CHARACTER_CHAR</span></span> <span class="operator">=</span> <span class="cons_StringSort">string</span></span>
    <span class="cons_SortAlias"><span id="ESCAPE_SEQUENCE_438_453" title="Not referenced locally, nor via imports"><span class="token sort_Id">ESCAPE_SEQUENCE</span></span> <span class="operator">=</span> <span class="cons_StringSort">string</span></span>
    <span class="cons_SortAlias"><span id="ESCAPE_ZERO_467_478" title="Not referenced locally, nor via imports"><span class="token sort_Id">ESCAPE_ZERO</span></span> <span class="operator">=</span> <span class="cons_StringSort">string</span></span>
    <span class="cons_SortAlias"><span id="BACKSLASH_CHAR_492_506" title="Not referenced locally, nor via imports"><span class="token sort_Id">BACKSLASH_CHAR</span></span> <span class="operator">=</span> <span class="cons_StringSort">string</span></span>
    <span class="cons_SortAlias"><span id="ML_COM_520_526" title="Not referenced locally, nor via imports"><span class="token sort_Id">ML_COM</span></span> <span class="operator">=</span> <span class="cons_StringSort">string</span></span>
    <span class="cons_SortAlias"><span id="LONESTAR_540_548" title="Not referenced locally, nor via imports"><span class="token sort_Id">LONESTAR</span></span> <span class="operator">=</span> <span class="cons_StringSort">string</span></span>
    <span class="cons_SortAlias"><span id="EOF_562_565" title="Not referenced locally, nor via imports"><span class="token sort_Id">EOF</span></span> <span class="operator">=</span> <span class="cons_StringSort">string</span></span>

  <span class="keyword">constructors</span>

<span class="keyword">signature</span>

  <span class="keyword">constructors</span>
</code></pre></td></tr></tbody></table></div>