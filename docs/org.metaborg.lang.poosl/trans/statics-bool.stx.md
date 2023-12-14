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
<td class="code"><pre><code><span class="keyword">module</span> <a href="../statics-typing.stx/#statics-bool_6_5" id="statics-bool_1_8" title="Referenced at ../statics-typing.stx line 6"><span class="token sort_Id">statics-bool</span></a>

<span class="keyword">signature</span>

    <span class="keyword">sorts</span>
        <span class="cons_SortDecl"><button class="modal-open" id="TYPE_BOOL_6_9" title="Multi-file references" data-urls="#TYPE_BOOL_9_17 line 9, 10, 14, 19, 25; ../statics-typing.stx/#TYPE_BOOL_18_59 line 18, 28, 35, 41"><span class="token sort_Id">TYPE_BOOL</span></button></span>

    <span class="keyword">constructors</span>
        <span class="cons_OpDecl"><button class="modal-open" id="FALSE_9_9" title="Multi-file references" data-urls="#FALSE_16_13 line 16, 20, 26; ../statics-typing.stx/#FALSE_31_32 line 31, 43"><span class="token sort_Id">FALSE</span></button> <span class="operator">:</span> <span class="cons_SimpleSort"><a href="#TYPE_BOOL_6_9" id="TYPE_BOOL_9_17" title="Defined at line 6"><span class="token sort_Id">TYPE_BOOL</span></a></span></span>
        <span class="cons_OpDecl"><button class="modal-open" id="TRUE_10_9" title="Multi-file references" data-urls="#TRUE_15_28 line 15, 17, 21, 27; ../statics-typing.stx/#TRUE_14_61 line 14, 30, 42, 44"><span class="token sort_Id">TRUE</span></button> <span class="operator">:</span> <span class="cons_SimpleSort"><a href="#TYPE_BOOL_6_9" id="TYPE_BOOL_10_16" title="Defined at line 6"><span class="token sort_Id">TYPE_BOOL</span></a></span></span>

<span class="keyword">rules</span>

    <button class="modal-open" id="forall_14_5" title="Multi-file references" data-urls="#forall_15_5 line 15, 16, 17; ../statics-typing.stx/#forall_36_72 line 36"><span class="token sort_Id">forall</span></button> <span class="operator">:</span> <span class="keyword">list</span><span class="operator">(</span><span class="cons_SimpleSort"><a href="#TYPE_BOOL_6_9" id="TYPE_BOOL_14_19" title="Defined at line 6"><span class="token sort_Id">TYPE_BOOL</span></a></span><span class="operator">)</span> <span class="operator">-&gt;</span> <span class="cons_SimpleSort"><a href="#TYPE_BOOL_6_9" id="TYPE_BOOL_14_33" title="Defined at line 6"><span class="token sort_Id">TYPE_BOOL</span></a></span>
    <a href="#forall_14_5" id="forall_15_5" title="Defined at line 14"><span class="token sort_Id">forall</span></a><span class="operator">([]</span>          <span class="operator">)</span> <span class="operator">=</span> <span class="cons_Op"><a href="#TRUE_10_9" id="TRUE_15_28" title="Defined at line 10"><span class="token sort_Id">TRUE</span></a>()</span><span class="operator">.</span>
    <a href="#forall_14_5" id="forall_16_5" title="Defined at line 14"><span class="token sort_Id">forall</span></a><span class="operator">([</span><span class="cons_Op"><a href="#FALSE_9_9" id="FALSE_16_13" title="Defined at line 9"><span class="token sort_Id">FALSE</span></a>()</span><span class="operator">|</span><span class="cons_Var"><span id="Ts_16_21" title="Not referenced"><span class="token sort_Id">Ts</span></span></span><span class="operator">])</span> <span class="operator">=</span> <span class="cons_Op"><a href="#FALSE_9_9" id="FALSE_16_28" title="Defined at line 9"><span class="token sort_Id">FALSE</span></a>()</span><span class="operator">.</span>
    <a href="#forall_14_5" id="forall_17_5" title="Defined at line 14"><span class="token sort_Id">forall</span></a><span class="operator">([</span><span class="cons_Op"><a href="#TRUE_10_9" id="TRUE_17_13" title="Defined at line 10"><span class="token sort_Id">TRUE</span></a>()</span> <span class="operator">|</span><span class="cons_Var">Ts</span><span class="operator">])</span> <span class="operator">=</span> <a href="#forall_14_5" id="forall_17_28" title="Defined at line 14"><span class="token sort_Id">forall</span></a><span class="operator">(</span><span class="cons_Var"><span id="Ts_17_35" title="Not referenced"><span class="token sort_Id">Ts</span></span></span><span class="operator">).</span>

    <a href="#bool_and_20_5" id="bool_and_19_5" title="Referenced at line 20, 21"><span class="token sort_Id">bool_and</span></a> <span class="operator">:</span> <span class="cons_SimpleSort"><a href="#TYPE_BOOL_6_9" id="TYPE_BOOL_19_16" title="Defined at line 6"><span class="token sort_Id">TYPE_BOOL</span></a></span> <span class="operator">*</span> <span class="cons_SimpleSort"><a href="#TYPE_BOOL_6_9" id="TYPE_BOOL_19_28" title="Defined at line 6"><span class="token sort_Id">TYPE_BOOL</span></a></span> <span class="operator">-&gt;</span> <span class="cons_SimpleSort"><a href="#TYPE_BOOL_6_9" id="TYPE_BOOL_19_41" title="Defined at line 6"><span class="token sort_Id">TYPE_BOOL</span></a></span>
    <a href="#bool_and_19_5" id="bool_and_20_5" title="Defined at line 19"><span class="token sort_Id">bool_and</span></a><span class="operator">(</span><span class="cons_Op"><a href="#FALSE_9_9" id="FALSE_20_14" title="Defined at line 9"><span class="token sort_Id">FALSE</span></a>()</span><span class="operator">,</span> <span class="operator">_</span>      <span class="operator">)</span> <span class="operator">=</span> <span class="cons_Op"><a href="#FALSE_9_9" id="FALSE_20_34" title="Defined at line 9"><span class="token sort_Id">FALSE</span></a>()</span><span class="operator">.</span>
    <a href="#bool_and_19_5" id="bool_and_21_5" title="Defined at line 19"><span class="token sort_Id">bool_and</span></a><span class="operator">(</span><span class="cons_Op"><a href="#TRUE_10_9" id="TRUE_21_14" title="Defined at line 10"><span class="token sort_Id">TRUE</span></a>()</span> <span class="operator">,</span> <span class="cons_Var"><span id="x_21_23" title="Not referenced"><span class="token sort_Id">x</span></span></span>      <span class="operator">)</span> <span class="operator">=</span> <span class="cons_Var">x</span><span class="operator">.</span>
<span class="layout">//  bool_and(_      , FALSE()) = FALSE().</span>
<span class="layout">//  bool_and(x      , TRUE() ) = x.</span>

    <button class="modal-open" id="or_25_5" title="Multi-file references" data-urls="#or_26_5 line 26, 27; ../statics-typing.stx/#or_19_34 line 19"><span class="token sort_Id">or</span></button> <span class="operator">:</span> <span class="cons_SimpleSort"><a href="#TYPE_BOOL_6_9" id="TYPE_BOOL_25_10" title="Defined at line 6"><span class="token sort_Id">TYPE_BOOL</span></a></span> <span class="operator">*</span> <span class="cons_SimpleSort"><a href="#TYPE_BOOL_6_9" id="TYPE_BOOL_25_22" title="Defined at line 6"><span class="token sort_Id">TYPE_BOOL</span></a></span> <span class="operator">-&gt;</span> <span class="cons_SimpleSort"><a href="#TYPE_BOOL_6_9" id="TYPE_BOOL_25_35" title="Defined at line 6"><span class="token sort_Id">TYPE_BOOL</span></a></span>
    <a href="#or_25_5" id="or_26_5" title="Defined at line 25"><span class="token sort_Id">or</span></a><span class="operator">(</span><span class="cons_Op"><a href="#FALSE_9_9" id="FALSE_26_8" title="Defined at line 9"><span class="token sort_Id">FALSE</span></a>()</span><span class="operator">,</span> <span class="cons_Var"><span id="x_26_17" title="Not referenced"><span class="token sort_Id">x</span></span></span>      <span class="operator">)</span> <span class="operator">=</span> <span class="cons_Var">x</span><span class="operator">.</span>
    <a href="#or_25_5" id="or_27_5" title="Defined at line 25"><span class="token sort_Id">or</span></a><span class="operator">(</span><span class="cons_Op"><a href="#TRUE_10_9" id="TRUE_27_8" title="Defined at line 10"><span class="token sort_Id">TRUE</span></a>()</span> <span class="operator">,</span> <span class="operator">_</span>      <span class="operator">)</span> <span class="operator">=</span> <span class="cons_Op"><a href="#TRUE_10_9" id="TRUE_27_28" title="Defined at line 10"><span class="token sort_Id">TRUE</span></a>()</span><span class="operator">.</span>
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
