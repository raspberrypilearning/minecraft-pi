## आपको किन चीज़ों की आवश्यकता होगी

### सॉफ्टवेयर

#### सॉफ्टवेयर इंस्टालेशन

Minecraft सितंबर 2014 से Raspbian में डिफ़ॉल्ट रूप से इंस्टाल किया गया है।

![Minecraft Pi डेस्कटॉप आइकन](images/minecraft-pi-shortcut.png)

यदि आप Raspbian के पुराने संस्करण का उपयोग कर रहे हैं, तो टर्मिनल विंडो खोलें और निम्नलिखित कमांड टाइप करें (आपको ऑनलाइन होना चाहिए):

```bash
sudo apt-get update
sudo apt-get install minecraft-pi
```

इसके पूरा हो जाने के बाद, Minecraft Pi और Python लाइब्रेरी इंस्टाल की जानी चाहिए।

#### Minecraft का परीक्षण करें

Minecraft चलाने के लिए डेस्कटॉप आइकन पर डबल क्लिक करें या टर्मिनल में `minecraft-pi` दर्ज करें।

![](images/mcpi-start.png)

जब Minecraft Pi लोड हो जाए, तो **Start Game** (गेम स्टार्ट करें) पर क्लिक करें, उसके बाद **Create new** (नया बनाएँ) पर। आप देखेंगे कि मुख्य विंडो थोड़ी-सी ऑफसेट है। इसका मतलब है कि विंडो को आस-पास ड्रैग करने के लिए आपको Minecraft विंडो के पीछे की title (शीर्षक) पट्टी को पकड़ना होगा।

![](images/mcpi-game.png)

अब आप Minecraft के एक गेम में हैं!

#### Python का परीक्षण करें

जब Minecraft चल रहा हो, और दुनिया तैयार हो, तो `Tab` (टैब) कुंजी को दबाकर अपना ध्यान गेम से हटा लें, जिससे आपका माउस मुक्त हो जाएगा। डेस्कटॉप पर Python 3 (IDLE) खोलें और विंडोज़ को खिसकाएँ ताकि दोनों एक दूसरे के आस-पास हों।

आप कमांड या तो सीधे Python विंडो में टाइप कर सकते हैं या एक फाइल बना सकते हैं ताकि आप अपना कोड सहेज सकें और इसे बाद में फिर से चला सकें।

यदि आप एक फाइल बनाना चाहते हैं तो `File > New window` और `File > Save` पर जाएँ।<0><0> आप शायद इसे अपने होम फ़ोल्डर या किसी नए प्रोजेक्ट फ़ोल्डर में सहेजना चाहेंगे।

Minecraft लाइब्रेरी को आयात करके, गेम से कनेक्शन बनाकर और स्क्रीन पर "Hello world" ("हैलो वर्ल्ड") संदेश पोस्ट करके इसका परीक्षण करना आरंभ करें:

```python
from mcpi import minecraft

mc = minecraft.Minecraft.create()

mc.postToChat("Hello world")
```

यदि आप सीधे Python विंडो में कमांड दर्ज कर रहे हैं, तो बस प्रत्येक पंक्ति के बाद `Enter` (एंटर) दबाएँ। यदि यह फ़ाइल है, तो `Ctrl + S` के साथ सहेजें और `F5` के साथ चलाएँ। जब आपका कोड चलता है, तो आपको गेम में स्क्रीन पर अपना संदेश दिखना चाहिए।

![](images/mcpi-idle.png)

यदि आप Minecraft विंडो में "Hello world" ("हैलो वर्ल्ड") देखते हैं, तो आप अगले चरण में जाने के लिए तैयार हैं।