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
<td class="code"><pre><code><span class="keyword">module</span> <a href="../statics-typing.stx/#statics-bool_6_5" id="statics-bool_1_8" title="a definition with a single reference"><span class="token sort_Id">statics-bool</span></a>

<span class="keyword">signature</span>

    <span class="keyword">sorts</span>
        <span class="cons_SortDecl"><button class="modal-open" id="TYPE_BOOL_6_9" title="a definition with multiple references" data-urls="#TYPE_BOOL line 9_17, 10_16, 14_19, 14_33, 19_16, 19_28, 19_41, 25_10, 25_22, 25_35; ../statics-typing.stx/#TYPE_BOOL line 18_59, 28_52, 35_79, 41_48"><span class="token sort_Id">TYPE_BOOL</span></button></span>

    <span class="keyword">constructors</span>
        <span class="cons_OpDecl"><button class="modal-open" id="FALSE_9_9" title="a definition with multiple references" data-urls="#FALSE line 16_13, 16_28, 20_14, 20_34, 26_8; ../statics-typing.stx/#FALSE line 31_32, 43_58"><span class="token sort_Id">FALSE</span></button> <span class="operator">:</span> <span class="cons_SimpleSort"><a href="#TYPE_BOOL_6_9" id="TYPE_BOOL_9_17" title="a reference to a single-file definition"><span class="token sort_Id">TYPE_BOOL</span></a></span></span>
        <span class="cons_OpDecl"><button class="modal-open" id="TRUE_10_9" title="a definition with multiple references" data-urls="#TRUE line 15_28, 17_13, 21_14, 27_8, 27_28; ../statics-typing.stx/#TRUE line 14_61, 30_32, 42_40, 44_58"><span class="token sort_Id">TRUE</span></button> <span class="operator">:</span> <span class="cons_SimpleSort"><a href="#TYPE_BOOL_6_9" id="TYPE_BOOL_10_16" title="a reference to a single-file definition"><span class="token sort_Id">TYPE_BOOL</span></a></span></span>

<span class="keyword">rules</span>

    <button class="modal-open" id="forall_14_5" title="a definition with multiple references" data-urls="#forall line 15_5, 16_5, 17_5, 17_28; ../statics-typing.stx/#forall line 36_72"><span class="token sort_Id">forall</span></button> <span class="operator">:</span> <span class="keyword">list</span><span class="operator">(</span><span class="cons_SimpleSort"><a href="#TYPE_BOOL_6_9" id="TYPE_BOOL_14_19" title="a reference to a single-file definition"><span class="token sort_Id">TYPE_BOOL</span></a></span><span class="operator">)</span> <span class="operator">-&gt;</span> <span class="cons_SimpleSort"><a href="#TYPE_BOOL_6_9" id="TYPE_BOOL_14_33" title="a reference to a single-file definition"><span class="token sort_Id">TYPE_BOOL</span></a></span>
    <a href="#forall_14_5" id="forall_15_5" title="a reference to a single-file definition"><span class="token sort_Id">forall</span></a><span class="operator">([]</span>          <span class="operator">)</span> <span class="operator">=</span> <span class="cons_Op"><a href="#TRUE_10_9" id="TRUE_15_28" title="a reference to a single-file definition"><span class="token sort_Id">TRUE</span></a><span class="operator">()</span></span><span class="operator">.</span>
    <a href="#forall_14_5" id="forall_16_5" title="a reference to a single-file definition"><span class="token sort_Id">forall</span></a><span class="operator">([</span><span class="cons_Op"><a href="#FALSE_9_9" id="FALSE_16_13" title="a reference to a single-file definition"><span class="token sort_Id">FALSE</span></a><span class="operator">()</span></span><span class="operator">|</span><span class="cons_Var"><span id="Ts_16_21" title="a definition with no references"><span class="token sort_Id">Ts</span></span></span><span class="operator">])</span> <span class="operator">=</span> <span class="cons_Op"><a href="#FALSE_9_9" id="FALSE_16_28" title="a reference to a single-file definition"><span class="token sort_Id">FALSE</span></a><span class="operator">()</span></span><span class="operator">.</span>
    <a href="#forall_14_5" id="forall_17_5" title="a reference to a single-file definition"><span class="token sort_Id">forall</span></a><span class="operator">([</span><span class="cons_Op"><a href="#TRUE_10_9" id="TRUE_17_13" title="a reference to a single-file definition"><span class="token sort_Id">TRUE</span></a><span class="operator">()</span></span> <span class="operator">|</span><span class="cons_Var"><span id="Ts_17_21" title="a definition with no references"><span class="token sort_Id">Ts</span></span></span><span class="operator">])</span> <span class="operator">=</span> <a href="#forall_14_5" id="forall_17_28" title="a reference to a single-file definition"><span class="token sort_Id">forall</span></a><span class="operator">(</span><span class="cons_Var">Ts</span><span class="operator">).</span>

    <button class="modal-open" id="bool_and_19_5" title="a definition with multiple references" data-urls="#bool_and line 20_5, 21_5"><span class="token sort_Id">bool_and</span></button> <span class="operator">:</span> <span class="cons_SimpleSort"><a href="#TYPE_BOOL_6_9" id="TYPE_BOOL_19_16" title="a reference to a single-file definition"><span class="token sort_Id">TYPE_BOOL</span></a></span> <span class="operator">*</span> <span class="cons_SimpleSort"><a href="#TYPE_BOOL_6_9" id="TYPE_BOOL_19_28" title="a reference to a single-file definition"><span class="token sort_Id">TYPE_BOOL</span></a></span> <span class="operator">-&gt;</span> <span class="cons_SimpleSort"><a href="#TYPE_BOOL_6_9" id="TYPE_BOOL_19_41" title="a reference to a single-file definition"><span class="token sort_Id">TYPE_BOOL</span></a></span>
    <a href="#bool_and_19_5" id="bool_and_20_5" title="a reference to a single-file definition"><span class="token sort_Id">bool_and</span></a><span class="operator">(</span><span class="cons_Op"><a href="#FALSE_9_9" id="FALSE_20_14" title="a reference to a single-file definition"><span class="token sort_Id">FALSE</span></a><span class="operator">()</span></span><span class="operator">,</span> <span class="operator">_</span>      <span class="operator">)</span> <span class="operator">=</span> <span class="cons_Op"><a href="#FALSE_9_9" id="FALSE_20_34" title="a reference to a single-file definition"><span class="token sort_Id">FALSE</span></a><span class="operator">()</span></span><span class="operator">.</span>
    <a href="#bool_and_19_5" id="bool_and_21_5" title="a reference to a single-file definition"><span class="token sort_Id">bool_and</span></a><span class="operator">(</span><span class="cons_Op"><a href="#TRUE_10_9" id="TRUE_21_14" title="a reference to a single-file definition"><span class="token sort_Id">TRUE</span></a><span class="operator">()</span></span> <span class="operator">,</span> <span class="cons_Var"><span id="x_21_23" title="a definition with no references"><span class="token sort_Id">x</span></span></span>      <span class="operator">)</span> <span class="operator">=</span> <span class="cons_Var">x</span><span class="operator">.</span>
<span class="layout">//  bool_and(_      , FALSE()) = FALSE().</span>
<span class="layout">//  bool_and(x      , TRUE() ) = x.</span>

    <button class="modal-open" id="or_25_5" title="a definition with multiple references" data-urls="#or line 26_5, 27_5; ../statics-typing.stx/#or line 19_34"><span class="token sort_Id">or</span></button> <span class="operator">:</span> <span class="cons_SimpleSort"><a href="#TYPE_BOOL_6_9" id="TYPE_BOOL_25_10" title="a reference to a single-file definition"><span class="token sort_Id">TYPE_BOOL</span></a></span> <span class="operator">*</span> <span class="cons_SimpleSort"><a href="#TYPE_BOOL_6_9" id="TYPE_BOOL_25_22" title="a reference to a single-file definition"><span class="token sort_Id">TYPE_BOOL</span></a></span> <span class="operator">-&gt;</span> <span class="cons_SimpleSort"><a href="#TYPE_BOOL_6_9" id="TYPE_BOOL_25_35" title="a reference to a single-file definition"><span class="token sort_Id">TYPE_BOOL</span></a></span>
    <a href="#or_25_5" id="or_26_5" title="a reference to a single-file definition"><span class="token sort_Id">or</span></a><span class="operator">(</span><span class="cons_Op"><a href="#FALSE_9_9" id="FALSE_26_8" title="a reference to a single-file definition"><span class="token sort_Id">FALSE</span></a><span class="operator">()</span></span><span class="operator">,</span> <span class="cons_Var">x</span>      <span class="operator">)</span> <span class="operator">=</span> <span class="cons_Var"><span id="x_26_28" title="a definition with no references"><span class="token sort_Id">x</span></span></span><span class="operator">.</span>
    <a href="#or_25_5" id="or_27_5" title="a reference to a single-file definition"><span class="token sort_Id">or</span></a><span class="operator">(</span><span class="cons_Op"><a href="#TRUE_10_9" id="TRUE_27_8" title="a reference to a single-file definition"><span class="token sort_Id">TRUE</span></a><span class="operator">()</span></span> <span class="operator">,</span> <span class="operator">_</span>      <span class="operator">)</span> <span class="operator">=</span> <span class="cons_Op"><a href="#TRUE_10_9" id="TRUE_27_28" title="a reference to a single-file definition"><span class="token sort_Id">TRUE</span></a><span class="operator">()</span></span><span class="operator">.</span>
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
