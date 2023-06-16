<p align="center"><a href="https://xxai.art"><img src="https://cdn.jsdelivr.net/gh/xxai-art/doc/logo.svg"/></a><br/><a href="https://xxai.art"><img src="https://cdn.jsdelivr.net/gh/xxai-art/doc/xxai.svg"/></a></p><p align="center"><a href="https://github.com/xxai-art/doc#readme"><img alt="I18N" src="https://cdn.jsdelivr.net/gh/wactax/img/t.svg"/></a>　<a href="https://groups.google.com/u/0/g/xxai-art"><img alt="Google Groups" src="https://cdn.jsdelivr.net/gh/wactax/img/g-groups.svg"/></a></p>

# xxAI.art के बा

वेबसाइट कोड के एगो हिस्सा ओपन सोर्स बा, अनुवाद के अनुकूलित करे में मदद करे खातिर स्वागत बा।

## फ्रंट-एंड कोड के बा

* [फ्रंट-एंड कोड के बा](https://github.com/xxai-art/web)
* [समग्र रूप से साइट खातिर भाषा पैक](https://github.com/xxai-art/web/tree/main/i18n)
* [लॉगिन मॉड्यूल खातिर भाषा पैक](https://github.com/wacpkg/user/tree/main/ui.i18n)
* [वेबसाइट बहुभाषी दस्तावेजीकरण के बा](https://github.com/xxai-doc)

फ्रंट-एंड प्रोग्रामिंग भाषा [@w5/coffee_plus](http://npmjs.com/@w5/coffee_plus) बाटे, जवन कॉफीस्क्रिप्ट सिंटैक्स के आधार पर कुछ फीचर जोड़े ला, देखल जाय [./coffee_plus.md](./coffee_plus.md) ।

## वेबसाइट आ दस्तावेजन के अंतर्राष्ट्रीयकरण

निम्नलिखित 3 परियोजना पर निर्माण करीं

### [@w5/mdt के बा](https://www.npmjs.com/package/@w5/mdt)

मार्कडाउन टेम्पलेट, `.mdt` प्रत्यय के साथ, बाहरी फाइल सभ के संदर्भ दे सके ला जेकर सिंटैक्स `<+ ./coffee_plus/import.js>` नियर होखे।

[@w5/trmd के बा](https://www.npmjs.com/package/@w5/trmd)

मार्कडाउन अनुवाद से कोड आ लिंक के अनुवाद ना होखी, आ अनुवादित वाक्यन के कैश कइल जाई. अगर अनुवाद में संशोधन कइल गइल होखे बाकी मूल पाठ में संशोधन ना भइल होखे तब एकरा के दोबारा निष्पादित कइला से अनुवाद के संशोधन के ओवरराइट ना कइल जाई।

[@w5/i18n के बा](https://www.npmjs.com/package/@w5/i18n)

`yaml` जनरेट कइल वेबसाइट सभ के अनुवाद करे खातिर भाषा फाइल।
