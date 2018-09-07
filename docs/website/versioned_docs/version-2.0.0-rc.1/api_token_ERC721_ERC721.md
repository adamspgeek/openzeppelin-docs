---
id: version-2.0.0-rc.1-token_ERC721_ERC721
title: ERC721
original_id: token_ERC721_ERC721
---

<div class="contract-doc"><div class="contract"><h2 class="contract-header"><span class="contract-kind">contract</span> ERC721</h2><p class="base-contracts"><span>is</span> <a href="introspection_ERC165.html">ERC165</a><span>, </span><a href="token_ERC721_IERC721.html">IERC721</a></p><p class="description">See https://github.com/ethereum/EIPs/blob/master/EIPS/eip-721.md.</p><div class="source">Source: <a href="https://github.com/OpenZeppelin/zeppelin-solidity/blob/v2.0.0-rc.1/contracts/token/ERC721/ERC721.sol" target="_blank">token/ERC721/ERC721.sol</a></div></div><div class="index"><h2>Index</h2><ul><li><a href="token_ERC721_ERC721.html#_addTokenTo">_addTokenTo</a></li><li><a href="token_ERC721_ERC721.html#_burn">_burn</a></li><li><a href="token_ERC721_ERC721.html#_checkAndCallSafeTransfer">_checkAndCallSafeTransfer</a></li><li><a href="token_ERC721_ERC721.html#_clearApproval">_clearApproval</a></li><li><a href="token_ERC721_ERC721.html#_exists">_exists</a></li><li><a href="token_ERC721_ERC721.html#_isApprovedOrOwner">_isApprovedOrOwner</a></li><li><a href="token_ERC721_ERC721.html#_mint">_mint</a></li><li><a href="token_ERC721_ERC721.html#_removeTokenFrom">_removeTokenFrom</a></li><li><a href="token_ERC721_ERC721.html#approve">approve</a></li><li><a href="token_ERC721_ERC721.html#balanceOf">balanceOf</a></li><li><a href="token_ERC721_ERC721.html#">fallback</a></li><li><a href="token_ERC721_ERC721.html#getApproved">getApproved</a></li><li><a href="token_ERC721_ERC721.html#isApprovedForAll">isApprovedForAll</a></li><li><a href="token_ERC721_ERC721.html#ownerOf">ownerOf</a></li><li><a href="token_ERC721_ERC721.html#safeTransferFrom">safeTransferFrom</a></li><li><a href="token_ERC721_ERC721.html#safeTransferFrom">safeTransferFrom</a></li><li><a href="token_ERC721_ERC721.html#setApprovalForAll">setApprovalForAll</a></li><li><a href="token_ERC721_ERC721.html#transferFrom">transferFrom</a></li></ul></div><div class="reference"><h2>Reference</h2><div class="functions"><h3>Functions</h3><ul><li><div class="item function"><span id="_addTokenTo" class="anchor-marker"></span><h4 class="name">_addTokenTo</h4><div class="body"><code class="signature">function <strong>_addTokenTo</strong><span>(address to, uint256 tokenId) </span><span>internal </span></code><hr/><div class="description"><p>Internal function to add a token ID to the list of a given address.</p></div><dl><dt><span class="label-parameters">Parameters:</span></dt><dd><div><code>to</code> - address representing the new owner of the given token ID</div><div><code>tokenId</code> - uint256 ID of the token to be added to the tokens list of the given address</div></dd></dl></div></div></li><li><div class="item function"><span id="_burn" class="anchor-marker"></span><h4 class="name">_burn</h4><div class="body"><code class="signature">function <strong>_burn</strong><span>(address owner, uint256 tokenId) </span><span>internal </span></code><hr/><div class="description"><p>Internal function to burn a specific token Reverts if the token does not exist.</p></div><dl><dt><span class="label-parameters">Parameters:</span></dt><dd><div><code>owner</code> - address</div><div><code>tokenId</code> - uint256 ID of the token being burned by the msg.sender</div></dd></dl></div></div></li><li><div class="item function"><span id="_checkAndCallSafeTransfer" class="anchor-marker"></span><h4 class="name">_checkAndCallSafeTransfer</h4><div class="body"><code class="signature">function <strong>_checkAndCallSafeTransfer</strong><span>(address from, address to, uint256 tokenId, bytes _data) </span><span>internal </span><span>returns  (bool) </span></code><hr/><div class="description"><p>Internal function to invoke `onERC721Received` on a target address The call is not executed if the target address is not a contract.</p></div><dl><dt><span class="label-parameters">Parameters:</span></dt><dd><div><code>from</code> - address representing the previous owner of the given token ID</div><div><code>to</code> - target address that will receive the tokens</div><div><code>tokenId</code> - uint256 ID of the token to be transferred</div><div><code>_data</code> - bytes optional data to send along with the call</div></dd><dt><span class="label-return">Returns:</span></dt><dd>whether the call correctly returned the expected magic value</dd></dl></div></div></li><li><div class="item function"><span id="_clearApproval" class="anchor-marker"></span><h4 class="name">_clearApproval</h4><div class="body"><code class="signature">function <strong>_clearApproval</strong><span>(address owner, uint256 tokenId) </span><span>internal </span></code><hr/><div class="description"><p>Internal function to clear current approval of a given token ID Reverts if the given address is not indeed the owner of the token.</p></div><dl><dt><span class="label-parameters">Parameters:</span></dt><dd><div><code>owner</code> - owner of the token</div><div><code>tokenId</code> - uint256 ID of the token to be transferred</div></dd></dl></div></div></li><li><div class="item function"><span id="_exists" class="anchor-marker"></span><h4 class="name">_exists</h4><div class="body"><code class="signature">function <strong>_exists</strong><span>(uint256 tokenId) </span><span>internal </span><span>view </span><span>returns  (bool) </span></code><hr/><div class="description"><p>Returns whether the specified token exists.</p></div><dl><dt><span class="label-parameters">Parameters:</span></dt><dd><div><code>tokenId</code> - uint256 ID of the token to query the existence of</div></dd><dt><span class="label-return">Returns:</span></dt><dd>whether the token exists</dd></dl></div></div></li><li><div class="item function"><span id="_isApprovedOrOwner" class="anchor-marker"></span><h4 class="name">_isApprovedOrOwner</h4><div class="body"><code class="signature">function <strong>_isApprovedOrOwner</strong><span>(address spender, uint256 tokenId) </span><span>internal </span><span>view </span><span>returns  (bool) </span></code><hr/><div class="description"><p>Returns whether the given spender can transfer a given token ID.</p></div><dl><dt><span class="label-parameters">Parameters:</span></dt><dd><div><code>spender</code> - address of the spender to query</div><div><code>tokenId</code> - uint256 ID of the token to be transferred</div></dd><dt><span class="label-return">Returns:</span></dt><dd>bool whether the msg.sender is approved for the given token ID, is an operator of the owner, or is the owner of the token</dd></dl></div></div></li><li><div class="item function"><span id="_mint" class="anchor-marker"></span><h4 class="name">_mint</h4><div class="body"><code class="signature">function <strong>_mint</strong><span>(address to, uint256 tokenId) </span><span>internal </span></code><hr/><div class="description"><p>Internal function to mint a new token Reverts if the given token ID already exists.</p></div><dl><dt><span class="label-parameters">Parameters:</span></dt><dd><div><code>to</code> - The address that will own the minted token</div><div><code>tokenId</code> - uint256 ID of the token to be minted by the msg.sender</div></dd></dl></div></div></li><li><div class="item function"><span id="_removeTokenFrom" class="anchor-marker"></span><h4 class="name">_removeTokenFrom</h4><div class="body"><code class="signature">function <strong>_removeTokenFrom</strong><span>(address from, uint256 tokenId) </span><span>internal </span></code><hr/><div class="description"><p>Internal function to remove a token ID from the list of a given address.</p></div><dl><dt><span class="label-parameters">Parameters:</span></dt><dd><div><code>from</code> - address representing the previous owner of the given token ID</div><div><code>tokenId</code> - uint256 ID of the token to be removed from the tokens list of the given address</div></dd></dl></div></div></li><li><div class="item function"><span id="approve" class="anchor-marker"></span><h4 class="name">approve</h4><div class="body"><code class="signature">function <strong>approve</strong><span>(address to, uint256 tokenId) </span><span>public </span></code><hr/><div class="description"><p>Approves another address to transfer the given token ID The zero address indicates there is no approved address. There can only be one approved address per token at a given time. Can only be called by the token owner or an approved operator.</p></div><dl><dt><span class="label-parameters">Parameters:</span></dt><dd><div><code>to</code> - address to be approved for the given token ID</div><div><code>tokenId</code> - uint256 ID of the token to be approved</div></dd></dl></div></div></li><li><div class="item function"><span id="balanceOf" class="anchor-marker"></span><h4 class="name">balanceOf</h4><div class="body"><code class="signature">function <strong>balanceOf</strong><span>(address owner) </span><span>public </span><span>view </span><span>returns  (uint256) </span></code><hr/><div class="description"><p>Gets the balance of the specified address.</p></div><dl><dt><span class="label-parameters">Parameters:</span></dt><dd><div><code>owner</code> - address to query the balance of</div></dd><dt><span class="label-return">Returns:</span></dt><dd>uint256 representing the amount owned by the passed address</dd></dl></div></div></li><li><div class="item function"><span id="fallback" class="anchor-marker"></span><h4 class="name">fallback</h4><div class="body"><code class="signature">function <strong></strong><span>() </span><span>public </span></code><hr/></div></div></li><li><div class="item function"><span id="getApproved" class="anchor-marker"></span><h4 class="name">getApproved</h4><div class="body"><code class="signature">function <strong>getApproved</strong><span>(uint256 tokenId) </span><span>public </span><span>view </span><span>returns  (address) </span></code><hr/><div class="description"><p>Gets the approved address for a token ID, or zero if no address set Reverts if the token ID does not exist.</p></div><dl><dt><span class="label-parameters">Parameters:</span></dt><dd><div><code>tokenId</code> - uint256 ID of the token to query the approval of</div></dd><dt><span class="label-return">Returns:</span></dt><dd>address currently approved for the given token ID</dd></dl></div></div></li><li><div class="item function"><span id="isApprovedForAll" class="anchor-marker"></span><h4 class="name">isApprovedForAll</h4><div class="body"><code class="signature">function <strong>isApprovedForAll</strong><span>(address owner, address operator) </span><span>public </span><span>view </span><span>returns  (bool) </span></code><hr/><div class="description"><p>Tells whether an operator is approved by a given owner.</p></div><dl><dt><span class="label-parameters">Parameters:</span></dt><dd><div><code>owner</code> - owner address which you want to query the approval of</div><div><code>operator</code> - operator address which you want to query the approval of</div></dd><dt><span class="label-return">Returns:</span></dt><dd>bool whether the given operator is approved by the given owner</dd></dl></div></div></li><li><div class="item function"><span id="ownerOf" class="anchor-marker"></span><h4 class="name">ownerOf</h4><div class="body"><code class="signature">function <strong>ownerOf</strong><span>(uint256 tokenId) </span><span>public </span><span>view </span><span>returns  (address) </span></code><hr/><div class="description"><p>Gets the owner of the specified token ID.</p></div><dl><dt><span class="label-parameters">Parameters:</span></dt><dd><div><code>tokenId</code> - uint256 ID of the token to query the owner of</div></dd><dt><span class="label-return">Returns:</span></dt><dd>owner address currently marked as the owner of the given token ID</dd></dl></div></div></li><li><div class="item function"><span id="safeTransferFrom" class="anchor-marker"></span><h4 class="name">safeTransferFrom</h4><div class="body"><code class="signature">function <strong>safeTransferFrom</strong><span>(address from, address to, uint256 tokenId) </span><span>public </span></code><hr/><div class="description"><p>Safely transfers the ownership of a given token ID to another address If the target address is a contract, it must implement `onERC721Received`, which is called upon a safe transfer, and return the magic value `bytes4(keccak256(&quot;onERC721Received(address,address,uint256,bytes)&quot;))`; otherwise, the transfer is reverted. * Requires the msg sender to be the owner, approved, or operator.</p></div><dl><dt><span class="label-parameters">Parameters:</span></dt><dd><div><code>from</code> - current owner of the token</div><div><code>to</code> - address to receive the ownership of the given token ID</div><div><code>tokenId</code> - uint256 ID of the token to be transferred</div></dd></dl></div></div></li><li><div class="item function"><span id="safeTransferFrom" class="anchor-marker"></span><h4 class="name">safeTransferFrom</h4><div class="body"><code class="signature">function <strong>safeTransferFrom</strong><span>(address from, address to, uint256 tokenId, bytes _data) </span><span>public </span></code><hr/><div class="description"><p>Safely transfers the ownership of a given token ID to another address If the target address is a contract, it must implement `onERC721Received`, which is called upon a safe transfer, and return the magic value `bytes4(keccak256(&quot;onERC721Received(address,address,uint256,bytes)&quot;))`; otherwise, the transfer is reverted. Requires the msg sender to be the owner, approved, or operator.</p></div><dl><dt><span class="label-parameters">Parameters:</span></dt><dd><div><code>from</code> - current owner of the token</div><div><code>to</code> - address to receive the ownership of the given token ID</div><div><code>tokenId</code> - uint256 ID of the token to be transferred</div><div><code>_data</code> - bytes data to send along with a safe transfer check</div></dd></dl></div></div></li><li><div class="item function"><span id="setApprovalForAll" class="anchor-marker"></span><h4 class="name">setApprovalForAll</h4><div class="body"><code class="signature">function <strong>setApprovalForAll</strong><span>(address to, bool approved) </span><span>public </span></code><hr/><div class="description"><p>Sets or unsets the approval of a given operator An operator is allowed to transfer all tokens of the sender on their behalf.</p></div><dl><dt><span class="label-parameters">Parameters:</span></dt><dd><div><code>to</code> - operator address to set the approval</div><div><code>approved</code> - representing the status of the approval to be set</div></dd></dl></div></div></li><li><div class="item function"><span id="transferFrom" class="anchor-marker"></span><h4 class="name">transferFrom</h4><div class="body"><code class="signature">function <strong>transferFrom</strong><span>(address from, address to, uint256 tokenId) </span><span>public </span></code><hr/><div class="description"><p>Transfers the ownership of a given token ID to another address Usage of this method is discouraged, use `safeTransferFrom` whenever possible Requires the msg sender to be the owner, approved, or operator.</p></div><dl><dt><span class="label-parameters">Parameters:</span></dt><dd><div><code>from</code> - current owner of the token</div><div><code>to</code> - address to receive the ownership of the given token ID</div><div><code>tokenId</code> - uint256 ID of the token to be transferred</div></dd></dl></div></div></li></ul></div></div></div>