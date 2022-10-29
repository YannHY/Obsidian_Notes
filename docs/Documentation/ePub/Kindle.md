## Send books to Kindle
You can send some books or any web page to your device without having to plug it onto your computer.

All you have to do is to follow those few steps.

1. First, you have to download a book. For instance, you can legally and freely download a `.mobi` file on [Project Gutenberg](https://www.gutenberg.org/) website.
2. Then you have to send it to your kindle. In order to do that, you have to know the **Send-to-Kindle e-mail address**. To find out what it is, go to the [Manage Your Devices](https://www.amazon.com/myk#manageDevices) page on Amazon. You will find your device and by clicking on the three dots on the left, you will find the address.
3. You have one more step: add a trusted e-mail account (visit the [Personal Document Settings](https://www.amazon.com/myk#pdocsSettings) page at [Manage Your Kindle](https://www.amazon.com/myk)).
4. To send a document to your Kindle device, simply attach it to an e-mail addressed to your Send-to-Kindle e-mail.

In practice, this is very simple. Say my Send-to-Kindle address is `myadresse@kindle.com`. All I have to do is send my book (or whatever I want: a PDF, a Microsoft document, a picture...) to my Kindle using this address and to send it from a trusted email account (say `myemailaddress@gmail.com`.

## Autres façons d'envoyer un livre sur la Kindle
- Utiliser l’adresse Kindle pour envoyer une page web sur la Kindle : [Push to Kindle v2 (Beta) bookmarklet](https://www.fivefilters.org/push-to-kindle/push-to-kindle-bookmarklet/)

### Bookmarklet:
`javascript:!function()%7Bvar%20e=function(e,t,n)%7Be.setAttribute(t,n)%7D,t=document,n=t.createElement('div'),o=n.style;e(n,'id','ffptkloader'),o.position='fixed',o.top=0,o.right=0,o.width='100%25',o.backgroundColor='%23000',o.color='%23EEE',o.textAlign='center',o.fontFamily='sans-serif',o.padding='2em',o.zIndex='6999999',n.textContent='Loading%20Push%20to%20Kindle...',t.body.appendChild(n);!function(n)%7Bvar%20o=t.createElement('form');e(o,'method','post'),e(o,'action',n),e(o,'accept-charset','UTF-8');var%20d=t.createElement('input');e(d,'type','hidden'),e(d,'name','inputhtml');try%7Bvar%20a,i=t.cloneNode(!0);(a=i.getElementById('ffptkloader'))&&a.parentNode.removeChild(a),%5B'script','style','canvas','select','textarea'%5D.forEach(function(e)%7Bfor(var%20t=i.getElementsByTagName(e),n=t.length-1;n%3E=0;n--)t%5Bn%5D.parentNode.removeChild(t%5Bn%5D)%7D),e(d,'value',i.documentElement.outerHTML),o.appendChild(d),t.body.appendChild(o),o.submit()%7Dcatch(e)%7B%7D%7D('https://pushtokindle.fivefilters.org/send2-html.php?url='+encodeURI(window.location.href))%7D();`

- [Comment envoyer un epub vers un Kindle sans utiliser Calibre ni de cable USB ?](https://korben.info/comment-envoyer-un-epub-vers-un-kindle-sans-utiliser-calibre-ni-de-cable-usb.html) -> [Send EPUB to Kindle](https://www.sendepubtokindle.com/) (The easiest way to send EPUBs to your Kindle!)
- [https://korben.info/comment-livre-epub-contenu-web.html](https://korben.info/comment-livre-epub-contenu-web.html) (extension [Firefox](https://addons.mozilla.org/en-US/firefox/addon/saveasebook/?source=korben.info) et [Chrome](https://chrome.google.com/webstore/detail/save-as-ebook/haaplkpoiimngbppjihnegfmpejdnffj?source=korben.info) = Save As Ebook)

![[send-epub-to-kindle.png | 600]]

- [PDF to Mobi converter](https://cloud convert.com/pdf-to-mobi) (CloudConvert)
> CloudConvert is an online document converter. Amongst many others, we support PDF, DOCX, PPTX, XLSX

-  [Convert text or ebooks to the MOBI format](https://ebook.online-convert.come/convert-to-mobi)


## À lire
- [ ]  [Get your Kindle highlights out of the cloud and onto your computer.](https://readwise.io/bookcision)
- [ ] [Kindle Highlights Formatter](https://kindle-formatter.vercel.app/)
- 