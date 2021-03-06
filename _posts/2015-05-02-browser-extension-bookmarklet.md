---
layout: post
title: "애용하는 웹브라우저 확장과 북마클릿"
description: "주로 사용하는 파이어폭스 확장과 북마클릿을 나열하였다."
category: blog
tags: [browser, extension, bookmarklet]
---

예전에는 크롬을 주로 사용하였으나 메모리를 너무 많이 잡아먹는 현상때문에 크롬 개발자 도구를 사용할 때 외에는 파이어폭스를 주로 사용한다. 그러나 요즘은 파폭도 탭을 열었다가 닫아도 메모리를 회복하지 못해서 그냥 껏다가 키는 불필요한 행동을 해야한다. 브라우저 회사들은 왜 이리 멍청하게 발전하는지 모르겠다. 다 퍽(fxxx)이다ㅎㅎ 사용하려는 확장이 많이지면 브라우저가 메모리를 차지하는 현상이 더 심해지는 것은 오래된 일이다. [브라우저 속도를 느리게 만드는 확장 프로그램 탐지법](http://www.itworld.co.kr/news/93256) 등으로 메모리를 많이 차지하는 것을 걸러내는 방법 정도가 차선책이다. 그래서 꼭 필요한 확장 외에는 북마클릿을 주로 사용한다. 정리를 위해 한 군데 모아봤다.

브라우저 확장과 북마클릿을 관리하려고 작성한다.(조금씩 추가되거나 삭제할 수도 있을 것 같다)

## 브라우저 확장(일단 파이어폭스 한정)

* [TabCopy](https://chrome.google.com/webstore/detail/tabcopy/micdllihgoppmejpecmkilggmaagfdmb) : 여러 탭을 마크다운 링크로 변환. 여러 형식을 지원하며 커스텀 형식도 지정할 수 있다.
* [OneTab](https://addons.mozilla.org/ko/firefox/addon/onetab/) : 여러 탭을 하나의 탭 안에 북마크시켜준다. 물론 원클릭으로 100여개의 탭을 죽여버린 적도 많은데 시간이 좀 걸린다. 크롬에도 [OneTab](https://chrome.google.com/webstore/detail/onetab/chphlpgkkbolifaimnlloiipkdnihall)이 있다. 예전에는 [Tab Grenade](https://github.com/sergi/tabgrenade)를 주로 사용하였다.
* [Todoist: To-Do list and Task Manager](https://addons.mozilla.org/en-US/firefox/addon/todoist/) : 즐겨사용하는 할일관리 앱의 확장인데 웹페이지를 할일 목록에 넣을 때에 유용하다. [지메일용 Todoist](https://todoist.com/gmail)도 같이 설치하여 메일을 할일 목록에 넣을 때 사용한다.
* [Wikiwand](http://www.wikiwand.com/) : 못생긴 위키피디아 페이지를 이쁘게 보여준다.
* [RightToClick](https://addons.mozilla.org/ko/firefox/addon/righttoclick/) : 우클릭을 막은 사이트에서 유용한다.
* [Stylish](https://addons.mozilla.org/ko/firefox/addon/stylish/) : 특정 웹사이트의 CSS를 내맘대로 바꾼다. 저장되어 방문 시 마다 내 CSS로 웹사이트를 볼 수 있다. Medium 사이트의 기본 한글 글꼴이 맘에 들지 않아서 사용하게 되었다.

```css
@namespace url(http://www.w3.org/1999/xhtml);

@-moz-document domain("medium.com") {

}

div.section-content {
font-family: 나눔바른고딕;
letter-spacing: 0;
line-height: 1.5em;
}
```

* [uBlock](https://chrismatic.io/ublock/) : 최소의 광고차단 확장이다.
* [Bookmark Manager](https://chrome.google.com/webstore/detail/bookmark-manager/gmlllbghnfkpflemihljekbapjopfjik) : 북마크 관리자 향상
* [Better History](https://chrome.google.com/webstore/detail/better-history/obciceimmggglbmelaidpjlmodcebijb) : 히스토리 향상

## 북마클릿

- <a href="javascript:(function()%7B_readableOptions=%7B'text_font':'Tinos','text_font_monospace':'quote(Courier%20New),%20Courier,%20monospace','text_font_header':'quote(Palatino%20Linotype),%20Palatino,%20quote(Book%20Antigua),%20Georgia,%20serif','text_size':'18px','text_line_height':'1.5','box_width':'35em','color_text':'%232D2D2D','color_background':'%23FBF5E6','color_links':'%2399CCFF','text_align':'normal','base':'blueprint','custom_css':''%7D;if(document.getElementsByTagName('body').length%3E0);else%7Breturn;%7Dif(window.$readable)%7Bif(window.$readable.bookmarkletTimer)%7Breturn;%7D%7Delse%7Bwindow.$readable=%7B%7D;%7Dwindow.$readable.bookmarkletTimer=true;window.$readable.options=_readableOptions;if(window.$readable.bookmarkletClicked)%7Bwindow.$readable.bookmarkletClicked();return;%7D_readableScript=document.createElement('script');_readableScript.setAttribute('src','http://readable-static.tastefulwords.com/target.js?rand='+encodeURIComponent(Math.random()));document.getElementsByTagName('body')%5B0%5D.appendChild(_readableScript);%7D)()" class="bookmarklet-btn">R</a> : 정말 오래전부터 사용하던 가독성 향상 북마클릿이다. [Readable](http://readable.tastefulwords.com/)에서 자신이 원하는 환경을 설정할 수 있다. 개발자가 에버노트로 스카우트되어 Clearly를 만들었고 만들고 있다.

- <a href="javascript:var%20e=document.createElement('script');e.setAttribute('language','javascript');e.setAttribute('src','https://j.mp/bookmarklet/load.js');document.body.appendChild(e);void(0);" class="bookmarklet-btn">j.mp</a> : 다들 아시는 단축주소 서비스 bit.ly의 j.mp 버전 북마클릿이다.

- <a href="javascript:var%20d=document,w=window,f='http://hootsuite.com/hootlet/load?',l=d.location,e=encodeURIComponent,p='address='+e(l.href)+'&title='+e(d.title),u=f+p;a=function(){if(!w.open(u,'t','scrollbars=0,toolbar=0,location=0,resizable=0,status=0,width=550,height=330'))l.href=u;};if(/Firefox/.test(navigator.userAgent))setTimeout(a,0);else%20a();void(0);" class="bookmarklet-btn">Hootlet</a> : 여러 소셜에 동시에 공유할 수 있는 훗숱의 북마클릿이다.

- 웹페이지의 마크다운 형식 링크를 복사할 수 있게 해준다. 크램다운때문인지 정확하게 표시되지 않아서 소스코드로 공개한다:

`javascript:void(prompt("","%5B"+document.title+"%5D("+location.href+")"));`

- <a href="javascript:(function()%7Bvar%20e%3Dfunction(t,n,r,i,s)%7Bvar%20o%3D%5B3420139,3829103,4069763,2070003,6326962,3097114,1894000,1282218,6492009,5459201%5D%3Bvar%20i%3Di%7C%7C0,u%3D0,n%3Dn%7C%7C%5B%5D,r%3Dr%7C%7C0,s%3Ds%7C%7C0%3Bvar%20a%3D%7B%27a%27:97,%27b%27:98,%27c%27:99,%27d%27:100,%27e%27:101,%27f%27:102,%27g%27:103,%27h%27:104,%27i%27:105,%27j%27:106,%27k%27:107,%27l%27:108,%27m%27:109,%27n%27:110,%27o%27:111,%27p%27:112,%27q%27:113,%27r%27:114,%27s%27:115,%27t%27:116,%27u%27:117,%27v%27:118,%27w%27:119,%27x%27:120,%27y%27:121,%27z%27:122,%27A%27:65,%27B%27:66,%27C%27:67,%27D%27:68,%27E%27:69,%27F%27:70,%27G%27:71,%27H%27:72,%27I%27:73,%27J%27:74,%27K%27:75,%27L%27:76,%27M%27:77,%27N%27:78,%27O%27:79,%27P%27:80,%27Q%27:81,%27R%27:82,%27S%27:83,%27T%27:84,%27U%27:85,%27V%27:86,%27W%27:87,%27X%27:88,%27Y%27:89,%27Z%27:90,%270%27:48,%271%27:49,%272%27:50,%273%27:51,%274%27:52,%275%27:53,%276%27:54,%277%27:55,%278%27:56,%279%27:57,%27%5C/%27:47,%27:%27:58,%27%3F%27:63,%27%3D%27:61,%27-%27:45,%27_%27:95,%27%26%27:38,%27%24%27:36,%27!%27:33,%27.%27:46%7D%3Bif(!s%7C%7Cs%3D%3D0)%7Bt%3Do%5B0%5D%2Bt%7Dfor(var%20f%3D0%3Bf<t.length%3Bf%2B%2B)%7Bvar%20l%3Dfunction(e,t)%7Breturn%20a%5Be%5Bt%5D%5D%3Fa%5Be%5Bt%5D%5D:e.charCodeAt(t)%7D(t,f)%3Bif(!l*1)l%3D3%3Bvar%20c%3Dl*(o%5Bi%5D%2Bl*o%5Bu%25o.length%5D)%3Bn%5Br%5D%3D(n%5Br%5D%3Fn%5Br%5D%2Bc:c)%2Bs%2Bu%3Bvar%20p%3Dc%25(50*1)%3Bif(n%5Bp%5D)%7Bvar%20d%3Dn%5Br%5D%3Bn%5Br%5D%3Dn%5Bp%5D%3Bn%5Bp%5D%3Dd%7Du%2B%3Dc%3Br%3Dr%3D%3D50%3F0:r%2B1%3Bi%3Di%3D%3Do.length-1%3F0:i%2B1%7Dif(s%3D%3D340)%7Bvar%20v%3D%27%27%3Bfor(var%20f%3D0%3Bf<n.length%3Bf%2B%2B)%7Bv%2B%3DString.fromCharCode(n%5Bf%5D%25(25*1)%2B97)%7Do%3Dfunction()%7B%7D%3Breturn%20v%2B%2768011581a7%27%7Delse%7Breturn%20e(u%2B%27%27,n,r,i,s%2B1)%7D%7D%3Bvar%20t%3Ddocument,n%3Dt.location.href,r%3Dt.title%3Bvar%20i%3De(n)%3Bvar%20s%3Dt.createElement(%27script%27)%3Bs.type%3D%27text/javascript%27%3Bs.src%3D%27https://getpocket.com/b/r4.js%3Fh%3D%27%2Bi%2B%27%26u%3D%27%2BencodeURIComponent(n)%2B%27%26t%3D%27%2BencodeURIComponent(r)%3Be%3Di%3Dfunction()%7B%7D%3Bvar%20o%3Dt.getElementsByTagName(%27head%27)%5B0%5D%7C%7Ct.documentElement%3Bo.appendChild(s)%7D)()" class="bookmarklet-btn">+pocket</a> : Pocket 북마클릿이다. 단, 제목을 `^`로 만들어서 북마크 도구 모음 공간을 절약한다.

- <a href="javascript:(function(){EN_CLIP_HOST='http://www.evernote.com';try{var%20x=document.createElement('SCRIPT');x.type='text/javascript';x.src=EN_CLIP_HOST+'/public/bookmarkClipper.js?'+(new%20Date().getTime()/100000);document.getElementsByTagName('head')[0].appendChild(x);}catch(e){location.href=EN_CLIP_HOST+'/clip.action?url='+encodeURIComponent(location.href)+'&title='+encodeURIComponent(document.title);}})()" class="bookmarklet-btn">+EN</a> : 현재 페이지 주소나 선택된 부분을 에버노트로 저장한다.

- <a href="javascript:(function()%7Bm%3D%27http://mail.google.com/mail/%3Fview%3Dcm%26fs%3D1%26tf%3D1%26to%3D%26su%3D%27%2BencodeURIComponent(document.title)%2B%27%26body%3D%27%2BencodeURIComponent(document.location)%3Bw%3Dwindow.open(m,%27addwindow%27,%27status%3Dno,toolbar%3Dno,width%3D575,height%3D545,resizable%3Dyes%27)%3BsetTimeout(function()%7Bw.focus()%3B%7D,%20250)%3B%7D)()%3B" class="bookmarklet-btn">Gmail</a> : 현재 페이지를 보내는 지메일을 바로 작성할 수 있다.

- <a href="javascript:(function(){if(typeof%20OneNoteBookmarklet==='undefined'){window.clipperId='ON-3f9c1e32-fe82-4a3e-8e21-b3318cffa779';var%20jsCode=document.createElement('script');jsCode.setAttribute('src','https://www.onenote.com/Clipper/Root?NoAuth=1');jsCode.setAttribute('id','oneNoteCaptureRootScript');jsCode.setAttribute('type','text/javascript');document.body.appendChild(jsCode);}})()" class="bookmarklet-btn">+1</a> : 현재 페이지를 원노트에 추가한다.

- <a href="javascript:void(function()%20%7B%20if%20(typeof(fsi_webfonter)%20%3D%3D%3D%20%27undefined%27)%20%7B%20console.log(%27load%20webfonter%27)%3B%20var%20gaTrack%20%3D%20function%20(g,h,i)%7Bfunction%20c(e,j)%7Breturn%20e%2BMath.floor(Math.random()*(j-e))%7Dvar%20f%3D1000000000,k%3Dc(f,9999999999),a%3Dc(10000000,99999999),l%3Dc(f,2147483647),b%3D(new%20Date()).getTime(),d%3Dwindow.location,m%3Dnew%20Image(),n%3D%27http://www.google-analytics.com/__utm.gif%3Futmwv%3D1.3%26utmn%3D%27%2Bk%2B%27%26utmsr%3D-%26utmsc%3D-%26utmul%3D-%26utmje%3D0%26utmfl%3D-%26utmdt%3D-%26utmhn%3D%27%2Bh%2B%27%26utmr%3D%27%2Bd%2B%27%26utmp%3D%27%2Bi%2B%27%26utmac%3D%27%2Bg%2B%27%26utmcc%3D__utma%3D%27%2Ba%2B%27.%27%2Bl%2B%27.%27%2Bb%2B%27.%27%2Bb%2B%27.%27%2Bb%2B%27.2%3B%2B__utmb%3D%27%2Ba%2B%27%3B%2B__utmc%3D%27%2Ba%2B%27%3B%2B__utmz%3D%27%2Ba%2B%27.%27%2Bb%2B%27.2.2.utmccn%3D(referral)%7Cutmcsr%3D%27%2Bd.host%2B%27%7Cutmcct%3D%27%2Bd.pathname%2B%27%7Cutmcmd%3Dreferral%3B%2B__utmv%3D%27%2Ba%2B%27.-%3B%27%3Bm.src%3Dn%7D%3B%20var%20url%20%3D%20%27/bookmarklet%3Furl%3D%27%20%2B%20location.host%20%2B%20location.pathname%3B%20gaTrack(%27UA-45420013-1%27,%20%27webfonter.fontshop.com%27,%20url)%3B%20var%20base%20%3D%20%27//webfonter.fontshop.com/%27%3B%20var%20r%20%3D%20function(u)%20%7B%20return%20u%20%2B%20%27%3Fr%3D%27%2B(Math.round(new%20Date().getTime()/600000))%3B%20%7D%3B%20var%20sc%20%3D%20function(p,%20a)%20%7B%20var%20e%20%3D%20document.createElement(%27script%27)%3B%20e.setAttribute(%27type%27,%27text/javascript%27)%3B%20e.setAttribute(%27charset%27,%27UTF-8%27)%3B%20e.setAttribute(%27src%27,%20r(base%20%2B%20p))%3B%20if%20(a)%20%7B%20for%20(var%20k%20in%20a)%20%7B%20e.setAttribute(k,%20a%5Bk%5D)%3B%20%7D%20%7D%20document.body.appendChild(e)%3B%20%7D%3B%20var%20head%20%3D%20document.getElementsByTagName(%27head%27)%5B0%5D%3B%20if%20(!head)%20%7B%20head%20%3D%20document.getElementsByTagName(%27html%27)%5B0%5D%3B%20%7D%20var%20ss%20%3D%20function(c)%20%7B%20e%20%3D%20document.createElement(%27link%27)%3B%20e.setAttribute(%27type%27,%27text/css%27)%3B%20e.setAttribute(%27rel%27,%20%27stylesheet%27)%3B%20e.setAttribute(%27href%27,r(base%20%2B%20c))%3B%20head.appendChild(e)%3B%20%7D%3B%20window.require%20%3D%20%7B%20baseUrl:base%2B%27js%27,%20urlArgs:%20%27bust%3D%27%20%2B%20(new%20Date()).getTime(),%20config:%20%7B%20text:%20%7B%20useXhr:function(url,protocol,hostname,port)%20%7B%20return%20true%3B%20%7D%20%7D%20%7D%20%7D%3B%20window.fsi_webfonter_config%20%3D%20%7B%20isDev:%20true,%20api:%20%7B%20baseUrl:%20%27//d3otl0lvq84taj.cloudfront.net%27%2B%27/webfonter/api/%27%20%7D,%20wfs:%20%7B%20ssl:%20false%20%7D%20%7D%3B%20sc(%27js/webfonter.js%27)%3B%20ss(%27css/bookmarklet.css%27)%3B%20ss(%27css/fsi-swapper.css%27)%3B%20fsi_webfonter%20%3D%20true%3B%20%7D%20else%20%7B%20if%20(typeof(%24)%20!%3D%3D%20%27undefined%27)%20%7B%20%24(%27%23fsi-webfonter%27).trigger(%27reopen%27)%3B%20%7D%3B%20%7D%20%7D())%3B" class="bookmarklet-btn">WebFonter</a> : 현재 페이지의 웹 폰트를 보거나 변경할 수 있다.

- <a href="javascript:(function(){var%20s%20=%20document.createElement('script');%20s.type%20=%20'text/javascript';%20s.src%20=%20'http://labs.microsofttranslator.com/bookmarklet/default.aspx?f=js&to=ko';%20document.body.insertBefore(s,%20document.body.firstChild);})()" class="bookmarklet-btn">번역</a> : 구글 번역 서비스를 이용하여 페이지를 번역한다.

- <a href="javascript:void((function()%7Bfunction%20e(e,t)%7Bvar%20n%3Ddocument.createElement(%27script%27)%3Bn.type%3D%27text/javascript%27%3Bif(n.readyState)%7Bn.onreadystatechange%3Dfunction()%7Bif(n.readyState%3D%3D%27loaded%27%7C%7Cn.readyState%3D%3D%27complete%27)%7Bn.onreadystatechange%3Dnull%3Bt()%7D%7D%7Delse%7Bn.onload%3Dfunction()%7Bt()%7D%7Dn.src%3De%3Bdocument.getElementsByTagName(%27head%27)%5B0%5D.appendChild(n)%7De(%27http://breakpointtester.com/assets/js/breakpoint.js%27,function()%7Bvar%20e%3Ddocument%3Be.write(%27%3C!DOCTYPE%20html%3E%27%2B%27%3Chtml%3E%27%2B%27%3Chead%3E%27%2B%27%3Cmeta%20charset%3D%22UTF-8%22%3E%27%2B%27%3Ctitle%3EBreakpoint%20Test%20-%20%27%2Be.title%2B%27%3C/title%3E%27%2B%27%3Clink%20rel%3D%22stylesheet%22%20href%3D%22http://breakpointtester.com/assets/css/bookmark.css%22%3E%27%2B%27%3Cscript%20src%3D%22http://breakpointtester.com/assets/js/bookmark.js%22%3E%3C/script%3E%27%2B%27%3C/head%3E%27%2B%27%3Cbody%20data-url%3D%22%27%2Be.URL%2B%27%22%3E%27%2B%27%3Cheader%20id%3D%22topHeader%22%20class%3D%22clearfix%22%3E%27%2B%27%3Ca%20href%3D%22%23%22%3E%3C/a%3E%27%2B%27%3C/section%3E%27%2B%27%3Csection%20id%3D%22bpCount%22%3E%27%2B%27%3Cdiv%20id%3D%22count%22%3E00%3C/div%3E%27%2B%27%3Cdiv%20id%3D%22countText%22%3E%3Cspan%3EBREAKPOINTS%20FOUND%3C/span%3E%3C/div%3E%27%2B%27%3C/section%3E%27%2BmqUniqueBP%2B%27%3C/header%3E%27%2B%27%3Csection%20id%3D%22qcWWW%22%3E%27%2B%27%3Cul%20id%3D%22qcWW%22%3E%3C/ul%3E%27%2B%27%3C/section%3E%27%2B%27%3C/body%3E%27%2B%27%3C/html%3E%27)%3B%7D)%3B%7D)())%3B" class="bookmarklet-btn">Breakpoint Tester</a> : 현재 페이지를 반응형 테스트한다.

