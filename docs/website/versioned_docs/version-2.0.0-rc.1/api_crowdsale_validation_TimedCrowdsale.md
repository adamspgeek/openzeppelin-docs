---
id: version-2.0.0-rc.1-crowdsale_validation_TimedCrowdsale
title: TimedCrowdsale
original_id: crowdsale_validation_TimedCrowdsale
---

<div class="contract-doc"><div class="contract"><h2 class="contract-header"><span class="contract-kind">contract</span> TimedCrowdsale</h2><p class="base-contracts"><span>is</span> <a href="crowdsale_Crowdsale.html">Crowdsale</a></p><p class="description">Crowdsale accepting contributions only within a time frame.</p><div class="source">Source: <a href="https://github.com/OpenZeppelin/zeppelin-solidity/blob/v2.0.0-rc.1/contracts/crowdsale/validation/TimedCrowdsale.sol" target="_blank">crowdsale/validation/TimedCrowdsale.sol</a></div></div><div class="index"><h2>Index</h2><ul><li><a href="crowdsale_validation_TimedCrowdsale.html#_preValidatePurchase">_preValidatePurchase</a></li><li><a href="crowdsale_validation_TimedCrowdsale.html#closingTime">closingTime</a></li><li><a href="crowdsale_validation_TimedCrowdsale.html#">fallback</a></li><li><a href="crowdsale_validation_TimedCrowdsale.html#hasClosed">hasClosed</a></li><li><a href="crowdsale_validation_TimedCrowdsale.html#isOpen">isOpen</a></li><li><a href="crowdsale_validation_TimedCrowdsale.html#onlyWhileOpen">onlyWhileOpen</a></li><li><a href="crowdsale_validation_TimedCrowdsale.html#openingTime">openingTime</a></li></ul></div><div class="reference"><h2>Reference</h2><div class="modifiers"><h3>Modifiers</h3><ul><li><div class="item modifier"><span id="onlyWhileOpen" class="anchor-marker"></span><h4 class="name">onlyWhileOpen</h4><div class="body"><code class="signature">modifier <strong>onlyWhileOpen</strong><span>() </span></code><hr/><div class="description"><p>Reverts if not in crowdsale time range.</p></div></div></div></li></ul></div><div class="functions"><h3>Functions</h3><ul><li><div class="item function"><span id="_preValidatePurchase" class="anchor-marker"></span><h4 class="name">_preValidatePurchase</h4><div class="body"><code class="signature">function <strong>_preValidatePurchase</strong><span>(address beneficiary, uint256 weiAmount) </span><span>internal </span></code><hr/><div class="description"><p>Extend parent behavior requiring to be within contributing period.</p></div><dl><dt><span class="label-modifiers">Modifiers:</span></dt><dd><a href="crowdsale_validation_TimedCrowdsale.html#onlyWhileOpen">onlyWhileOpen </a></dd><dt><span class="label-parameters">Parameters:</span></dt><dd><div><code>beneficiary</code> - Token purchaser</div><div><code>weiAmount</code> - Amount of wei contributed</div></dd></dl></div></div></li><li><div class="item function"><span id="closingTime" class="anchor-marker"></span><h4 class="name">closingTime</h4><div class="body"><code class="signature">function <strong>closingTime</strong><span>() </span><span>public </span><span>view </span><span>returns  (uint256) </span></code><hr/><dl><dt><span class="label-return">Returns:</span></dt><dd>the crowdsale closing time.</dd></dl></div></div></li><li><div class="item function"><span id="fallback" class="anchor-marker"></span><h4 class="name">fallback</h4><div class="body"><code class="signature">function <strong></strong><span>(uint256 openingTime, uint256 closingTime) </span><span>public </span></code><hr/><div class="description"><p>Constructor, takes crowdsale opening and closing times.</p></div><dl><dt><span class="label-parameters">Parameters:</span></dt><dd><div><code>openingTime</code> - Crowdsale opening time</div><div><code>closingTime</code> - Crowdsale closing time</div></dd></dl></div></div></li><li><div class="item function"><span id="hasClosed" class="anchor-marker"></span><h4 class="name">hasClosed</h4><div class="body"><code class="signature">function <strong>hasClosed</strong><span>() </span><span>public </span><span>view </span><span>returns  (bool) </span></code><hr/><div class="description"><p>Checks whether the period in which the crowdsale is open has already elapsed.</p></div><dl><dt><span class="label-return">Returns:</span></dt><dd>Whether crowdsale period has elapsed</dd></dl></div></div></li><li><div class="item function"><span id="isOpen" class="anchor-marker"></span><h4 class="name">isOpen</h4><div class="body"><code class="signature">function <strong>isOpen</strong><span>() </span><span>public </span><span>view </span><span>returns  (bool) </span></code><hr/><dl><dt><span class="label-return">Returns:</span></dt><dd>true if the crowdsale is open, false otherwise.</dd></dl></div></div></li><li><div class="item function"><span id="openingTime" class="anchor-marker"></span><h4 class="name">openingTime</h4><div class="body"><code class="signature">function <strong>openingTime</strong><span>() </span><span>public </span><span>view </span><span>returns  (uint256) </span></code><hr/><dl><dt><span class="label-return">Returns:</span></dt><dd>the crowdsale opening time.</dd></dl></div></div></li></ul></div></div></div>