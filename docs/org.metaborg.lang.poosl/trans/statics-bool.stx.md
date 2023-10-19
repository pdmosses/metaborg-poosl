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
<td class="code"><pre><code><span class="keyword">module</span> <a href="../statics-typing.stx/#statics-bool_86_98" id="statics-bool_7_19" title="Referenced at ../statics-typing.stx line 6"><span class="token sort_Id">statics-bool</span></a>

<span class="keyword">signature</span>

    <span class="keyword">sorts</span>
        <span class="cons_SortDecl"><a href="#TYPE_BOOL_94_103" id="TYPE_BOOL_50_59" title="Referenced at line 9, 10, 14, 19, 25; ../statics-typing.stx line 18, 28, 35, 41"><span class="token sort_Id">TYPE_BOOL</span></a></span>

    <span class="keyword">constructors</span>
        <span class="cons_OpDecl"><a href="#FALSE_226_231" id="FALSE_86_91" title="Referenced at line 16, 20, 26; ../statics-typing.stx line 31, 43"><span class="token sort_Id">FALSE</span></a> <span class="operator">:</span> <span class="cons_SimpleSort"><a href="#TYPE_BOOL_50_59" id="TYPE_BOOL_94_103" title="Defined at line 6"><span class="token sort_Id">TYPE_BOOL</span></a></span></span>
        <span class="cons_OpDecl"><a href="#TRUE_206_210" id="TRUE_112_116" title="Referenced at line 15, 17, 21, 27; ../statics-typing.stx line 14, 30, 42, 44"><span class="token sort_Id">TRUE</span></a> <span class="operator">:</span> <span class="cons_SimpleSort"><a href="#TYPE_BOOL_50_59" id="TYPE_BOOL_119_128" title="Defined at line 6"><span class="token sort_Id">TYPE_BOOL</span></a></span></span>

<span class="keyword">rules</span>

    <a href="#forall_183_189" id="forall_141_147" title="Referenced at line 15, 16, 17; ../statics-typing.stx line 36"><span class="token sort_Id">forall</span></a> <span class="operator">:</span> <span class="keyword">list</span><span class="operator">(</span><span class="cons_SimpleSort"><a href="#TYPE_BOOL_50_59" id="TYPE_BOOL_155_164" title="Defined at line 6"><span class="token sort_Id">TYPE_BOOL</span></a></span><span class="operator">)</span> <span class="operator">-&gt;</span> <span class="cons_SimpleSort"><a href="#TYPE_BOOL_50_59" id="TYPE_BOOL_169_178" title="Defined at line 6"><span class="token sort_Id">TYPE_BOOL</span></a></span>
    <a href="#forall_141_147" id="forall_183_189" title="Defined at line 14"><span class="token sort_Id">forall</span></a><span class="operator">([]</span>          <span class="operator">)</span> <span class="operator">=</span> <span class="cons_Op"><a href="#TRUE_112_116" id="TRUE_206_210" title="Defined at line 10"><span class="token sort_Id">TRUE</span></a>()</span><span class="operator">.</span>
    <a href="#forall_141_147" id="forall_218_224" title="Defined at line 14"><span class="token sort_Id">forall</span></a><span class="operator">([</span><span class="cons_Op"><a href="#FALSE_86_91" id="FALSE_226_231" title="Defined at line 9"><span class="token sort_Id">FALSE</span></a>()</span><span class="operator">|</span><span class="cons_Var"><span id="Ts_234_236" title="Not referenced locally, nor via imports"><span class="token sort_Id">Ts</span></span></span><span class="operator">])</span> <span class="operator">=</span> <span class="cons_Op"><a href="#FALSE_86_91" id="FALSE_241_246" title="Defined at line 9"><span class="token sort_Id">FALSE</span></a>()</span><span class="operator">.</span>
    <a href="#forall_141_147" id="forall_254_260" title="Defined at line 14"><span class="token sort_Id">forall</span></a><span class="operator">([</span><span class="cons_Op"><a href="#TRUE_112_116" id="TRUE_262_266" title="Defined at line 10"><span class="token sort_Id">TRUE</span></a>()</span> <span class="operator">|</span><span class="cons_Var">Ts</span><span class="operator">])</span> <span class="operator">=</span> <a href="#forall_141_147" id="forall_277_283" title="Defined at line 14"><span class="token sort_Id">forall</span></a><span class="operator">(</span><span class="cons_Var"><span id="Ts_284_286" title="Not referenced locally, nor via imports"><span class="token sort_Id">Ts</span></span></span><span class="operator">).</span>

    <a href="#bool_and_344_352" id="bool_and_294_302" title="Referenced at line 20, 21"><span class="token sort_Id">bool_and</span></a> <span class="operator">:</span> <span class="cons_SimpleSort"><a href="#TYPE_BOOL_50_59" id="TYPE_BOOL_305_314" title="Defined at line 6"><span class="token sort_Id">TYPE_BOOL</span></a></span> <span class="operator">*</span> <span class="cons_SimpleSort"><a href="#TYPE_BOOL_50_59" id="TYPE_BOOL_317_326" title="Defined at line 6"><span class="token sort_Id">TYPE_BOOL</span></a></span> <span class="operator">-&gt;</span> <span class="cons_SimpleSort"><a href="#TYPE_BOOL_50_59" id="TYPE_BOOL_330_339" title="Defined at line 6"><span class="token sort_Id">TYPE_BOOL</span></a></span>
    <a href="#bool_and_294_302" id="bool_and_344_352" title="Defined at line 19"><span class="token sort_Id">bool_and</span></a><span class="operator">(</span><span class="cons_Op"><a href="#FALSE_86_91" id="FALSE_353_358" title="Defined at line 9"><span class="token sort_Id">FALSE</span></a>()</span><span class="operator">,</span> <span class="operator">_</span>      <span class="operator">)</span> <span class="operator">=</span> <span class="cons_Op"><a href="#FALSE_86_91" id="FALSE_373_378" title="Defined at line 9"><span class="token sort_Id">FALSE</span></a>()</span><span class="operator">.</span>
    <a href="#bool_and_294_302" id="bool_and_386_394" title="Defined at line 19"><span class="token sort_Id">bool_and</span></a><span class="operator">(</span><span class="cons_Op"><a href="#TRUE_112_116" id="TRUE_395_399" title="Defined at line 10"><span class="token sort_Id">TRUE</span></a>()</span> <span class="operator">,</span> <span class="cons_Var">x</span>      <span class="operator">)</span> <span class="operator">=</span> <span class="cons_Var"><span id="x_415_416" title="Not referenced locally, nor via imports"><span class="token sort_Id">x</span></span></span><span class="operator">.</span>
<span class="layout">//  bool_and(_      , FALSE()) = FALSE().</span>
<span class="layout">//  bool_and(x      , TRUE() ) = x.</span>

    <a href="#or_545_547" id="or_501_503" title="Referenced at line 26, 27; ../statics-typing.stx line 19"><span class="token sort_Id">or</span></a> <span class="operator">:</span> <span class="cons_SimpleSort"><a href="#TYPE_BOOL_50_59" id="TYPE_BOOL_506_515" title="Defined at line 6"><span class="token sort_Id">TYPE_BOOL</span></a></span> <span class="operator">*</span> <span class="cons_SimpleSort"><a href="#TYPE_BOOL_50_59" id="TYPE_BOOL_518_527" title="Defined at line 6"><span class="token sort_Id">TYPE_BOOL</span></a></span> <span class="operator">-&gt;</span> <span class="cons_SimpleSort"><a href="#TYPE_BOOL_50_59" id="TYPE_BOOL_531_540" title="Defined at line 6"><span class="token sort_Id">TYPE_BOOL</span></a></span>
    <a href="#or_501_503" id="or_545_547" title="Defined at line 25"><span class="token sort_Id">or</span></a><span class="operator">(</span><span class="cons_Op"><a href="#FALSE_86_91" id="FALSE_548_553" title="Defined at line 9"><span class="token sort_Id">FALSE</span></a>()</span><span class="operator">,</span> <span class="cons_Var">x</span>      <span class="operator">)</span> <span class="operator">=</span> <span class="cons_Var"><span id="x_568_569" title="Not referenced locally, nor via imports"><span class="token sort_Id">x</span></span></span><span class="operator">.</span>
    <a href="#or_501_503" id="or_575_577" title="Defined at line 25"><span class="token sort_Id">or</span></a><span class="operator">(</span><span class="cons_Op"><a href="#TRUE_112_116" id="TRUE_578_582" title="Defined at line 10"><span class="token sort_Id">TRUE</span></a>()</span> <span class="operator">,</span> <span class="operator">_</span>      <span class="operator">)</span> <span class="operator">=</span> <span class="cons_Op"><a href="#TRUE_112_116" id="TRUE_598_602" title="Defined at line 10"><span class="token sort_Id">TRUE</span></a>()</span><span class="operator">.</span>
<span class="layout">//  or(x      , FALSE()) = x.</span>
<span class="layout">//  or(_      , TRUE() ) = TRUE().</span>

</code></pre></td></tr></tbody></table></div>