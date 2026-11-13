Mohammad Pharmacy Android APK Project
=================================

এই ZIP-এ আপনার আপলোড করা দুইটি HTML সফটওয়্যারকে এক Android অ্যাপে যুক্ত করা হয়েছে:
- স্টক ও বিক্রয় (stock.html)
- দোকান হিসাব (accounting.html)

অফলাইন:
- অ্যাপের HTML ফাইল Android assets-এর ভিতরে আছে; প্রথমবার ইনস্টল হওয়ার পর চালাতে ইন্টারনেট লাগে না।
- WebView DOM Storage/localStorage চালু আছে। দুই HTML অংশের ডাটা আলাদা key-তে একই অ্যাপের লোকাল স্টোরেজে থাকে।
- দুই অংশের নিজস্ব Backup অপশন থেকে আলাদা JSON ব্যাকআপ নিন।

APK তৈরি করার নিয়ম:
1. কম্পিউটারে Android Studio ইনস্টল করুন।
2. Android Studio > Open দিয়ে এই ফোল্ডারটি খুলুন (MedicineShopAPK)।
3. Gradle Sync সম্পন্ন হতে দিন। প্রথমবার Android Gradle Plugin ও AndroidX WebKit ডাউনলোডে ইন্টারনেট লাগবে।
4. Build > Build Bundle(s) / APK(s) > Build APK(s) নির্বাচন করুন।
5. APK পাওয়া যাবে: app/build/outputs/apk/debug/app-debug.apk
6. APK ফোনে কপি করে ইনস্টল করুন। প্রয়োজন হলে Android Settings থেকে ওই ফাইল ম্যানেজারকে Install unknown apps অনুমতি দিন।

গুরুত্বপূর্ণ:
- এখানে প্রস্তুত করা হয়েছে Android Studio project; এই পরিবেশে Android SDK/Gradle build tool নেই, তাই APK binary কম্পাইল বা ফোনে পরীক্ষা করা হয়নি।
- দুই সফটওয়্যারের ডাটা আলাদা থাকবে; একটি অংশের ব্যাকআপ অন্য অংশে restore করা যাবে না।
- অ্যাপ আনইনস্টল/ডাটা clear করলে local data মুছে যেতে পারে। তাই নিয়মিত JSON backup রাখুন।

GitHub দিয়ে মোবাইল থেকেই APK build (কম্পিউটার ছাড়া):
1. ZIP extract করে MedicineShopAPK ফোল্ডারের ভেতরের সব ফাইল নতুন GitHub repository-তে upload করুন (ফোল্ডারটিকে nested অবস্থায় নয়; app/, .github/, build.gradle, settings.gradle ইত্যাদি repository root-এ থাকতে হবে)।
2. Repository-তে Actions tab খুলুন। প্রথমবার workflow অনুমোদন চাইলে Allow দিন।
3. Build Medicine Shop APK workflow চালু করুন; স্বয়ংক্রিয়ভাবে push-এও build হবে।
4. Workflow সফল হলে Actions > সফল run > Artifacts > Mohammad-Pharmacy-debug-APK ডাউনলোড করুন। ZIP খুলে app-debug.apk পাবেন।
5. APK ফোনে install করুন।

দোকানের পরিচিতি:
নাম: Mohammad Pharmacy
ঠিকানা: 491/1 East Kazipara, Kafrul, Mirpur, Dhaka
ফোন: 01325682483
