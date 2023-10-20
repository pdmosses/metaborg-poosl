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
<td class="code"><pre><code><span class="keyword">module</span> <a href="../statics-comm.stx/#statics-opt_84_95" id="statics-opt_7_18" title="Referenced at ../statics-comm.stx line 6; ../statics-expr-stat.stx line 6; ../statics.stx line 9"><span class="token sort_Id">statics-opt</span></a>

<span class="keyword">imports</span>
    <a href="../../src-gen/statix/signatures/Poosl-sig.stx/#signatures/Poosl-sig_7_27" id="signatures/Poosl-sig_32_52" title="Defined at ../../src-gen/statix/signatures/Poosl-sig.stx line 1"><span class="token sort_Id">signatures/Poosl-sig</span></a>
    <a href="../../src-gen/statix/signatures/Common-sig.stx/#signatures/Common-sig_7_28" id="signatures/Common-sig_57_78" title="Defined at ../../src-gen/statix/signatures/Common-sig.stx line 1"><span class="token sort_Id">signatures/Common-sig</span></a>

<span class="keyword">rules</span>   <span class="layout">// === Strip optional lists =======</span>

    <a href="#stripOptExpressionList_196_218" id="stripOptExpressionList_129_151" title="Referenced at line 10, 11; ../statics-expr-stat.stx line 72, 167"><span class="token sort_Id">stripOptExpressionList</span></a> <span class="operator">:</span> <span class="cons_SimpleSort"><a href="../../src-gen/statix/signatures/ExprStat-sig.stx/#OptExpressionList_294_311" id="OptExpressionList_154_171" title="Defined at ../../src-gen/statix/signatures/ExprStat-sig.stx line 20"><span class="token sort_Id">OptExpressionList</span></a></span> <span class="operator">-&gt;</span> <span class="keyword">list</span><span class="operator">(</span><span class="cons_SimpleSort"><a href="../../src-gen/statix/signatures/ExprStat-sig.stx/#Expression_241_251" id="Expression_180_190" title="Defined at ../../src-gen/statix/signatures/ExprStat-sig.stx line 17"><span class="token sort_Id">Expression</span></a></span><span class="operator">)</span>
    <a href="#stripOptExpressionList_129_151" id="stripOptExpressionList_196_218" title="Defined at line 9"><span class="token sort_Id">stripOptExpressionList</span></a><span class="operator">(</span><span class="cons_Op"><a href="../../src-gen/statix/signatures/ExprStat-sig.stx/#NoExpressions_5583_5596" id="NoExpressions_219_232" title="Defined at ../../src-gen/statix/signatures/ExprStat-sig.stx line 126"><span class="token sort_Id">NoExpressions</span></a>()</span><span class="operator">)</span> <span class="operator">=</span> <span class="operator">[].</span>
    <a href="#stripOptExpressionList_129_151" id="stripOptExpressionList_246_268" title="Defined at line 9"><span class="token sort_Id">stripOptExpressionList</span></a><span class="operator">(</span><span class="cons_Op"><a href="../../src-gen/statix/signatures/ExprStat-sig.stx/#Expressions_5527_5538" id="Expressions_269_280" title="Defined at ../../src-gen/statix/signatures/ExprStat-sig.stx line 125"><span class="token sort_Id">Expressions</span></a><span class="operator">(</span><span class="cons_Var">exprs</span>)</span><span class="operator">)</span> <span class="operator">=</span> <span class="cons_Var"><span id="exprs_291_296" title="Not referenced locally, nor via imports"><span class="token sort_Id">exprs</span></span></span><span class="operator">.</span>

    <a href="#stripOptInstanceParameterList_391_420" id="stripOptInstanceParameterList_303_332" title="Referenced at line 14, 15; ../statics-comm.stx line 39"><span class="token sort_Id">stripOptInstanceParameterList</span></a> <span class="operator">:</span> <span class="cons_SimpleSort"><a href="../../src-gen/statix/signatures/Poosl-sig.stx/#OptInstanceParameterList_641_665" id="OptInstanceParameterList_335_359" title="Defined at ../../src-gen/statix/signatures/Poosl-sig.stx line 40"><span class="token sort_Id">OptInstanceParameterList</span></a></span> <span class="operator">-&gt;</span> <span class="keyword">list</span><span class="operator">(</span><span class="cons_SimpleSort"><a href="../../src-gen/statix/signatures/Poosl-sig.stx/#InstanceParameter_670_687" id="InstanceParameter_368_385" title="Defined at ../../src-gen/statix/signatures/Poosl-sig.stx line 41"><span class="token sort_Id">InstanceParameter</span></a></span><span class="operator">)</span>
    <a href="#stripOptInstanceParameterList_303_332" id="stripOptInstanceParameterList_391_420" title="Defined at line 13"><span class="token sort_Id">stripOptInstanceParameterList</span></a><span class="operator">(</span><span class="cons_Op"><a href="../../src-gen/statix/signatures/Poosl-sig.stx/#NoInstanceParameters_5572_5592" id="NoInstanceParameters_421_441" title="Defined at ../../src-gen/statix/signatures/Poosl-sig.stx line 141"><span class="token sort_Id">NoInstanceParameters</span></a>()</span><span class="operator">)</span> <span class="operator">=</span> <span class="operator">[].</span>
    <a href="#stripOptInstanceParameterList_303_332" id="stripOptInstanceParameterList_455_484" title="Defined at line 13"><span class="token sort_Id">stripOptInstanceParameterList</span></a><span class="operator">(</span><span class="cons_Op"><a href="../../src-gen/statix/signatures/Poosl-sig.stx/#InstanceParameters_5495_5513" id="InstanceParameters_485_503" title="Defined at ../../src-gen/statix/signatures/Poosl-sig.stx line 140"><span class="token sort_Id">InstanceParameters</span></a><span class="operator">(</span><span class="cons_Var">parameters</span>)</span><span class="operator">)</span> <span class="operator">=</span> <span class="cons_Var"><span id="parameters_519_529" title="Not referenced locally, nor via imports"><span class="token sort_Id">parameters</span></span></span><span class="operator">.</span>

    <a href="#stripOptLocalVariablesList_611_637" id="stripOptLocalVariablesList_536_562" title="Referenced at line 18, 19; ../statics.stx line 100, 110, 117, 126"><span class="token sort_Id">stripOptLocalVariablesList</span></a> <span class="operator">:</span> <span class="cons_SimpleSort"><a href="../../src-gen/statix/signatures/Poosl-sig.stx/#OptLocalVariableList_450_470" id="OptLocalVariableList_565_585" title="Defined at ../../src-gen/statix/signatures/Poosl-sig.stx line 30"><span class="token sort_Id">OptLocalVariableList</span></a></span> <span class="operator">-&gt;</span> <span class="keyword">list</span><span class="operator">(</span><span class="cons_SimpleSort"><a href="../../src-gen/statix/signatures/Poosl-sig.stx/#Declaration_326_337" id="Declaration_594_605" title="Defined at ../../src-gen/statix/signatures/Poosl-sig.stx line 24"><span class="token sort_Id">Declaration</span></a></span><span class="operator">)</span>
    <a href="#stripOptLocalVariablesList_536_562" id="stripOptLocalVariablesList_611_637" title="Defined at line 17"><span class="token sort_Id">stripOptLocalVariablesList</span></a><span class="operator">(</span><span class="cons_Op"><a href="../../src-gen/statix/signatures/Poosl-sig.stx/#NoLocalVariables_4320_4336" id="NoLocalVariables_638_654" title="Defined at ../../src-gen/statix/signatures/Poosl-sig.stx line 125"><span class="token sort_Id">NoLocalVariables</span></a>()</span><span class="operator">)</span> <span class="operator">=</span> <span class="operator">[].</span>
    <a href="#stripOptLocalVariablesList_536_562" id="stripOptLocalVariablesList_668_694" title="Defined at line 17"><span class="token sort_Id">stripOptLocalVariablesList</span></a><span class="operator">(</span><span class="cons_Op"><a href="../../src-gen/statix/signatures/Poosl-sig.stx/#LocalVariables_4257_4271" id="LocalVariables_695_709" title="Defined at ../../src-gen/statix/signatures/Poosl-sig.stx line 124"><span class="token sort_Id">LocalVariables</span></a><span class="operator">(</span><span class="cons_Var">declarations</span>)</span><span class="operator">)</span> <span class="operator">=</span> <span class="cons_Var"><span id="declarations_727_739" title="Not referenced locally, nor via imports"><span class="token sort_Id">declarations</span></span></span><span class="operator">.</span>

    <a href="#stripOptParameterList_812_833" id="stripOptParameterList_746_767" title="Referenced at line 22, 23; ../statics.stx line 50, 61, 107, 132"><span class="token sort_Id">stripOptParameterList</span></a> <span class="operator">:</span> <span class="cons_SimpleSort"><a href="../../src-gen/statix/signatures/Poosl-sig.stx/#OptParameterList_429_445" id="OptParameterList_770_786" title="Defined at ../../src-gen/statix/signatures/Poosl-sig.stx line 29"><span class="token sort_Id">OptParameterList</span></a></span> <span class="operator">-&gt;</span> <span class="keyword">list</span><span class="operator">(</span><span class="cons_SimpleSort"><a href="../../src-gen/statix/signatures/Poosl-sig.stx/#Declaration_326_337" id="Declaration_795_806" title="Defined at ../../src-gen/statix/signatures/Poosl-sig.stx line 24"><span class="token sort_Id">Declaration</span></a></span><span class="operator">)</span>
    <a href="#stripOptParameterList_746_767" id="stripOptParameterList_812_833" title="Defined at line 21"><span class="token sort_Id">stripOptParameterList</span></a><span class="operator">(</span><span class="cons_Op"><a href="../../src-gen/statix/signatures/Poosl-sig.stx/#NoParameters_4221_4233" id="NoParameters_834_846" title="Defined at ../../src-gen/statix/signatures/Poosl-sig.stx line 123"><span class="token sort_Id">NoParameters</span></a>()</span><span class="operator">)</span> <span class="operator">=</span> <span class="operator">[].</span>
    <a href="#stripOptParameterList_746_767" id="stripOptParameterList_860_881" title="Defined at line 21"><span class="token sort_Id">stripOptParameterList</span></a><span class="operator">(</span><span class="cons_Op"><a href="../../src-gen/statix/signatures/Poosl-sig.stx/#Parameters_4166_4176" id="Parameters_882_892" title="Defined at ../../src-gen/statix/signatures/Poosl-sig.stx line 122"><span class="token sort_Id">Parameters</span></a><span class="operator">(</span><span class="cons_Var">declarations</span>)</span><span class="operator">)</span> <span class="operator">=</span> <span class="cons_Var"><span id="declarations_910_922" title="Not referenced locally, nor via imports"><span class="token sort_Id">declarations</span></span></span><span class="operator">.</span>

    <a href="#stripOptVariableList_988_1008" id="stripOptVariableList_929_949" title="Referenced at line 26, 27; ../statics-expr-stat.stx line 78"><span class="token sort_Id">stripOptVariableList</span></a> <span class="operator">:</span> <span class="cons_SimpleSort"><a href="../../src-gen/statix/signatures/ExprStat-sig.stx/#OptVariableList_316_331" id="OptVariableList_952_967" title="Defined at ../../src-gen/statix/signatures/ExprStat-sig.stx line 21"><span class="token sort_Id">OptVariableList</span></a></span> <span class="operator">-&gt;</span> <span class="keyword">list</span><span class="operator">(</span><span class="cons_StringSort">string</span><span class="operator">)</span>
    <a href="#stripOptVariableList_929_949" id="stripOptVariableList_988_1008" title="Defined at line 25"><span class="token sort_Id">stripOptVariableList</span></a><span class="operator">(</span><span class="cons_Op"><a href="../../src-gen/statix/signatures/ExprStat-sig.stx/#NoVariables_3668_3679" id="NoVariables_1009_1020" title="Defined at ../../src-gen/statix/signatures/ExprStat-sig.stx line 95"><span class="token sort_Id">NoVariables</span></a>()</span><span class="operator">)</span> <span class="operator">=</span> <span class="operator">[].</span>
    <a href="#stripOptVariableList_929_949" id="stripOptVariableList_1034_1054" title="Defined at line 25"><span class="token sort_Id">stripOptVariableList</span></a><span class="operator">(</span><span class="cons_Op"><a href="../../src-gen/statix/signatures/ExprStat-sig.stx/#Variables_3624_3633" id="Variables_1055_1064" title="Defined at ../../src-gen/statix/signatures/ExprStat-sig.stx line 94"><span class="token sort_Id">Variables</span></a><span class="operator">(</span><span class="cons_Var"><span id="vars_1065_1069" title="Not referenced locally, nor via imports"><span class="token sort_Id">vars</span></span></span>)</span><span class="operator">)</span> <span class="operator">=</span> <span class="cons_Var">vars</span><span class="operator">.</span>

</code></pre></td></tr></tbody></table></div>