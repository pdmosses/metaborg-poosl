---
title: statics-opt.stx
hide:
  - toc
---

# `statics-opt.stx`

:simple-github: [pdmosses/metaborg-poosl/org.metaborg.lang.poosl/trans/statics-opt.stx]

[pdmosses/metaborg-poosl/org.metaborg.lang.poosl/trans/statics-opt.stx]: https://github.com/pdmosses/metaborg-poosl/blob/master/org.metaborg.lang.poosl/trans/statics-opt.stx "The source file on GitHub"

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
</pre></div></td>
<td class="code"><pre><code><span class="keyword">module</span> <button class="modal-open" id="statics-opt_1_8" title="Multi-file references" data-urls="../statics-comm.stx/#statics-opt_6_5 line 6; ../statics-expr-stat.stx/#statics-opt_6_5 line 6; ../statics.stx/#statics-opt_9_5 line 9"><span class="token sort_Id">statics-opt</span></button>

<span class="keyword">imports</span>
    <a href="../../src-gen/statix/signatures/Poosl-sig.stx/#signatures/Poosl-sig_1_8" id="signatures/Poosl-sig_4_5" title="Defined at ../../src-gen/statix/signatures/Poosl-sig.stx line 1"><span class="token sort_Id">signatures/Poosl-sig</span></a>
    <a href="../../src-gen/statix/signatures/Common-sig.stx/#signatures/Common-sig_1_8" id="signatures/Common-sig_5_5" title="Defined at ../../src-gen/statix/signatures/Common-sig.stx line 1"><span class="token sort_Id">signatures/Common-sig</span></a>

<span class="keyword">rules</span>   <span class="layout">// === Strip optional lists =======</span>

    <button class="modal-open" id="stripOptExpressionList_9_5" title="Multi-file references" data-urls="#stripOptExpressionList_10_5 line 10, 11; ../statics-expr-stat.stx/#stripOptExpressionList_72_72 line 72, 167"><span class="token sort_Id">stripOptExpressionList</span></button> <span class="operator">:</span> <span class="cons_SimpleSort"><a href="../../src-gen/statix/signatures/ExprStat-sig.stx/#OptExpressionList_20_5" id="OptExpressionList_9_30" title="Defined at ../../src-gen/statix/signatures/ExprStat-sig.stx line 20"><span class="token sort_Id">OptExpressionList</span></a></span> <span class="operator">-&gt;</span> <span class="keyword">list</span><span class="operator">(</span><span class="cons_SimpleSort"><a href="../../src-gen/statix/signatures/ExprStat-sig.stx/#Expression_17_5" id="Expression_9_56" title="Defined at ../../src-gen/statix/signatures/ExprStat-sig.stx line 17"><span class="token sort_Id">Expression</span></a></span><span class="operator">)</span>
    <a href="#stripOptExpressionList_9_5" id="stripOptExpressionList_10_5" title="Defined at line 9"><span class="token sort_Id">stripOptExpressionList</span></a><span class="operator">(</span><span class="cons_Op"><a href="../../src-gen/statix/signatures/ExprStat-sig.stx/#NoExpressions_126_5" id="NoExpressions_10_28" title="Defined at ../../src-gen/statix/signatures/ExprStat-sig.stx line 126"><span class="token sort_Id">NoExpressions</span></a>()</span><span class="operator">)</span> <span class="operator">=</span> <span class="operator">[].</span>
    <a href="#stripOptExpressionList_9_5" id="stripOptExpressionList_11_5" title="Defined at line 9"><span class="token sort_Id">stripOptExpressionList</span></a><span class="operator">(</span><span class="cons_Op"><a href="../../src-gen/statix/signatures/ExprStat-sig.stx/#Expressions_125_5" id="Expressions_11_28" title="Defined at ../../src-gen/statix/signatures/ExprStat-sig.stx line 125"><span class="token sort_Id">Expressions</span></a><span class="operator">(</span><span class="cons_Var"><span id="exprs_11_40" title="Not referenced"><span class="token sort_Id">exprs</span></span></span>)</span><span class="operator">)</span> <span class="operator">=</span> <span class="cons_Var">exprs</span><span class="operator">.</span>

    <button class="modal-open" id="stripOptInstanceParameterList_13_5" title="Multi-file references" data-urls="#stripOptInstanceParameterList_14_5 line 14, 15; ../statics-comm.stx/#stripOptInstanceParameterList_39_78 line 39"><span class="token sort_Id">stripOptInstanceParameterList</span></button> <span class="operator">:</span> <span class="cons_SimpleSort"><a href="../../src-gen/statix/signatures/Poosl-sig.stx/#OptInstanceParameterList_40_5" id="OptInstanceParameterList_13_37" title="Defined at ../../src-gen/statix/signatures/Poosl-sig.stx line 40"><span class="token sort_Id">OptInstanceParameterList</span></a></span> <span class="operator">-&gt;</span> <span class="keyword">list</span><span class="operator">(</span><span class="cons_SimpleSort"><a href="../../src-gen/statix/signatures/Poosl-sig.stx/#InstanceParameter_41_5" id="InstanceParameter_13_70" title="Defined at ../../src-gen/statix/signatures/Poosl-sig.stx line 41"><span class="token sort_Id">InstanceParameter</span></a></span><span class="operator">)</span>
    <a href="#stripOptInstanceParameterList_13_5" id="stripOptInstanceParameterList_14_5" title="Defined at line 13"><span class="token sort_Id">stripOptInstanceParameterList</span></a><span class="operator">(</span><span class="cons_Op"><a href="../../src-gen/statix/signatures/Poosl-sig.stx/#NoInstanceParameters_141_5" id="NoInstanceParameters_14_35" title="Defined at ../../src-gen/statix/signatures/Poosl-sig.stx line 141"><span class="token sort_Id">NoInstanceParameters</span></a>()</span><span class="operator">)</span> <span class="operator">=</span> <span class="operator">[].</span>
    <a href="#stripOptInstanceParameterList_13_5" id="stripOptInstanceParameterList_15_5" title="Defined at line 13"><span class="token sort_Id">stripOptInstanceParameterList</span></a><span class="operator">(</span><span class="cons_Op"><a href="../../src-gen/statix/signatures/Poosl-sig.stx/#InstanceParameters_140_5" id="InstanceParameters_15_35" title="Defined at ../../src-gen/statix/signatures/Poosl-sig.stx line 140"><span class="token sort_Id">InstanceParameters</span></a><span class="operator">(</span><span class="cons_Var"><span id="parameters_15_54" title="Not referenced"><span class="token sort_Id">parameters</span></span></span>)</span><span class="operator">)</span> <span class="operator">=</span> <span class="cons_Var">parameters</span><span class="operator">.</span>

    <button class="modal-open" id="stripOptLocalVariablesList_17_5" title="Multi-file references" data-urls="#stripOptLocalVariablesList_18_5 line 18, 19; ../statics.stx/#stripOptLocalVariablesList_100_34 line 100, 110, 117, 126"><span class="token sort_Id">stripOptLocalVariablesList</span></button> <span class="operator">:</span> <span class="cons_SimpleSort"><a href="../../src-gen/statix/signatures/Poosl-sig.stx/#OptLocalVariableList_30_5" id="OptLocalVariableList_17_34" title="Defined at ../../src-gen/statix/signatures/Poosl-sig.stx line 30"><span class="token sort_Id">OptLocalVariableList</span></a></span> <span class="operator">-&gt;</span> <span class="keyword">list</span><span class="operator">(</span><span class="cons_SimpleSort"><a href="../../src-gen/statix/signatures/Poosl-sig.stx/#Declaration_24_5" id="Declaration_17_63" title="Defined at ../../src-gen/statix/signatures/Poosl-sig.stx line 24"><span class="token sort_Id">Declaration</span></a></span><span class="operator">)</span>
    <a href="#stripOptLocalVariablesList_17_5" id="stripOptLocalVariablesList_18_5" title="Defined at line 17"><span class="token sort_Id">stripOptLocalVariablesList</span></a><span class="operator">(</span><span class="cons_Op"><a href="../../src-gen/statix/signatures/Poosl-sig.stx/#NoLocalVariables_125_5" id="NoLocalVariables_18_32" title="Defined at ../../src-gen/statix/signatures/Poosl-sig.stx line 125"><span class="token sort_Id">NoLocalVariables</span></a>()</span><span class="operator">)</span> <span class="operator">=</span> <span class="operator">[].</span>
    <a href="#stripOptLocalVariablesList_17_5" id="stripOptLocalVariablesList_19_5" title="Defined at line 17"><span class="token sort_Id">stripOptLocalVariablesList</span></a><span class="operator">(</span><span class="cons_Op"><a href="../../src-gen/statix/signatures/Poosl-sig.stx/#LocalVariables_124_5" id="LocalVariables_19_32" title="Defined at ../../src-gen/statix/signatures/Poosl-sig.stx line 124"><span class="token sort_Id">LocalVariables</span></a><span class="operator">(</span><span class="cons_Var"><span id="declarations_19_47" title="Not referenced"><span class="token sort_Id">declarations</span></span></span>)</span><span class="operator">)</span> <span class="operator">=</span> <span class="cons_Var">declarations</span><span class="operator">.</span>

    <button class="modal-open" id="stripOptParameterList_21_5" title="Multi-file references" data-urls="#stripOptParameterList_22_5 line 22, 23; ../statics.stx/#stripOptParameterList_50_36 line 50, 61, 107, 132"><span class="token sort_Id">stripOptParameterList</span></button> <span class="operator">:</span> <span class="cons_SimpleSort"><a href="../../src-gen/statix/signatures/Poosl-sig.stx/#OptParameterList_29_5" id="OptParameterList_21_29" title="Defined at ../../src-gen/statix/signatures/Poosl-sig.stx line 29"><span class="token sort_Id">OptParameterList</span></a></span> <span class="operator">-&gt;</span> <span class="keyword">list</span><span class="operator">(</span><span class="cons_SimpleSort"><a href="../../src-gen/statix/signatures/Poosl-sig.stx/#Declaration_24_5" id="Declaration_21_54" title="Defined at ../../src-gen/statix/signatures/Poosl-sig.stx line 24"><span class="token sort_Id">Declaration</span></a></span><span class="operator">)</span>
    <a href="#stripOptParameterList_21_5" id="stripOptParameterList_22_5" title="Defined at line 21"><span class="token sort_Id">stripOptParameterList</span></a><span class="operator">(</span><span class="cons_Op"><a href="../../src-gen/statix/signatures/Poosl-sig.stx/#NoParameters_123_5" id="NoParameters_22_27" title="Defined at ../../src-gen/statix/signatures/Poosl-sig.stx line 123"><span class="token sort_Id">NoParameters</span></a>()</span><span class="operator">)</span> <span class="operator">=</span> <span class="operator">[].</span>
    <a href="#stripOptParameterList_21_5" id="stripOptParameterList_23_5" title="Defined at line 21"><span class="token sort_Id">stripOptParameterList</span></a><span class="operator">(</span><span class="cons_Op"><a href="../../src-gen/statix/signatures/Poosl-sig.stx/#Parameters_122_5" id="Parameters_23_27" title="Defined at ../../src-gen/statix/signatures/Poosl-sig.stx line 122"><span class="token sort_Id">Parameters</span></a><span class="operator">(</span><span class="cons_Var"><span id="declarations_23_38" title="Not referenced"><span class="token sort_Id">declarations</span></span></span>)</span><span class="operator">)</span> <span class="operator">=</span> <span class="cons_Var">declarations</span><span class="operator">.</span>

    <button class="modal-open" id="stripOptVariableList_25_5" title="Multi-file references" data-urls="#stripOptVariableList_26_5 line 26, 27; ../statics-expr-stat.stx/#stripOptVariableList_78_51 line 78"><span class="token sort_Id">stripOptVariableList</span></button> <span class="operator">:</span> <span class="cons_SimpleSort"><a href="../../src-gen/statix/signatures/ExprStat-sig.stx/#OptVariableList_21_5" id="OptVariableList_25_28" title="Defined at ../../src-gen/statix/signatures/ExprStat-sig.stx line 21"><span class="token sort_Id">OptVariableList</span></a></span> <span class="operator">-&gt;</span> <span class="keyword">list</span><span class="operator">(</span><span class="cons_StringSort">string</span><span class="operator">)</span>
    <a href="#stripOptVariableList_25_5" id="stripOptVariableList_26_5" title="Defined at line 25"><span class="token sort_Id">stripOptVariableList</span></a><span class="operator">(</span><span class="cons_Op"><a href="../../src-gen/statix/signatures/ExprStat-sig.stx/#NoVariables_95_5" id="NoVariables_26_26" title="Defined at ../../src-gen/statix/signatures/ExprStat-sig.stx line 95"><span class="token sort_Id">NoVariables</span></a>()</span><span class="operator">)</span> <span class="operator">=</span> <span class="operator">[].</span>
    <a href="#stripOptVariableList_25_5" id="stripOptVariableList_27_5" title="Defined at line 25"><span class="token sort_Id">stripOptVariableList</span></a><span class="operator">(</span><span class="cons_Op"><a href="../../src-gen/statix/signatures/ExprStat-sig.stx/#Variables_94_5" id="Variables_27_26" title="Defined at ../../src-gen/statix/signatures/ExprStat-sig.stx line 94"><span class="token sort_Id">Variables</span></a><span class="operator">(</span><span class="cons_Var">vars</span>)</span><span class="operator">)</span> <span class="operator">=</span> <span class="cons_Var"><span id="vars_27_45" title="Not referenced"><span class="token sort_Id">vars</span></span></span><span class="operator">.</span>

</code></pre></td></tr></tbody></table></div>

<div id="modal">
  <div id="modal-content">
    <span id="modal-close">&times;</span>
    <h2 id="modal-h2"></h2>
    <p  id="modal-p"></p>
    <ul id="modal-ul"></ul>
  </div>
</div>
