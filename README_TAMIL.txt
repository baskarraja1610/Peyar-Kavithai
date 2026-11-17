பெயர் கவிதை – Netlify வெளியீட்டு வழிகாட்டி

1. Anthropic Console-ல் API key உருவாக்கவும்: https://console.anthropic.com/
   API பயன்பாட்டிற்கு billing/credits தேவைப்படலாம்.
2. இந்த முழு peyar-kavithai folder-ஐ GitHub repository-க்கு upload செய்யவும்.
3. Netlify-ல் Add new site > Import an existing project > GitHub தேர்வு செய்யவும்.
4. Build command காலியாக விடவும்; Publish directory = .
5. Site configuration > Environment variables-ல்:
   ANTHROPIC_API_KEY = உங்களுடைய Claude API key
   ANTHROPIC_MODEL = claude-haiku-4-5-20251001 (தேவைப்பட்டால் உங்கள் கணக்கில் ஆதரிக்கப்படும் model ID)
6. Deploy செய்யவும். Deploy ஆன பிறகு site URL திறந்து சோதிக்கவும்.

PAYMENT குறிப்பு:
- index.html-ல் உள்ள UPI ID baskarraja1610@oksbi; இது உங்களுடைய சரியான UPI ID என்பதை உறுதி செய்யவும்.
- UPI Intent என்பது பணம் செலுத்தும் app-ஐத் திறக்கும் இணைப்பு மட்டுமே.
- இந்த MVP-ல் தானியங்கி payment verification இல்லை. UTR-ஐப் பார்த்து பணம் வந்ததை நீங்கள் கைமுறையாகச் சரிபார்க்க வேண்டும்.
- உண்மையான automatic verification வேண்டுமெனில் Razorpay/ Cashfree போன்ற payment gateway அல்லது வங்கியின் அங்கீகரிக்கப்பட்ட API + server-side webhook தேவை. UTR எண் மட்டும் வைத்து browser-ல் பணம் வந்ததை நிரூபிக்க முடியாது.

பாதுகாப்பு:
- API key-ஐ index.html-ல் ஒருபோதும் சேர்க்க வேண்டாம்.
- API key-ஐ Netlify Environment Variables-ல் மட்டுமே வைக்கவும்.
- API பயன்பாட்டிற்கு செலவு வரலாம்; Anthropic Console-ல் usage limit அமைக்கவும்.
