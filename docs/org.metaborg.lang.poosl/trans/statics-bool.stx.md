---
title: statics-bool.stx
hide:
  - toc
---

# `statics-bool.stx`

:simple-github: [pdmosses/metaborg-poosl/org.metaborg.lang.poosl/trans/statics-bool.stx]

[pdmosses/metaborg-poosl/org.metaborg.lang.poosl/trans/statics-bool.stx]: https://github.com/pdmosses/metaborg-poosl/blob/master/org.metaborg.lang.poosl/trans/statics-bool.stx "The source file on GitHub"

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
</pre></div></td>
<td class="code"><pre><code><span class="keyword">module</span> <a href="../statics-typing.stx/#statics-bool_5_4" id="statics-bool_0_7" title="Referenced at ../statics-typing.stx line 6"><span class="token sort_Id">statics-bool</span></a>

<span class="keyword">signature</span>

    <span class="keyword">sorts</span>
        <span class="cons_SortDecl"><button class="modal-open" id="TYPE_BOOL_5_8" title="Multi-file references" data-urls="#TYPE_BOOL_8_16 ../statics-typing.stx/#TYPE_BOOL_17_58"><span class="token sort_Id">TYPE_BOOL</span></button></span>

    <span class="keyword">constructors</span>
        <span class="cons_OpDecl"><button class="modal-open" id="FALSE_8_8" title="Multi-file references" data-urls="#FALSE/0_15_12 ../statics-typing.stx/#FALSE/0_30_31"><span class="token sort_Id">FALSE</span></button> <span class="operator">:</span> <span class="cons_SimpleSort"><a href="#TYPE_BOOL_5_8" id="TYPE_BOOL_8_16" title="Defined at line 6"><span class="token sort_Id">TYPE_BOOL</span></a></span></span>
        <span class="cons_OpDecl"><button class="modal-open" id="TRUE_9_8" title="Multi-file references" data-urls="#TRUE/0_14_27 ../statics-typing.stx/#TRUE/0_13_60"><span class="token sort_Id">TRUE</span></button> <span class="operator">:</span> <span class="cons_SimpleSort"><a href="#TYPE_BOOL_5_8" id="TYPE_BOOL_9_15" title="Defined at line 6"><span class="token sort_Id">TYPE_BOOL</span></a></span></span>

<span class="keyword">rules</span>

    <button class="modal-open" id="forall_13_4" title="Multi-file references" data-urls="#forall_14_4 ../statics-typing.stx/#forall_35_71"><span class="token sort_Id">forall</span></button> <span class="operator">:</span> <span class="keyword">list</span><span class="operator">(</span><span class="cons_SimpleSort"><a href="#TYPE_BOOL_5_8" id="TYPE_BOOL_13_18" title="Defined at line 6"><span class="token sort_Id">TYPE_BOOL</span></a></span><span class="operator">)</span> <span class="operator">-&gt;</span> <span class="cons_SimpleSort"><a href="#TYPE_BOOL_5_8" id="TYPE_BOOL_13_32" title="Defined at line 6"><span class="token sort_Id">TYPE_BOOL</span></a></span>
    <a href="#forall_13_4" id="forall_14_4" title="Defined at line 14"><span class="token sort_Id">forall</span></a><span class="operator">([]</span>          <span class="operator">)</span> <span class="operator">=</span> <span class="cons_Op"><a href="#TRUE_9_8" id="TRUE_14_27" title="Defined at line 10"><span class="token sort_Id">TRUE</span></a>()</span><span class="operator">.</span>
    <a href="#forall_13_4" id="forall_15_4" title="Defined at line 14"><span class="token sort_Id">forall</span></a><span class="operator">([</span><span class="cons_Op"><a href="#FALSE_8_8" id="FALSE_15_12" title="Defined at line 9"><span class="token sort_Id">FALSE</span></a>()</span><span class="operator">|</span><span class="cons_Var"><span id="Ts_15_20" title="Not referenced locally, nor via imports"><span class="token sort_Id">Ts</span></span></span><span class="operator">])</span> <span class="operator">=</span> <span class="cons_Op"><a href="#FALSE_8_8" id="FALSE_15_27" title="Defined at line 9"><span class="token sort_Id">FALSE</span></a>()</span><span class="operator">.</span>
    <a href="#forall_13_4" id="forall_16_4" title="Defined at line 14"><span class="token sort_Id">forall</span></a><span class="operator">([</span><span class="cons_Op"><a href="#TRUE_9_8" id="TRUE_16_12" title="Defined at line 10"><span class="token sort_Id">TRUE</span></a>()</span> <span class="operator">|</span><span class="cons_Var"><span id="Ts_16_20" title="Not referenced locally, nor via imports"><span class="token sort_Id">Ts</span></span></span><span class="operator">])</span> <span class="operator">=</span> <a href="#forall_13_4" id="forall_16_27" title="Defined at line 14"><span class="token sort_Id">forall</span></a><span class="operator">(</span><span class="cons_Var">Ts</span><span class="operator">).</span>

    <a href="#bool_and_19_4" id="bool_and_18_4" title="Referenced at line 20, 21"><span class="token sort_Id">bool_and</span></a> <span class="operator">:</span> <span class="cons_SimpleSort"><a href="#TYPE_BOOL_5_8" id="TYPE_BOOL_18_15" title="Defined at line 6"><span class="token sort_Id">TYPE_BOOL</span></a></span> <span class="operator">*</span> <span class="cons_SimpleSort"><a href="#TYPE_BOOL_5_8" id="TYPE_BOOL_18_27" title="Defined at line 6"><span class="token sort_Id">TYPE_BOOL</span></a></span> <span class="operator">-&gt;</span> <span class="cons_SimpleSort"><a href="#TYPE_BOOL_5_8" id="TYPE_BOOL_18_40" title="Defined at line 6"><span class="token sort_Id">TYPE_BOOL</span></a></span>
    <a href="#bool_and_18_4" id="bool_and_19_4" title="Defined at line 19"><span class="token sort_Id">bool_and</span></a><span class="operator">(</span><span class="cons_Op"><a href="#FALSE_8_8" id="FALSE_19_13" title="Defined at line 9"><span class="token sort_Id">FALSE</span></a>()</span><span class="operator">,</span> <span class="operator">_</span>      <span class="operator">)</span> <span class="operator">=</span> <span class="cons_Op"><a href="#FALSE_8_8" id="FALSE_19_33" title="Defined at line 9"><span class="token sort_Id">FALSE</span></a>()</span><span class="operator">.</span>
    <a href="#bool_and_18_4" id="bool_and_20_4" title="Defined at line 19"><span class="token sort_Id">bool_and</span></a><span class="operator">(</span><span class="cons_Op"><a href="#TRUE_9_8" id="TRUE_20_13" title="Defined at line 10"><span class="token sort_Id">TRUE</span></a>()</span> <span class="operator">,</span> <span class="cons_Var">x</span>      <span class="operator">)</span> <span class="operator">=</span> <span class="cons_Var"><span id="x_20_33" title="Not referenced locally, nor via imports"><span class="token sort_Id">x</span></span></span><span class="operator">.</span>
<span class="layout">//  bool_and(_      , FALSE()) = FALSE().</span>
<span class="layout">//  bool_and(x      , TRUE() ) = x.</span>

    <button class="modal-open" id="or_24_4" title="Multi-file references" data-urls="#or_25_4 ../statics-typing.stx/#or_18_33"><span class="token sort_Id">or</span></button> <span class="operator">:</span> <span class="cons_SimpleSort"><a href="#TYPE_BOOL_5_8" id="TYPE_BOOL_24_9" title="Defined at line 6"><span class="token sort_Id">TYPE_BOOL</span></a></span> <span class="operator">*</span> <span class="cons_SimpleSort"><a href="#TYPE_BOOL_5_8" id="TYPE_BOOL_24_21" title="Defined at line 6"><span class="token sort_Id">TYPE_BOOL</span></a></span> <span class="operator">-&gt;</span> <span class="cons_SimpleSort"><a href="#TYPE_BOOL_5_8" id="TYPE_BOOL_24_34" title="Defined at line 6"><span class="token sort_Id">TYPE_BOOL</span></a></span>
    <a href="#or_24_4" id="or_25_4" title="Defined at line 25"><span class="token sort_Id">or</span></a><span class="operator">(</span><span class="cons_Op"><a href="#FALSE_8_8" id="FALSE_25_7" title="Defined at line 9"><span class="token sort_Id">FALSE</span></a>()</span><span class="operator">,</span> <span class="cons_Var"><span id="x_25_16" title="Not referenced locally, nor via imports"><span class="token sort_Id">x</span></span></span>      <span class="operator">)</span> <span class="operator">=</span> <span class="cons_Var">x</span><span class="operator">.</span>
    <a href="#or_24_4" id="or_26_4" title="Defined at line 25"><span class="token sort_Id">or</span></a><span class="operator">(</span><span class="cons_Op"><a href="#TRUE_9_8" id="TRUE_26_7" title="Defined at line 10"><span class="token sort_Id">TRUE</span></a>()</span> <span class="operator">,</span> <span class="operator">_</span>      <span class="operator">)</span> <span class="operator">=</span> <span class="cons_Op"><a href="#TRUE_9_8" id="TRUE_26_27" title="Defined at line 10"><span class="token sort_Id">TRUE</span></a>()</span><span class="operator">.</span>
<span class="layout">//  or(x      , FALSE()) = x.</span>
<span class="layout">//  or(_      , TRUE() ) = TRUE().</span>

</code></pre></td></tr></tbody></table></div>

<div id="modal">
  <div id="modal-content">
    <span id="modal-close">&times;</span>
    <h2 id="modal-h2"></h2>
    <p  id="modal-p"></p>
    <ul id="modal-ul"></ul>
  </div>
</div>
