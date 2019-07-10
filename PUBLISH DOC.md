---


---

<h4 id="buenas-noches-los-siguientes-componentes-ya-se-encuentran-publicados-y-no-van-a-tener-en-cuenta.">Buenas Noches, los siguientes componentes ya se encuentran publicados y no van a tener en cuenta.</h4>
<pre class=" language-bash"><code class="prism  language-bash">* exito.category-menu@2.x
* allied-promotions@1.0.0
* exito.file-graphql@1.x
* exito.geolocation@2.x
* exito.icons@2.x
* exito.login@2.x
* exito.menu-graphql@2.x
* exito.minicart@3.x
* exito.regionshandle@1.x
</code></pre>
<h4 id="los-componentes-que-han-sido-publicados-son">Los componentes que han sido publicados son:</h4>
<pre class=" language-bash"><code class="prism  language-bash">Dependency <span class="token function">diff</span> between dev and master
                                     dev             master
exito.breadcrumb                     2.1.0<span class="token punctuation">(</span>linked<span class="token punctuation">)</span>    2.1.0 
exito.components                     2.9.0<span class="token punctuation">(</span>linked<span class="token punctuation">)</span>    2.9.0 
exito.footer                         2.12.0<span class="token punctuation">(</span>linked<span class="token punctuation">)</span>   2.12.0
exito.header                         2.2.0<span class="token punctuation">(</span>linked<span class="token punctuation">)</span>    2.2.0
exito.home-components                0.3.5<span class="token punctuation">(</span>linked<span class="token punctuation">)</span>    0.3.5 
exito.my-account                     0.1.2<span class="token punctuation">(</span>linked<span class="token punctuation">)</span>    0.1.2
exito.order-placed                   1.1.9<span class="token punctuation">(</span>linked<span class="token punctuation">)</span>    1.1.9
exito.product-details                2.10.1<span class="token punctuation">(</span>linked<span class="token punctuation">)</span>   2.10.1
exito.product-summary                2.23.3<span class="token punctuation">(</span>linked<span class="token punctuation">)</span>   2.23.3
exito.profile-form                   3.2.5<span class="token punctuation">(</span>linked<span class="token punctuation">)</span>    3.2.5
exito.search-result                  3.4.0<span class="token punctuation">(</span>linked<span class="token punctuation">)</span>    3.4.0 
exito.shipping-estimate-translator   2.1.3<span class="token punctuation">(</span>linked<span class="token punctuation">)</span>    2.1.3
exito.store                          2.29.0<span class="token punctuation">(</span>linked<span class="token punctuation">)</span>   2.29.0
exito.upload-promotions              0.1.0<span class="token punctuation">(</span>linked<span class="token punctuation">)</span>          
exito.upload-promotions-graphql      0.1.0<span class="token punctuation">(</span>linked<span class="token punctuation">)</span>          
exito.vtex-components                2.6.4<span class="token punctuation">(</span>linked<span class="token punctuation">)</span>    2.6.4 
</code></pre>
<h4 id="los-siguientes-proyectos-son-del-core-y-no-se-publican-account">Los siguientes proyectos son del core y no se publican account</h4>
<pre><code>exito.upload-promotions 0.1.0(linked)
exito.upload-promotions-graphql 0.1.0(linked)
</code></pre>
<h4 id="los-siguientes-proyectos-fallaron-al-ser-publicados.">Los siguientes proyectos fallaron al ser publicados.</h4>
<p><code>exito.profile-form 3.2.5</code></p>
<p><em>codebuild error:</em> <a href="https://console.aws.amazon.com/codesuite/codebuild/projects/exito-vtex-deploy-master/build/exito-vtex-deploy-master%3A4b24d456-e5b3-4cf5-9050-afac7f4d2e76/log">https://console.aws.amazon.com/codesuite/codebuild/projects/exito-vtex-deploy-master/build/exito-vtex-deploy-master%3A4b24d456-e5b3-4cf5-9050-afac7f4d2e76/log</a>.</p>
<blockquote>
<p>Al parecer no esta pudiendo instalar node_modules de la forma nomral, viendo el proyecto fue necesario correr el comando localmente para publicar y de la siguiente manera <code>npm run symlinks &amp;&amp; vtex publish</code>, esto genera el archivo package.json dentro de react y instala node_mdoules. hay que ver como arreglar esto para integración continua</p>
</blockquote>
<h2 id="se-identificaron-los-siguientes-fallos-al-publicar-en-exitocol">Se identificaron los siguientes fallos al publicar en exitocol</h2>
<ul>
<li>
<p>El menu en exitocol no esta obteniendo el resultado. hay que revisar esta parte.</p>
</li>
<li>
<p>Al instalar en exitocol el store. se esta ejecutando constantemente una petición. ver que sucede, se instalo la ultima versión en el workspace dev de exitocol.<br>
<a href="https://dev--exitocol.myvtex.com/">dev exitocol</a></p>
</li>
</ul>
<p>Log capturado</p>
<pre class=" language-json"><code class="prism  language-json"><span class="token punctuation">{</span>

<span class="token string">"data"</span><span class="token punctuation">:</span> <span class="token punctuation">{</span>

<span class="token string">"setOrderFormCustomData"</span><span class="token punctuation">:</span> <span class="token keyword">null</span>

<span class="token punctuation">}</span><span class="token punctuation">,</span>

<span class="token string">"errors"</span><span class="token punctuation">:</span> <span class="token punctuation">[</span><span class="token punctuation">{</span>

<span class="token string">"message"</span><span class="token punctuation">:</span> <span class="token string">"Request failed with status code 404"</span><span class="token punctuation">,</span>

<span class="token string">"path"</span><span class="token punctuation">:</span> <span class="token punctuation">[</span><span class="token string">"setOrderFormCustomData"</span><span class="token punctuation">]</span><span class="token punctuation">,</span>

<span class="token string">"extensions"</span><span class="token punctuation">:</span> <span class="token punctuation">{</span>

<span class="token string">"code"</span><span class="token punctuation">:</span> <span class="token string">"INTERNAL_SERVER_ERROR"</span><span class="token punctuation">,</span>

<span class="token string">"exception"</span><span class="token punctuation">:</span> <span class="token punctuation">{</span>

<span class="token string">"config"</span><span class="token punctuation">:</span> <span class="token punctuation">{</span>

<span class="token string">"baseURL"</span><span class="token punctuation">:</span> <span class="token string">"http://portal.vtexcommercestable.com.br"</span><span class="token punctuation">,</span>

<span class="token string">"data"</span><span class="token punctuation">:</span> <span class="token string">"{\"value\":\"11\"}"</span><span class="token punctuation">,</span>

<span class="token string">"headers"</span><span class="token punctuation">:</span> <span class="token punctuation">{</span>

<span class="token string">"Accept"</span><span class="token punctuation">:</span> <span class="token string">"application/json, text/plain, */*"</span><span class="token punctuation">,</span>

<span class="token string">"Content-Type"</span><span class="token punctuation">:</span> <span class="token string">"application/json;charset=utf-8"</span><span class="token punctuation">,</span>

<span class="token string">"accept-encoding"</span><span class="token punctuation">:</span> <span class="token string">"gzip"</span><span class="token punctuation">,</span>

<span class="token string">"user-agent"</span><span class="token punctuation">:</span> <span class="token string">"vtex.store-graphql@2.92.0"</span><span class="token punctuation">,</span>

<span class="token string">"x-vtex-operation-id"</span><span class="token punctuation">:</span> <span class="token string">"d88f8898-64c7-4c74-b5bc-aff23fe70290"</span><span class="token punctuation">,</span>

<span class="token string">"x-vtex-segment"</span><span class="token punctuation">:</span> <span class="token string">"eyJjYW1wYWlnbnMiOm51bGwsImNoYW5uZWwiOiIxIiwicHJpY2VUYWJsZXMiOm51bGwsInJlZ2lvbklkIjpudWxsLCJ1dG1fY2FtcGFpZ24iOm51bGwsInV0bV9zb3VyY2UiOm51bGwsInV0bWlfY2FtcGFpZ24iOm51bGwsImN1cnJlbmN5Q29kZSI6IkNPUCIsImN1cnJlbmN5U3ltYm9sIjoiJCIsImNvdW50cnlDb2RlIjoiQ09MIiwiY3VsdHVyZUluZm8iOiJlcy1DTyJ9"</span><span class="token punctuation">,</span>

<span class="token string">"x-vtex-session"</span><span class="token punctuation">:</span> <span class="token string">"eyJhbGciOiJFUzI1NiIsImtpZCI6IjlFRERGMjVBOEMwNjc5RTZCQ0U3OEEwNjY1N0ZBMDAxOTkyQTc2NDEiLCJ0eXAiOiJqd3QifQ.eyJhY2NvdW50LmlkIjoiZjQ1MzFhM2ItNzc2ZS00MDdjLWIyMTMtNjhkNmRlOWU0MDVhIiwiaWQiOiIxMWExZTE1Yy04NWQzLTQ0ZTQtYmNhOC0zYWY2YjA3NjM1YzQiLCJ2ZXJzaW9uIjoyLCJzdWIiOiJzZXNzaW9uIiwiYWNjb3VudCI6InNlc3Npb24iLCJleHAiOjE1NjM0Mjc2MTIsImlhdCI6MTU2MjczNjQxMiwiaXNzIjoidG9rZW4tZW1pdHRlciIsImp0aSI6IjlkYzdhY2U2LWZhMzYtNDJjYi1hMDE3LTgyZjQyMzFjM2JiNiJ9.aNsl_wGAn054f9jfY8PztBRumLW84y7osFiDtBQK_jrycq0tdrD1hDgrF64QfCjNYmKjXKb3pOysjKLXzi3Hhg"</span><span class="token punctuation">,</span>

<span class="token string">"cookie"</span><span class="token punctuation">:</span> <span class="token string">"checkout.vtex.com=__ofid=bb371688449845de8cb00d0961f71e01;vtex_segment=eyJjYW1wYWlnbnMiOm51bGwsImNoYW5uZWwiOiIxIiwicHJpY2VUYWJsZXMiOm51bGwsInJlZ2lvbklkIjpudWxsLCJ1dG1fY2FtcGFpZ24iOm51bGwsInV0bV9zb3VyY2UiOm51bGwsInV0bWlfY2FtcGFpZ24iOm51bGwsImN1cnJlbmN5Q29kZSI6IkNPUCIsImN1cnJlbmN5U3ltYm9sIjoiJCIsImNvdW50cnlDb2RlIjoiQ09MIiwiY3VsdHVyZUluZm8iOiJlcy1DTyJ9;vtex_session=eyJhbGciOiJFUzI1NiIsImtpZCI6IjlFRERGMjVBOEMwNjc5RTZCQ0U3OEEwNjY1N0ZBMDAxOTkyQTc2NDEiLCJ0eXAiOiJqd3QifQ.eyJhY2NvdW50LmlkIjoiZjQ1MzFhM2ItNzc2ZS00MDdjLWIyMTMtNjhkNmRlOWU0MDVhIiwiaWQiOiIxMWExZTE1Yy04NWQzLTQ0ZTQtYmNhOC0zYWY2YjA3NjM1YzQiLCJ2ZXJzaW9uIjoyLCJzdWIiOiJzZXNzaW9uIiwiYWNjb3VudCI6InNlc3Npb24iLCJleHAiOjE1NjM0Mjc2MTIsImlhdCI6MTU2MjczNjQxMiwiaXNzIjoidG9rZW4tZW1pdHRlciIsImp0aSI6IjlkYzdhY2U2LWZhMzYtNDJjYi1hMDE3LTgyZjQyMzFjM2JiNiJ9.aNsl_wGAn054f9jfY8PztBRumLW84y7osFiDtBQK_jrycq0tdrD1hDgrF64QfCjNYmKjXKb3pOysjKLXzi3Hhg;"</span><span class="token punctuation">,</span>

<span class="token string">"Content-Length"</span><span class="token punctuation">:</span> <span class="token number">14</span>

<span class="token punctuation">}</span><span class="token punctuation">,</span>

<span class="token string">"method"</span><span class="token punctuation">:</span> <span class="token string">"put"</span><span class="token punctuation">,</span>

<span class="token string">"timeout"</span><span class="token punctuation">:</span> <span class="token number">10000</span><span class="token punctuation">,</span>

<span class="token string">"url"</span><span class="token punctuation">:</span> <span class="token string">"http://portal.vtexcommercestable.com.br/api/checkout/pub/orderForm/bb371688449845de8cb00d0961f71e01/customData/order/channelId"</span><span class="token punctuation">,</span>

<span class="token string">"metric"</span><span class="token punctuation">:</span> <span class="token string">"checkout-setOrderFormCustomData"</span><span class="token punctuation">,</span>

<span class="token string">"params"</span><span class="token punctuation">:</span> <span class="token punctuation">{</span>

<span class="token string">"an"</span><span class="token punctuation">:</span> <span class="token string">"exitocol"</span>

<span class="token punctuation">}</span>

<span class="token punctuation">}</span><span class="token punctuation">,</span>

<span class="token string">"request"</span><span class="token punctuation">:</span> <span class="token punctuation">{</span>

<span class="token string">"finished"</span><span class="token punctuation">:</span> <span class="token boolean">true</span><span class="token punctuation">,</span>

<span class="token string">"method"</span><span class="token punctuation">:</span> <span class="token string">"PUT"</span><span class="token punctuation">,</span>

<span class="token string">"path"</span><span class="token punctuation">:</span> <span class="token string">"/api/checkout/pub/orderForm/bb371688449845de8cb00d0961f71e01/customData/order/channelId?an=exitocol"</span>

<span class="token punctuation">}</span><span class="token punctuation">,</span>

<span class="token string">"response"</span><span class="token punctuation">:</span> <span class="token punctuation">{</span>

<span class="token string">"data"</span><span class="token punctuation">:</span> <span class="token punctuation">{</span>

<span class="token string">"Fields"</span><span class="token punctuation">:</span> <span class="token punctuation">{</span><span class="token punctuation">}</span><span class="token punctuation">,</span>

<span class="token string">"operationId"</span><span class="token punctuation">:</span> <span class="token string">"d88f8898-64c7-4c74-b5bc-aff23fe70290"</span><span class="token punctuation">,</span>

<span class="token string">"error"</span><span class="token punctuation">:</span> <span class="token punctuation">{</span>

<span class="token string">"code"</span><span class="token punctuation">:</span> <span class="token string">"1"</span><span class="token punctuation">,</span>

<span class="token string">"message"</span><span class="token punctuation">:</span> <span class="token string">"Id de la aplicación no encontrado"</span><span class="token punctuation">,</span>

<span class="token string">"exception"</span><span class="token punctuation">:</span> <span class="token keyword">null</span>

<span class="token punctuation">}</span>

<span class="token punctuation">}</span><span class="token punctuation">,</span>

<span class="token string">"headers"</span><span class="token punctuation">:</span> <span class="token punctuation">{</span>

<span class="token string">"date"</span><span class="token punctuation">:</span> <span class="token string">"Wed, 10 Jul 2019 05:44:11 GMT"</span><span class="token punctuation">,</span>

<span class="token string">"content-type"</span><span class="token punctuation">:</span> <span class="token string">"application/json; charset=utf-8"</span><span class="token punctuation">,</span>

<span class="token string">"server"</span><span class="token punctuation">:</span> <span class="token string">"VTEX IO"</span><span class="token punctuation">,</span>

<span class="token string">"content-length"</span><span class="token punctuation">:</span> <span class="token string">"151"</span><span class="token punctuation">,</span>

<span class="token string">"cache-control"</span><span class="token punctuation">:</span> <span class="token string">"no-cache"</span><span class="token punctuation">,</span>

<span class="token string">"pragma"</span><span class="token punctuation">:</span> <span class="token string">"no-cache"</span><span class="token punctuation">,</span>

<span class="token string">"expires"</span><span class="token punctuation">:</span> <span class="token string">"-1"</span><span class="token punctuation">,</span>

<span class="token string">"set-cookie"</span><span class="token punctuation">:</span> <span class="token punctuation">[</span><span class="token string">"janus_sid=44d56838-91f5-4d87-bb9f-9a14b3ba2065; expires=Sat, 13 Jul 2019 05:44:04 GMT; domain=portal.vtexcommercestable.com.br; path=/; samesite=lax"</span><span class="token punctuation">]</span><span class="token punctuation">,</span>

<span class="token string">"x-aspnet-version"</span><span class="token punctuation">:</span> <span class="token string">"4.0.30319"</span><span class="token punctuation">,</span>

<span class="token string">"x-powered-by"</span><span class="token punctuation">:</span> <span class="token string">"ASP.NET"</span><span class="token punctuation">,</span>

<span class="token string">"x-vtex-error-code"</span><span class="token punctuation">:</span> <span class="token string">"1"</span><span class="token punctuation">,</span>

<span class="token string">"x-vtex-error-message"</span><span class="token punctuation">:</span> <span class="token string">"Id%20de%20la%20aplicaci%C3%B3n%20no%20encontrado"</span><span class="token punctuation">,</span>

<span class="token string">"x-vtex-janus-router-backend-app"</span><span class="token punctuation">:</span> <span class="token string">"chk-v2.99.4"</span><span class="token punctuation">,</span>

<span class="token string">"x-vtex-operation-id"</span><span class="token punctuation">:</span> <span class="token string">"d88f8898-64c7-4c74-b5bc-aff23fe70290"</span><span class="token punctuation">,</span>

<span class="token string">"x-request-id"</span><span class="token punctuation">:</span> <span class="token string">"1d1f7c64b81a4c93b628cf4c7e821644"</span><span class="token punctuation">,</span>

<span class="token string">"x-vtex-router-version"</span><span class="token punctuation">:</span> <span class="token string">"2.17.3"</span><span class="token punctuation">,</span>

<span class="token string">"x-vtex-backend-status-code"</span><span class="token punctuation">:</span> <span class="token string">"NotFound"</span><span class="token punctuation">,</span>

<span class="token string">"x-vtex-backend-elapsed-time"</span><span class="token punctuation">:</span> <span class="token string">"00:00:00.0570141"</span><span class="token punctuation">,</span>

<span class="token string">"x-vtex-router-elapsed-time"</span><span class="token punctuation">:</span> <span class="token string">"00:00:00.0690867"</span><span class="token punctuation">,</span>

<span class="token string">"x-vtex-io-cluster-id"</span><span class="token punctuation">:</span> <span class="token string">"aws-2-us-east-1"</span>

<span class="token punctuation">}</span><span class="token punctuation">,</span>

<span class="token string">"status"</span><span class="token punctuation">:</span> <span class="token number">404</span>

<span class="token punctuation">}</span><span class="token punctuation">,</span>

<span class="token string">"code"</span><span class="token punctuation">:</span> <span class="token string">"E_HTTP_404"</span><span class="token punctuation">,</span>

<span class="token string">"name"</span><span class="token punctuation">:</span> <span class="token string">"Error"</span><span class="token punctuation">,</span>

<span class="token string">"message"</span><span class="token punctuation">:</span> <span class="token string">"Request failed with status code 404"</span><span class="token punctuation">,</span>

<span class="token string">"stack"</span><span class="token punctuation">:</span> <span class="token string">"Error: Request failed with status code 404\n at createError (/usr/local/app/node_modules/axios/lib/core/createError.js:16:15)\n at settle (/usr/local/app/node_modules/axios/lib/core/settle.js:18:12)\n at IncomingMessage.handleStreamEnd (/usr/local/app/node_modules/axios/lib/adapters/http.js:202:11)\n at IncomingMessage.emit (events.js:208:15)\n at endReadableNT (_stream_readable.js:1154:12)\n at processTicksAndRejections (internal/process/task_queues.js:77:11)"</span>

<span class="token punctuation">}</span>

<span class="token punctuation">}</span><span class="token punctuation">,</span>

<span class="token string">"name"</span><span class="token punctuation">:</span> <span class="token string">"GraphQLError"</span><span class="token punctuation">,</span>

<span class="token string">"originalError"</span><span class="token punctuation">:</span> <span class="token punctuation">{</span>

<span class="token string">"config"</span><span class="token punctuation">:</span> <span class="token punctuation">{</span>

<span class="token string">"baseURL"</span><span class="token punctuation">:</span> <span class="token string">"http://portal.vtexcommercestable.com.br"</span><span class="token punctuation">,</span>

<span class="token string">"data"</span><span class="token punctuation">:</span> <span class="token string">"{\"value\":\"11\"}"</span><span class="token punctuation">,</span>

<span class="token string">"headers"</span><span class="token punctuation">:</span> <span class="token punctuation">{</span>

<span class="token string">"Accept"</span><span class="token punctuation">:</span> <span class="token string">"application/json, text/plain, */*"</span><span class="token punctuation">,</span>

<span class="token string">"Content-Type"</span><span class="token punctuation">:</span> <span class="token string">"application/json;charset=utf-8"</span><span class="token punctuation">,</span>

<span class="token string">"accept-encoding"</span><span class="token punctuation">:</span> <span class="token string">"gzip"</span><span class="token punctuation">,</span>

<span class="token string">"user-agent"</span><span class="token punctuation">:</span> <span class="token string">"vtex.store-graphql@2.92.0"</span><span class="token punctuation">,</span>

<span class="token string">"x-vtex-operation-id"</span><span class="token punctuation">:</span> <span class="token string">"d88f8898-64c7-4c74-b5bc-aff23fe70290"</span><span class="token punctuation">,</span>

<span class="token string">"x-vtex-segment"</span><span class="token punctuation">:</span> <span class="token string">"eyJjYW1wYWlnbnMiOm51bGwsImNoYW5uZWwiOiIxIiwicHJpY2VUYWJsZXMiOm51bGwsInJlZ2lvbklkIjpudWxsLCJ1dG1fY2FtcGFpZ24iOm51bGwsInV0bV9zb3VyY2UiOm51bGwsInV0bWlfY2FtcGFpZ24iOm51bGwsImN1cnJlbmN5Q29kZSI6IkNPUCIsImN1cnJlbmN5U3ltYm9sIjoiJCIsImNvdW50cnlDb2RlIjoiQ09MIiwiY3VsdHVyZUluZm8iOiJlcy1DTyJ9"</span><span class="token punctuation">,</span>

<span class="token string">"x-vtex-session"</span><span class="token punctuation">:</span> <span class="token string">"eyJhbGciOiJFUzI1NiIsImtpZCI6IjlFRERGMjVBOEMwNjc5RTZCQ0U3OEEwNjY1N0ZBMDAxOTkyQTc2NDEiLCJ0eXAiOiJqd3QifQ.eyJhY2NvdW50LmlkIjoiZjQ1MzFhM2ItNzc2ZS00MDdjLWIyMTMtNjhkNmRlOWU0MDVhIiwiaWQiOiIxMWExZTE1Yy04NWQzLTQ0ZTQtYmNhOC0zYWY2YjA3NjM1YzQiLCJ2ZXJzaW9uIjoyLCJzdWIiOiJzZXNzaW9uIiwiYWNjb3VudCI6InNlc3Npb24iLCJleHAiOjE1NjM0Mjc2MTIsImlhdCI6MTU2MjczNjQxMiwiaXNzIjoidG9rZW4tZW1pdHRlciIsImp0aSI6IjlkYzdhY2U2LWZhMzYtNDJjYi1hMDE3LTgyZjQyMzFjM2JiNiJ9.aNsl_wGAn054f9jfY8PztBRumLW84y7osFiDtBQK_jrycq0tdrD1hDgrF64QfCjNYmKjXKb3pOysjKLXzi3Hhg"</span><span class="token punctuation">,</span>

<span class="token string">"cookie"</span><span class="token punctuation">:</span> <span class="token string">"checkout.vtex.com=__ofid=bb371688449845de8cb00d0961f71e01;vtex_segment=eyJjYW1wYWlnbnMiOm51bGwsImNoYW5uZWwiOiIxIiwicHJpY2VUYWJsZXMiOm51bGwsInJlZ2lvbklkIjpudWxsLCJ1dG1fY2FtcGFpZ24iOm51bGwsInV0bV9zb3VyY2UiOm51bGwsInV0bWlfY2FtcGFpZ24iOm51bGwsImN1cnJlbmN5Q29kZSI6IkNPUCIsImN1cnJlbmN5U3ltYm9sIjoiJCIsImNvdW50cnlDb2RlIjoiQ09MIiwiY3VsdHVyZUluZm8iOiJlcy1DTyJ9;vtex_session=eyJhbGciOiJFUzI1NiIsImtpZCI6IjlFRERGMjVBOEMwNjc5RTZCQ0U3OEEwNjY1N0ZBMDAxOTkyQTc2NDEiLCJ0eXAiOiJqd3QifQ.eyJhY2NvdW50LmlkIjoiZjQ1MzFhM2ItNzc2ZS00MDdjLWIyMTMtNjhkNmRlOWU0MDVhIiwiaWQiOiIxMWExZTE1Yy04NWQzLTQ0ZTQtYmNhOC0zYWY2YjA3NjM1YzQiLCJ2ZXJzaW9uIjoyLCJzdWIiOiJzZXNzaW9uIiwiYWNjb3VudCI6InNlc3Npb24iLCJleHAiOjE1NjM0Mjc2MTIsImlhdCI6MTU2MjczNjQxMiwiaXNzIjoidG9rZW4tZW1pdHRlciIsImp0aSI6IjlkYzdhY2U2LWZhMzYtNDJjYi1hMDE3LTgyZjQyMzFjM2JiNiJ9.aNsl_wGAn054f9jfY8PztBRumLW84y7osFiDtBQK_jrycq0tdrD1hDgrF64QfCjNYmKjXKb3pOysjKLXzi3Hhg;"</span><span class="token punctuation">,</span>

<span class="token string">"Content-Length"</span><span class="token punctuation">:</span> <span class="token number">14</span>

<span class="token punctuation">}</span><span class="token punctuation">,</span>

<span class="token string">"method"</span><span class="token punctuation">:</span> <span class="token string">"put"</span><span class="token punctuation">,</span>

<span class="token string">"timeout"</span><span class="token punctuation">:</span> <span class="token number">10000</span><span class="token punctuation">,</span>

<span class="token string">"url"</span><span class="token punctuation">:</span> <span class="token string">"http://portal.vtexcommercestable.com.br/api/checkout/pub/orderForm/bb371688449845de8cb00d0961f71e01/customData/order/channelId"</span><span class="token punctuation">,</span>

<span class="token string">"metric"</span><span class="token punctuation">:</span> <span class="token string">"checkout-setOrderFormCustomData"</span><span class="token punctuation">,</span>

<span class="token string">"params"</span><span class="token punctuation">:</span> <span class="token punctuation">{</span>

<span class="token string">"an"</span><span class="token punctuation">:</span> <span class="token string">"exitocol"</span>

<span class="token punctuation">}</span>

<span class="token punctuation">}</span><span class="token punctuation">,</span>

<span class="token string">"request"</span><span class="token punctuation">:</span> <span class="token punctuation">{</span>

<span class="token string">"finished"</span><span class="token punctuation">:</span> <span class="token boolean">true</span><span class="token punctuation">,</span>

<span class="token string">"method"</span><span class="token punctuation">:</span> <span class="token string">"PUT"</span><span class="token punctuation">,</span>

<span class="token string">"path"</span><span class="token punctuation">:</span> <span class="token string">"/api/checkout/pub/orderForm/bb371688449845de8cb00d0961f71e01/customData/order/channelId?an=exitocol"</span>

<span class="token punctuation">}</span><span class="token punctuation">,</span>

<span class="token string">"response"</span><span class="token punctuation">:</span> <span class="token punctuation">{</span>

<span class="token string">"data"</span><span class="token punctuation">:</span> <span class="token punctuation">{</span>

<span class="token string">"Fields"</span><span class="token punctuation">:</span> <span class="token punctuation">{</span><span class="token punctuation">}</span><span class="token punctuation">,</span>

<span class="token string">"operationId"</span><span class="token punctuation">:</span> <span class="token string">"d88f8898-64c7-4c74-b5bc-aff23fe70290"</span><span class="token punctuation">,</span>

<span class="token string">"error"</span><span class="token punctuation">:</span> <span class="token punctuation">{</span>

<span class="token string">"code"</span><span class="token punctuation">:</span> <span class="token string">"1"</span><span class="token punctuation">,</span>

<span class="token string">"message"</span><span class="token punctuation">:</span> <span class="token string">"Id de la aplicación no encontrado"</span><span class="token punctuation">,</span>

<span class="token string">"exception"</span><span class="token punctuation">:</span> <span class="token keyword">null</span>

<span class="token punctuation">}</span>

<span class="token punctuation">}</span><span class="token punctuation">,</span>

<span class="token string">"headers"</span><span class="token punctuation">:</span> <span class="token punctuation">{</span>

<span class="token string">"date"</span><span class="token punctuation">:</span> <span class="token string">"Wed, 10 Jul 2019 05:44:11 GMT"</span><span class="token punctuation">,</span>

<span class="token string">"content-type"</span><span class="token punctuation">:</span> <span class="token string">"application/json; charset=utf-8"</span><span class="token punctuation">,</span>

<span class="token string">"server"</span><span class="token punctuation">:</span> <span class="token string">"VTEX IO"</span><span class="token punctuation">,</span>

<span class="token string">"content-length"</span><span class="token punctuation">:</span> <span class="token string">"151"</span><span class="token punctuation">,</span>

<span class="token string">"cache-control"</span><span class="token punctuation">:</span> <span class="token string">"no-cache"</span><span class="token punctuation">,</span>

<span class="token string">"pragma"</span><span class="token punctuation">:</span> <span class="token string">"no-cache"</span><span class="token punctuation">,</span>

<span class="token string">"expires"</span><span class="token punctuation">:</span> <span class="token string">"-1"</span><span class="token punctuation">,</span>

<span class="token string">"set-cookie"</span><span class="token punctuation">:</span> <span class="token punctuation">[</span><span class="token string">"janus_sid=44d56838-91f5-4d87-bb9f-9a14b3ba2065; expires=Sat, 13 Jul 2019 05:44:04 GMT; domain=portal.vtexcommercestable.com.br; path=/; samesite=lax"</span><span class="token punctuation">]</span><span class="token punctuation">,</span>

<span class="token string">"x-aspnet-version"</span><span class="token punctuation">:</span> <span class="token string">"4.0.30319"</span><span class="token punctuation">,</span>

<span class="token string">"x-powered-by"</span><span class="token punctuation">:</span> <span class="token string">"ASP.NET"</span><span class="token punctuation">,</span>

<span class="token string">"x-vtex-error-code"</span><span class="token punctuation">:</span> <span class="token string">"1"</span><span class="token punctuation">,</span>

<span class="token string">"x-vtex-error-message"</span><span class="token punctuation">:</span> <span class="token string">"Id%20de%20la%20aplicaci%C3%B3n%20no%20encontrado"</span><span class="token punctuation">,</span>

<span class="token string">"x-vtex-janus-router-backend-app"</span><span class="token punctuation">:</span> <span class="token string">"chk-v2.99.4"</span><span class="token punctuation">,</span>

<span class="token string">"x-vtex-operation-id"</span><span class="token punctuation">:</span> <span class="token string">"d88f8898-64c7-4c74-b5bc-aff23fe70290"</span><span class="token punctuation">,</span>

<span class="token string">"x-request-id"</span><span class="token punctuation">:</span> <span class="token string">"1d1f7c64b81a4c93b628cf4c7e821644"</span><span class="token punctuation">,</span>

<span class="token string">"x-vtex-router-version"</span><span class="token punctuation">:</span> <span class="token string">"2.17.3"</span><span class="token punctuation">,</span>

<span class="token string">"x-vtex-backend-status-code"</span><span class="token punctuation">:</span> <span class="token string">"NotFound"</span><span class="token punctuation">,</span>

<span class="token string">"x-vtex-backend-elapsed-time"</span><span class="token punctuation">:</span> <span class="token string">"00:00:00.0570141"</span><span class="token punctuation">,</span>

<span class="token string">"x-vtex-router-elapsed-time"</span><span class="token punctuation">:</span> <span class="token string">"00:00:00.0690867"</span><span class="token punctuation">,</span>

<span class="token string">"x-vtex-io-cluster-id"</span><span class="token punctuation">:</span> <span class="token string">"aws-2-us-east-1"</span>

<span class="token punctuation">}</span><span class="token punctuation">,</span>

<span class="token string">"status"</span><span class="token punctuation">:</span> <span class="token number">404</span>

<span class="token punctuation">}</span><span class="token punctuation">,</span>

<span class="token string">"name"</span><span class="token punctuation">:</span> <span class="token string">"Error"</span><span class="token punctuation">,</span>

<span class="token string">"message"</span><span class="token punctuation">:</span> <span class="token string">"Request failed with status code 404"</span><span class="token punctuation">,</span>

<span class="token string">"stack"</span><span class="token punctuation">:</span> <span class="token string">"Error: Request failed with status code 404\n at createError (/usr/local/app/node_modules/axios/lib/core/createError.js:16:15)\n at settle (/usr/local/app/node_modules/axios/lib/core/settle.js:18:12)\n at IncomingMessage.handleStreamEnd (/usr/local/app/node_modules/axios/lib/adapters/http.js:202:11)\n at IncomingMessage.emit (events.js:208:15)\n at endReadableNT (_stream_readable.js:1154:12)\n at processTicksAndRejections (internal/process/task_queues.js:77:11)"</span><span class="token punctuation">,</span>

<span class="token string">"code"</span><span class="token punctuation">:</span> <span class="token string">"E_HTTP_404"</span>

<span class="token punctuation">}</span><span class="token punctuation">,</span>

<span class="token string">"forwardedHost"</span><span class="token punctuation">:</span> <span class="token string">"dev--exitocol.myvtex.com"</span><span class="token punctuation">,</span>

<span class="token string">"forwardedProto"</span><span class="token punctuation">:</span> <span class="token string">"http"</span><span class="token punctuation">,</span>

<span class="token string">"operationId"</span><span class="token punctuation">:</span> <span class="token string">"d88f8898-64c7-4c74-b5bc-aff23fe70290"</span><span class="token punctuation">,</span>

<span class="token string">"query"</span><span class="token punctuation">:</span> <span class="token punctuation">{</span>

<span class="token string">"query"</span><span class="token punctuation">:</span> <span class="token string">"mutation ($orderFormId: String, $appId: String, $field: String, $value: String) {\n setOrderFormCustomData(orderFormId: $orderFormId, appId: $appId, field: $field, value: $value) {\n customData {\n customApps {\n fields\n __typename\n }\n __typename\n }\n __typename\n }\n}\n"</span><span class="token punctuation">,</span>

<span class="token string">"variables"</span><span class="token punctuation">:</span> <span class="token punctuation">{</span>

<span class="token string">"orderFormId"</span><span class="token punctuation">:</span> <span class="token string">"bb371688449845de8cb00d0961f71e01"</span><span class="token punctuation">,</span>

<span class="token string">"appId"</span><span class="token punctuation">:</span> <span class="token string">"order"</span><span class="token punctuation">,</span>

<span class="token string">"field"</span><span class="token punctuation">:</span> <span class="token string">"channelId"</span><span class="token punctuation">,</span>

<span class="token string">"value"</span><span class="token punctuation">:</span> <span class="token string">"11"</span>

<span class="token punctuation">}</span><span class="token punctuation">,</span>

<span class="token string">"senderApp"</span><span class="token punctuation">:</span> <span class="token string">"exito.components@2.9.0"</span><span class="token punctuation">,</span>

<span class="token string">"providerApp"</span><span class="token punctuation">:</span> <span class="token string">"vtex.store-graphql@2.92.0"</span>

<span class="token punctuation">}</span><span class="token punctuation">,</span>

<span class="token string">"requestId"</span><span class="token punctuation">:</span> <span class="token string">"6298fe6146734197b7389e0696918e1e"</span><span class="token punctuation">,</span>

<span class="token string">"pathName"</span><span class="token punctuation">:</span> <span class="token string">"setOrderFormCustomData"</span>

<span class="token punctuation">}</span><span class="token punctuation">]</span>

<span class="token punctuation">}</span>
</code></pre>

