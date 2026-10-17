NOVA PWA — Windows / VS Code में चलाने का तरीका

इस ZIP में ये फाइलें हैं:
- index.html: तुम्हारी मौजूदा NOVA स्क्रीन
- manifest.json: ऐप का नाम, आइकन और इंस्टॉल सेटिंग्स
- sw.js: ऑफलाइन कैश के लिए service worker
- icons/: NOVA के 192px और 512px आइकन

ज़रूरी बात: PWA इंस्टॉल करने के लिए index.html पर सिर्फ डबल-क्लिक मत करना। PWA के लिए localhost या HTTPS ज़रूरी है।

VS Code Live Server से चलाओ:
1. ZIP को डाउनलोड करके Extract All करो।
2. Extract किए गए NOVA_PWA_Package फ़ोल्डर को VS Code में खोलो: File > Open Folder.
3. अगर Live Server इंस्टॉल नहीं है, तो Ctrl+Shift+X दबाओ, Extensions में “Live Server” खोजो और इंस्टॉल करो।
4. VS Code में index.html पर right-click करके “Open with Live Server” चुनो।
5. ब्राउज़र में ऐसा पता खुलेगा: http://127.0.0.1:5500/index.html
6. Chrome या Edge में address bar के Install आइकन या menu से “Install NOVA” चुनो।
7. NOVA को पहली बार खुलने दो, ताकि ऑफलाइन कैश बन सके। ऑफलाइन टेस्ट करते समय Live Server चालू रहना चाहिए।

फोन में इंस्टॉल करने के लिए: लैपटॉप का localhost फोन पर काम नहीं करेगा। PWA को किसी HTTPS वेबसाइट पर होस्ट करना होगा। हम लोकल टेस्ट ठीक होने के बाद यह करेंगे।

तुम्हारा डेटा: NOVA अभी browser localStorage का इस्तेमाल करता है। file:// से localhost या बाद में किसी वेबसाइट पर जाने पर पुराना डेटा अपने-आप नहीं आ सकता। पुरानी HTML फ़ाइल संभालकर रखना और browser data साफ़ मत करना।

NOVA Ask को अभी शामिल नहीं किया गया है—जैसा तय हुआ था, वह सबसे अंत में बनेगा।
