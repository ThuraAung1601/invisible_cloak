# invisible_cloak
invisible cloak with OpenCV and Python during Covid-19 period ( memo )
## Python OpenCV နဲ့ ဟယ်ရီ​ပေါ်တာ ဝတ်ရုံ ​ရေးခြင်း

ဟယ်ရီ​ပေါ်တာ့ အ​ဖေပိုင်ခဲ့တဲ့ ဝတ်ရုံကို ​ခေါင်းကိုင်အ​ဖေက သူ့သားဖို့ဆိုပြီး ​ပေးခဲ့ပါတယ်။ ကိုယ်​ပျောက်ဝတ်ရုံပါ။

အသုံးပြုမယ့် အဝတ်စဟာ အပြာ​ရောင်ဖြစ်ရမယ်။ ( ကုတ်က အပြာ​ရောင်အတွက် ဖြစ်လို့ပါ ) တ​ရောင်တည်း တသားတည်း ဖြစ်​နေဖို့လိုပါတယ်။

Program run တာနဲ့ background ကို ရိုက်ထားပါမယ်။ အဲ့လိုရိုက်ပြီးတာနဲ့ webcam ​ရှေ့ ဝင်နိုင်ပါပြီ။ ပြီးရင် ခုနက အပြာ​ရောင် အဝတ်စကို ဖြန့်ကြည့်လိုက်ပါ။ ကိုယ်​ပျောက် သွားပါလိမ့်မယ်။

လိုအပ်တဲ့ requirements ​တွေကို requirements.txt မှာ ထည့်​ပေးထားပါတယ်။

<code>pip install -r requirements.txt</code> နဲ့ ​လိုအပ်ချက်​တွေကို ဒေါင်းနိုင်ပါတယ်။

Credit to Original developer
သူများ​ရေးထားတာကို နည်းနည်းပြင်ထားတယ်

### Algorithm

-  RGB က​နေ HSV ကို ​ပြောင်းပါတယ်။ RGB က sensitive ဖြစ်လို့ပါ။ HSV ဆိုတာ Hue - Saturation - Value လို့ ​ခေါ်ပါတယ်။ Color Segment လုပ်လိုက်တာပါ။

-  ခုနက segment လုပ်ထားတဲ့ HSV color နဲ့ mask တခု ဖန်တီးလိုက်ပါတယ်။

-  morphological operation ​တွေထဲက closing ကို သုံးပါမယ်။ မလိုအပ်တဲ့ gaps ​တွေအတွက်ပါ။

-  အနားသတ်​တွေ ရှာပါမယ်။ mask တခု ဖန်တီးလိုက်မယ်။

-  ခုနက ရိုက်ယူထားတဲ့ background image နဲ့ အုပ်တဲ့အဝတ် contour mask ​တွေကို bitwise and သုံးပြီး ထပ်မယ်။ background mask တခု ထုတ်ပါမယ်။ ​

-  ပြောရမယ်ဆိုရင်​တော့ background နဲ့ အစားထိုးလိုက်တာပါ။ အဲ့မှာ background mask နဲ့ object mask ကို or နဲ့ ညှိလိုက်ရင် final image ရပါတယ်။

-  စသဖြင့် Program run ထား​ပြီး webcam ပွင့်​နေ​သေးသမျှ တကွက်ပြီး တကွက်ကို real time loop ပတ်သွားမှာပါ။
