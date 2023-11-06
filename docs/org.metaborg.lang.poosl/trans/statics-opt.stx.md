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
<td class="code"><pre><code><span class="keyword">module</span> <button class="modal-open" id="statics-opt_0_7" title="Multi-file links" data-urls="../statics-comm.stx/#statics-opt_5_4 ../statics-expr-stat.stx/#statics-opt_5_4 ../statics.stx/#statics-opt_8_4"><span class="token sort_Id">statics-opt</span></button>

<span class="keyword">imports</span>
    <a href="../../src-gen/statix/signatures/Poosl-sig.stx/#signatures/Poosl-sig_0_7" id="signatures/Poosl-sig_3_4" title="Defined at ../../src-gen/statix/signatures/Poosl-sig.stx line 1"><span class="token sort_Id">signatures/Poosl-sig</span></a>
    <a href="../../src-gen/statix/signatures/Common-sig.stx/#signatures/Common-sig_0_7" id="signatures/Common-sig_4_4" title="Defined at ../../src-gen/statix/signatures/Common-sig.stx line 1"><span class="token sort_Id">signatures/Common-sig</span></a>

<span class="keyword">rules</span>   <span class="layout">// === Strip optional lists =======</span>

    <button class="modal-open" id="stripOptExpressionList_8_4" title="Multi-file links" data-urls="#stripOptExpressionList_9_4 ../statics-expr-stat.stx/#stripOptExpressionList_71_71"><span class="token sort_Id">stripOptExpressionList</span></button> <span class="operator">:</span> <span class="cons_SimpleSort"><a href="../../src-gen/statix/signatures/ExprStat-sig.stx/#OptExpressionList_19_4" id="OptExpressionList_8_29" title="Defined at ../../src-gen/statix/signatures/ExprStat-sig.stx line 20"><span class="token sort_Id">OptExpressionList</span></a></span> <span class="operator">-&gt;</span> <span class="keyword">list</span><span class="operator">(</span><span class="cons_SimpleSort"><a href="../../src-gen/statix/signatures/ExprStat-sig.stx/#Expression_16_4" id="Expression_8_55" title="Defined at ../../src-gen/statix/signatures/ExprStat-sig.stx line 17"><span class="token sort_Id">Expression</span></a></span><span class="operator">)</span>
    <a href="#stripOptExpressionList_8_4" id="stripOptExpressionList_9_4" title="Defined at line 9"><span class="token sort_Id">stripOptExpressionList</span></a><span class="operator">(</span><span class="cons_Op"><a href="../../src-gen/statix/signatures/ExprStat-sig.stx/#NoExpressions_125_4" id="NoExpressions_9_27" title="Defined at ../../src-gen/statix/signatures/ExprStat-sig.stx line 126"><span class="token sort_Id">NoExpressions</span></a>()</span><span class="operator">)</span> <span class="operator">=</span> <span class="operator">[].</span>
    <a href="#stripOptExpressionList_8_4" id="stripOptExpressionList_10_4" title="Defined at line 9"><span class="token sort_Id">stripOptExpressionList</span></a><span class="operator">(</span><span class="cons_Op"><a href="../../src-gen/statix/signatures/ExprStat-sig.stx/#Expressions_124_4" id="Expressions_10_27" title="Defined at ../../src-gen/statix/signatures/ExprStat-sig.stx line 125"><span class="token sort_Id">Expressions</span></a><span class="operator">(</span><span class="cons_Var">exprs</span>)</span><span class="operator">)</span> <span class="operator">=</span> <span class="cons_Var"><span id="exprs_10_49" title="Not referenced locally, nor via imports"><span class="token sort_Id">exprs</span></span></span><span class="operator">.</span>

    <button class="modal-open" id="stripOptInstanceParameterList_12_4" title="Multi-file links" data-urls="#stripOptInstanceParameterList_13_4 ../statics-comm.stx/#stripOptInstanceParameterList_38_77"><span class="token sort_Id">stripOptInstanceParameterList</span></button> <span class="operator">:</span> <span class="cons_SimpleSort"><a href="../../src-gen/statix/signatures/Poosl-sig.stx/#OptInstanceParameterList_39_4" id="OptInstanceParameterList_12_36" title="Defined at ../../src-gen/statix/signatures/Poosl-sig.stx line 40"><span class="token sort_Id">OptInstanceParameterList</span></a></span> <span class="operator">-&gt;</span> <span class="keyword">list</span><span class="operator">(</span><span class="cons_SimpleSort"><a href="../../src-gen/statix/signatures/Poosl-sig.stx/#InstanceParameter_40_4" id="InstanceParameter_12_69" title="Defined at ../../src-gen/statix/signatures/Poosl-sig.stx line 41"><span class="token sort_Id">InstanceParameter</span></a></span><span class="operator">)</span>
    <a href="#stripOptInstanceParameterList_12_4" id="stripOptInstanceParameterList_13_4" title="Defined at line 13"><span class="token sort_Id">stripOptInstanceParameterList</span></a><span class="operator">(</span><span class="cons_Op"><a href="../../src-gen/statix/signatures/Poosl-sig.stx/#NoInstanceParameters_140_4" id="NoInstanceParameters_13_34" title="Defined at ../../src-gen/statix/signatures/Poosl-sig.stx line 141"><span class="token sort_Id">NoInstanceParameters</span></a>()</span><span class="operator">)</span> <span class="operator">=</span> <span class="operator">[].</span>
    <a href="#stripOptInstanceParameterList_12_4" id="stripOptInstanceParameterList_14_4" title="Defined at line 13"><span class="token sort_Id">stripOptInstanceParameterList</span></a><span class="operator">(</span><span class="cons_Op"><a href="../../src-gen/statix/signatures/Poosl-sig.stx/#InstanceParameters_139_4" id="InstanceParameters_14_34" title="Defined at ../../src-gen/statix/signatures/Poosl-sig.stx line 140"><span class="token sort_Id">InstanceParameters</span></a><span class="operator">(</span><span class="cons_Var"><span id="parameters_14_53" title="Not referenced locally, nor via imports"><span class="token sort_Id">parameters</span></span></span>)</span><span class="operator">)</span> <span class="operator">=</span> <span class="cons_Var">parameters</span><span class="operator">.</span>

    <button class="modal-open" id="stripOptLocalVariablesList_16_4" title="Multi-file links" data-urls="#stripOptLocalVariablesList_17_4 ../statics.stx/#stripOptLocalVariablesList_99_33"><span class="token sort_Id">stripOptLocalVariablesList</span></button> <span class="operator">:</span> <span class="cons_SimpleSort"><a href="../../src-gen/statix/signatures/Poosl-sig.stx/#OptLocalVariableList_29_4" id="OptLocalVariableList_16_33" title="Defined at ../../src-gen/statix/signatures/Poosl-sig.stx line 30"><span class="token sort_Id">OptLocalVariableList</span></a></span> <span class="operator">-&gt;</span> <span class="keyword">list</span><span class="operator">(</span><span class="cons_SimpleSort"><a href="../../src-gen/statix/signatures/Poosl-sig.stx/#Declaration_23_4" id="Declaration_16_62" title="Defined at ../../src-gen/statix/signatures/Poosl-sig.stx line 24"><span class="token sort_Id">Declaration</span></a></span><span class="operator">)</span>
    <a href="#stripOptLocalVariablesList_16_4" id="stripOptLocalVariablesList_17_4" title="Defined at line 17"><span class="token sort_Id">stripOptLocalVariablesList</span></a><span class="operator">(</span><span class="cons_Op"><a href="../../src-gen/statix/signatures/Poosl-sig.stx/#NoLocalVariables_124_4" id="NoLocalVariables_17_31" title="Defined at ../../src-gen/statix/signatures/Poosl-sig.stx line 125"><span class="token sort_Id">NoLocalVariables</span></a>()</span><span class="operator">)</span> <span class="operator">=</span> <span class="operator">[].</span>
    <a href="#stripOptLocalVariablesList_16_4" id="stripOptLocalVariablesList_18_4" title="Defined at line 17"><span class="token sort_Id">stripOptLocalVariablesList</span></a><span class="operator">(</span><span class="cons_Op"><a href="../../src-gen/statix/signatures/Poosl-sig.stx/#LocalVariables_123_4" id="LocalVariables_18_31" title="Defined at ../../src-gen/statix/signatures/Poosl-sig.stx line 124"><span class="token sort_Id">LocalVariables</span></a><span class="operator">(</span><span class="cons_Var">declarations</span>)</span><span class="operator">)</span> <span class="operator">=</span> <span class="cons_Var"><span id="declarations_18_63" title="Not referenced locally, nor via imports"><span class="token sort_Id">declarations</span></span></span><span class="operator">.</span>

    <button class="modal-open" id="stripOptParameterList_20_4" title="Multi-file links" data-urls="#stripOptParameterList_21_4 ../statics.stx/#stripOptParameterList_49_35"><span class="token sort_Id">stripOptParameterList</span></button> <span class="operator">:</span> <span class="cons_SimpleSort"><a href="../../src-gen/statix/signatures/Poosl-sig.stx/#OptParameterList_28_4" id="OptParameterList_20_28" title="Defined at ../../src-gen/statix/signatures/Poosl-sig.stx line 29"><span class="token sort_Id">OptParameterList</span></a></span> <span class="operator">-&gt;</span> <span class="keyword">list</span><span class="operator">(</span><span class="cons_SimpleSort"><a href="../../src-gen/statix/signatures/Poosl-sig.stx/#Declaration_23_4" id="Declaration_20_53" title="Defined at ../../src-gen/statix/signatures/Poosl-sig.stx line 24"><span class="token sort_Id">Declaration</span></a></span><span class="operator">)</span>
    <a href="#stripOptParameterList_20_4" id="stripOptParameterList_21_4" title="Defined at line 21"><span class="token sort_Id">stripOptParameterList</span></a><span class="operator">(</span><span class="cons_Op"><a href="../../src-gen/statix/signatures/Poosl-sig.stx/#NoParameters_122_4" id="NoParameters_21_26" title="Defined at ../../src-gen/statix/signatures/Poosl-sig.stx line 123"><span class="token sort_Id">NoParameters</span></a>()</span><span class="operator">)</span> <span class="operator">=</span> <span class="operator">[].</span>
    <a href="#stripOptParameterList_20_4" id="stripOptParameterList_22_4" title="Defined at line 21"><span class="token sort_Id">stripOptParameterList</span></a><span class="operator">(</span><span class="cons_Op"><a href="../../src-gen/statix/signatures/Poosl-sig.stx/#Parameters_121_4" id="Parameters_22_26" title="Defined at ../../src-gen/statix/signatures/Poosl-sig.stx line 122"><span class="token sort_Id">Parameters</span></a><span class="operator">(</span><span class="cons_Var"><span id="declarations_22_37" title="Not referenced locally, nor via imports"><span class="token sort_Id">declarations</span></span></span>)</span><span class="operator">)</span> <span class="operator">=</span> <span class="cons_Var">declarations</span><span class="operator">.</span>

    <button class="modal-open" id="stripOptVariableList_24_4" title="Multi-file links" data-urls="#stripOptVariableList_25_4 ../statics-expr-stat.stx/#stripOptVariableList_77_50"><span class="token sort_Id">stripOptVariableList</span></button> <span class="operator">:</span> <span class="cons_SimpleSort"><a href="../../src-gen/statix/signatures/ExprStat-sig.stx/#OptVariableList_20_4" id="OptVariableList_24_27" title="Defined at ../../src-gen/statix/signatures/ExprStat-sig.stx line 21"><span class="token sort_Id">OptVariableList</span></a></span> <span class="operator">-&gt;</span> <span class="keyword">list</span><span class="operator">(</span><span class="cons_StringSort">string</span><span class="operator">)</span>
    <a href="#stripOptVariableList_24_4" id="stripOptVariableList_25_4" title="Defined at line 25"><span class="token sort_Id">stripOptVariableList</span></a><span class="operator">(</span><span class="cons_Op"><a href="../../src-gen/statix/signatures/ExprStat-sig.stx/#NoVariables_94_4" id="NoVariables_25_25" title="Defined at ../../src-gen/statix/signatures/ExprStat-sig.stx line 95"><span class="token sort_Id">NoVariables</span></a>()</span><span class="operator">)</span> <span class="operator">=</span> <span class="operator">[].</span>
    <a href="#stripOptVariableList_24_4" id="stripOptVariableList_26_4" title="Defined at line 25"><span class="token sort_Id">stripOptVariableList</span></a><span class="operator">(</span><span class="cons_Op"><a href="../../src-gen/statix/signatures/ExprStat-sig.stx/#Variables_93_4" id="Variables_26_25" title="Defined at ../../src-gen/statix/signatures/ExprStat-sig.stx line 94"><span class="token sort_Id">Variables</span></a><span class="operator">(</span><span class="cons_Var"><span id="vars_26_35" title="Not referenced locally, nor via imports"><span class="token sort_Id">vars</span></span></span>)</span><span class="operator">)</span> <span class="operator">=</span> <span class="cons_Var">vars</span><span class="operator">.</span>

</code></pre></td></tr></tbody></table></div>

<div id="modal">
  <div id="modal-content">
    <span id="modal-close">&times;</span>
    <h2 id="modal-h2"></h2>
    <ul id="modal-ul"></ul>
  </div>
</div>
