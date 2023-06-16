<p align="center"><a href="https://xxai.art"><img src="https://cdn.jsdelivr.net/gh/xxai-art/doc/logo.svg"/></a><br/><a href="https://xxai.art"><img src="https://cdn.jsdelivr.net/gh/xxai-art/doc/xxai.svg"/></a></p><p align="center"><a href="https://github.com/xxai-art/doc#readme"><img alt="I18N" src="https://cdn.jsdelivr.net/gh/wactax/img/t.svg"/></a>　<a href="https://groups.google.com/u/0/g/xxai-art"><img alt="Google Groups" src="https://cdn.jsdelivr.net/gh/wactax/img/g-groups.svg"/></a></p>

ई सलाह दिहल जाला कि पहिले nodejs, [direnv](https://direnv.net) , [bun](https://github.com/oven-sh/bun) इंस्टॉल कइल जाय, आ फिर डाइरेक्टरी में प्रवेश कइला के बाद `direnv allow` ( डाइरेक्टरी में प्रवेश कइला के बाद [.envrc](https://github.com/xxai-art/doc/blob/main/.envrc) स्वचालित रूप से निष्पादित हो जाई)।

मतलब बा: चीनी अनुवाद जापानी, कोरियाई, अंग्रेजी, अंग्रेजी अनुवाद बाकी सभ भाषा में। अगर रउआ खाली चीनी आ अंग्रेजी के समर्थन करे के बा त बस `zh: en` लिख सकेनी।

मतलब बा: चीनी अनुवाद जापानी, कोरियाई, अंग्रेजी, अंग्रेजी अनुवाद बाकी सभ भाषा में। अगर रउआ खाली चीनी आ अंग्रेजी के समर्थन करे के बा त बस `zh: en` लिख सकेनी।

* [फ्रंट-एंड कोड के बा](https://github.com/xxai-art/web)
* [समग्र रूप से साइट खातिर भाषा पैक](https://github.com/xxai-art/web/tree/main/i18n)
* [लॉगिन मॉड्यूल खातिर भाषा पैक](https://github.com/wacpkg/user/tree/main/ui.i18n)
* [वेबसाइट बहुभाषी दस्तावेजीकरण के बा](https://github.com/xxai-doc)

फ्रंट-एंड प्रोग्रामिंग भाषा [@w5/coffee_plus](http://npmjs.com/@w5/coffee_plus) बाटे, जवन कॉफीस्क्रिप्ट सिंटैक्स के आधार पर कुछ फीचर जोड़े ला, देखल जाय [./coffee_plus.md](./coffee_plus.md) ।

## वेबसाइट आ दस्तावेजन के अंतर्राष्ट्रीयकरण

निम्नलिखित 3 परियोजना पर निर्माण करीं

* [@w5/mdt के बा](https://www.npmjs.com/package/@w5/mdt)

  प्रत्यय `.mdt` बा, रउआँ बाहरी फाइल सभ के संदर्भ देवे खातिर `<+ ./coffee_plus/import.js>` नियर सिंटैक्स के इस्तेमाल क सकत बानी, आ `.md` प्रत्यय के साथ मार्कडाउन जनरेट क सकत बानी।

* [@w5/trmd के बा](https://www.npmjs.com/package/@w5/trmd)

  मार्कडाउन अनुवाद से कोड आ लिंक के अनुवाद ना होखी, आ अनुवादित वाक्यन के कैश कइल जाई. अगर अनुवाद में संशोधन कइल गइल होखे बाकी मूल पाठ में संशोधन ना भइल होखे तब एकरा के दोबारा निष्पादित कइला से अनुवाद के संशोधन के ओवरराइट ना कइल जाई।

* [@w5/i18n के बा](https://www.npmjs.com/package/@w5/i18n)

  `yaml` जनरेट कइल वेबसाइट सभ के अनुवाद करे खातिर भाषा फाइल।

### दस्तावेज अनुवाद स्वचालन के निर्देश दिहल गइल बा

कोड रिपोजिटरी [xxai-art/doc](https://github.com/xxai-art/doc) देखल जाय

ई सलाह दिहल जाला कि पहिले nodejs, [direnv](https://direnv.net) , [bun](https://github.com/oven-sh/bun) इंस्टॉल कइल जाय, आ फिर डाइरेक्टरी में प्रवेश कइला के बाद `direnv allow` ( डाइरेक्टरी में प्रवेश कइला के बाद [.envrc](https://github.com/xxai-art/doc/blob/main/.envrc) स्वचालित रूप से निष्पादित हो जाई)।

सैकड़न भाषा में अनुवादित बड़हन कोड बेस से बचे खातिर हम हर भाषा खातिर अलग से कोड बेस बनवनी आ कोड बेस के स्टोर करे खातिर एगो संगठन बनवनी

वातावरण चर `GITHUB_ACCESS_TOKEN` सेट कइल आ फिर [create.github.coffee](https://github.com/xxai-art/doc/blob/main/create.github.coffee) चलावे से कोड रिपोजिटरी स्वचालित रूप से बन जाई।

बेशक, रउआ एकरा के कोड बेस में भी डाल सकेनी।

अनुवाद स्क्रिप्ट संदर्भ [run.sh के](https://github.com/xxai-art/doc/blob/main/run.sh) बा

स्क्रिप्ट कोड के व्याख्या निम्नलिखित तरीका से कइल जाला:

[bunx](https://bun.sh/docs/cli/bunx) npx के जगह ह, जवन तेज बा। बेशक, अगर रउरा लगे बन इंस्टॉल नइखे त एकरा बदले `npx` इस्तेमाल कर सकीलें.

`bunx mdt zh` डाइरेक्टरी में `.mdt` `.md` के रूप में रेंडर करे ला, नीचे दिहल 2 गो लिंक कइल फाइल सभ के देखल जाय

* [कॉफी_प्लस.एमडीटी के बा](https://github.com/xxai-doc/zh/blob/main/coffee_plus.mdt)
* [कॉफी_प्लस.एमडी के बा](https://github.com/xxai-doc/zh/blob/main/coffee_plus.md)

`bunx i18n` अनुवाद खातिर कोर कोड हवे (अगर रउआँ के लगे खाली `nodejs` इंस्टॉल बा, बाकी `bun` आ `direnv` इंस्टॉल नइखे, त रउआँ अनुवाद करे खातिर `npx i18n` भी चला सकत बानी)।

ई [i18n.yml के](https://github.com/xxai-art/doc/blob/main/i18n.yml) पार्स करी, एह दस्तावेज में `i18n.yml` के कॉन्फ़िगरेशन निम्नलिखित बा:

```
en:
zh: ja ko en
```

मतलब बा: चीनी अनुवाद जापानी, कोरियाई, अंग्रेजी, अंग्रेजी अनुवाद बाकी सभ भाषा में। अगर रउआ खाली चीनी आ अंग्रेजी के समर्थन करे के बा त बस `zh: en` लिख सकेनी।

अंतिम बा [gen.README.coffee](https://github.com/xxai-art/doc/blob/main/gen.README.coffee) , जवन हर भाषा के `README.md` के मुख्य शीर्षक आ पहिला उपशीर्षक के बीच के सामग्री के निकाल के एगो प्रविष्टि `README.md` पैदा करेला। कोड बहुत सरल बा, रउआ खुदे देख सकेनी।

गूगल एपीआई के इस्तेमाल मुफ्त अनुवाद खातिर कइल जाला। अगर रउआँ गूगल तक ना पहुँच पावत बानी त कृपया कवनो प्रॉक्सी कॉन्फ़िगर आ सेट करीं, जइसे कि:

```
export https_proxy=http://127.0.0.1:7890 http_proxy=http://127.0.0.1:7890 all_proxy=socks5://127.0.0.1:7890
```

अनुवाद स्क्रिप्ट `.i18n` डाइरेक्टरी में अनुवादित कैश पैदा करी, कृपया एकरा के `git status` के साथ जांच करीं आ कोड रिपोजिटरी में जोड़ीं ताकि बार-बार अनुवाद ना होखे।

कृपया हर बेर जब कैश अपडेट करे खातिर अनुवाद में संशोधन करीं त `bunx i18n` चलाईं।

अगर मूल पाठ आ अनुवाद के एक साथ संशोधित कइल जाय तब कैश में भ्रम पैदा हो जाई, एह से अगर आप संशोधित कइल चाहत बानी त खाली एक के संशोधित क सकत बानी, आ फिर कैश के अपडेट करे खातिर `bunx i18n` चला सकत बानी।
