#  Next.js + AWS S3 File Uploader

এই প্রজেক্টে আপনি সহজেই **ইমেজ, ভিডিও, PDF বা যেকোনো ফাইল** AWS S3-এ আপলোড করতে পারবেন।  
একই কোড দিয়ে **single** এবং **multiple** ফাইল আপলোড দুইটাই করা যাবে।  
এছাড়াও, আছে **preview, remove option এবং error handling**।

---

## 🚀 বৈশিষ্ট্যসমূহ

✅ Single & Multiple ফাইল আপলোড  
✅ Preview before upload  
✅ Remove option  
✅ File size ও type validation  
✅ AWS S3 Integration  
✅ Next.js API Routes ব্যবহার করে backend upload  

---

## 🧩 প্রয়োজনীয় টুলস

- Node.js (v18 বা তার উপরে)  
- Next.js 14+  
- AWS Account (S3 bucket তৈরি করার জন্য)  

---

## ⚙️ Step by Step সেটআপ গাইড

### 1️⃣ S3 Bucket তৈরি করা

1. [AWS Console](https://aws.amazon.com/console/) এ লগইন করুন  
2. “S3” সার্ভিসে যান  
3. একটি নতুন bucket তৈরি করুন  
   - উদাহরণঃ `my-next-s3-uploader`
4. “Block all public access” **off** রাখুন (যদি public file upload চান)  
5. Bucket তৈরি হয়ে গেলে নামটি মনে রাখুন (bucket name)

---

### 2️⃣ IAM User তৈরি করা

1. “IAM” সার্ভিসে যান  
2. নতুন একটি user তৈরি করুন  
3. “Attach policies directly” নির্বাচন করুন  
4. **AmazonS3FullAccess** policy যুক্ত করুন  
5. তৈরি শেষে Access key ID ও Secret access key কপি করুন  

---

### 3️⃣ `.env.local` ফাইল তৈরি করুন

Next.js প্রজেক্টের root এ `.env.local` ফাইল বানিয়ে নিচেরগুলো লিখুন👇

```env
AWS_ACCESS_KEY_ID=your_access_key
AWS_SECRET_ACCESS_KEY=your_secret_key
AWS_REGION=ap-south-1
AWS_S3_BUCKET=your_bucket_name
```

