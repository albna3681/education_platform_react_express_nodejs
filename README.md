# 🎓 منصة تعليمية  front end + backend  |  Educational Platform

<div align="center">

![Platform Banner](https://via.placeholder.com/1200x300/667eea/ffffff?text=Educational+Platform)

**منصة تعليمية شاملة لإدارة الكورسات والطلاب مع نظام دفع متكامل**

[![License](https://img.shields.io/badge/License-Proprietary-red.svg)](LICENSE)
[![Status](https://img.shields.io/badge/Status-Production-success.svg)]()
[![Version](https://img.shields.io/badge/Version-3.0.0-blue.svg)]()

[🎥 شاهد الفيديو التوضيحي](https://drive.google.com/file/d/YOUR_VIDEO_ID/view)

</div>

---

## 📖 نظرة عامة | Overview

منصة تعليمية متكاملة مصممة خصيصاً لإدارة الكورسات التعليمية والطلاب مع نظام دفع إلكتروني آمن. المشروع يوفر تجربة مستخدم سلسة مع واجهة حديثة ونظام إدارة قوي.

### ✨ المميزات الرئيسية | Key Features

#### 🎯 للطلاب | Student Features
- ✅ **نظام تسجيل آمن** - تسجيل دخول بالبريد الإلكتروني أو رقم الهاتف
- 🎥 **مشاهدة الفيديوهات** - مشغل فيديو محمي مع Plyr.js
- 📚 **إدارة الكورسات** - عرض الكورسات المشترك فيها
- 💳 **نظام الدفع** - تفعيل الكورسات عبر أكواد التفعيل
- 🔐 **حماية المحتوى** - منع تحميل ونسخ الفيديوهات
- 📱 **Responsive Design** - متوافق مع جميع الأجهزة
- 🌙 **Dark Mode** - وضع مظلم تلقائي

#### 👨‍🏫 للمدرسين | Teacher Features
- 📊 **لوحة تحكم متقدمة** - إحصائيات تفصيلية
- ➕ **إدارة الكورسات** - إضافة وتعديل الكورسات
- 🎬 **رفع الفيديوهات** - إضافة فيديوهات YouTube
- 👥 **إدارة الطلاب** - متابعة المشتركين
- 💰 **نظام الأكواد** - توليد أكواد التفعيل
- 📈 **التقارير** - تقارير مفصلة عن الإيرادات

#### 🔧 للإدارة | Admin Features
- 🎛️ **لوحة تحكم شاملة** - إدارة كاملة للمنصة
- 👤 **إدارة المستخدمين** - طلاب ومدرسين
- 💼 **إدارة الكورسات** - جميع الكورسات
- 📊 **الإحصائيات** - تقارير مفصلة
- 🔒 **الأمان** - إدارة الصلاحيات

---

## 🛠️ التقنيات المستخدمة | Tech Stack

### 🎨 Frontend
{
"framework": "React 18.3.1",
"routing": "React Router DOM 6.x",
"styling": "Pure CSS (Custom Design System)",
"icons": "Font Awesome 6.x",
"video-player": "Plyr.js 3.7.8",
"http-client": "Axios 1.7.2"
}


### ⚙️ Backend

{
"runtime": "Node.js 18.x",
"framework": "Express.js 4.19.2",
"database": "MySQL 8.0",
"authentication": "JWT + Sessions",
"security": "bcryptjs, express-validator",
"cors": "CORS enabled"
}



### 🗄️ قاعدة البيانات | Database

#### 📊 الجداول الرئيسية | Main Tables

**جدول المستخدمين (users_YEAR)**

id (Primary Key)

name (الاسم الكامل)

email (البريد الإلكتروني - Unique)

phone (رقم الهاتف - Unique)

password (كلمة المرور المشفرة)

grade (الصف الدراسي)

isTeacher (حالة المدرس)

teacherId (معرف المدرس)

c1...c25 (حالة الاشتراك في الكورسات)

device_idd (معرف الجهاز)

created_at, updated_at

**جدول الكورسات (courses_YEAR)**
Courseid (Primary Key)

coursename (اسم الكورس)

coursedescription (الوصف)

courseprice (السعر)

isfree (مجاني؟)

grade (الصف)

teacherId (معرف المدرس)

created_at, updated_at

**جدول الفيديوهات (videos_YEAR)**

id (Primary Key)

video_title (عنوان الفيديو)

video_description (الوصف)

link (رابط YouTube)

video_duration (المدة)

Courseid (معرف الكورس - Foreign Key)

created_at

**جدول الأكواد (codes_YEAR)**

id (Primary Key)

code (كود التفعيل - Unique)

courseId (معرف الكورس)

isUsed (مستخدم؟)

usedBy (معرف المستخدم)

usedAt (تاريخ الاستخدام)

created_at

**جدول الإشعارات (notifications_YEAR)**

id (Primary Key)

userId (معرف المستخدم)

message (نص الإشعار)

isRead (مقروء؟)

created_at


---

## 🚀 بنية المشروع | Project Structure


educational-platform-v3/
│
├── 📁 frontend/ # تطبيق React
│ ├── 📁 public/
│ │ ├── index.html
│ │ └── favicon.ico
│ ├── 📁 src/
│ │ ├── 📁 components/ # المكونات المشتركة
│ │ │ ├── Header.jsx
│ │ │ ├── Footer.jsx
│ │ │ └── ProtectedRoute.jsx
│ │ ├── 📁 pages/ # الصفحات
│ │ │ ├── Login.jsx
│ │ │ ├── Register.jsx
│ │ │ ├── Dashboard.jsx
│ │ │ ├── Courses.jsx
│ │ │ ├── CourseContent.jsx
│ │ │ ├── Videos.jsx
│ │ │ ├── Enroll.jsx
│ │ │ ├── TeacherDashboard.jsx
│ │ │ └── AdminDashboard.jsx
│ │ ├── 📁 context/ # Context API
│ │ │ ├── AuthContext.jsx
│ │ │ └── TeacherContext.jsx
│ │ ├── 📁 services/ # خدمات API
│ │ │ └── api.js
│ │ ├── App.js
│ │ └── index.js
│ └── package.json
│
├── 📁 backend/ # خادم Node.js
│ ├── 📁 config/
│ │ └── database.js # إعدادات قاعدة البيانات
│ ├── 📁 middleware/
│ │ ├── auth.js # التحقق من JWT
│ │ └── validation.js # التحقق من البيانات
│ ├── 📁 routes/
│ │ ├── auth.routes.js # مسارات التسجيل
│ │ ├── courses.routes.js # مسارات الكورسات
│ │ ├── videos.routes.js # مسارات الفيديوهات
│ │ ├── enroll.routes.js # مسارات التفعيل
│ │ ├── teacher.routes.js # مسارات المدرسين
│ │ └── admin.routes.js # مسارات الإدارة
│ ├── server.js
│ └── package.json


---

## 🔐 الأمان والحماية | Security Features

### 🛡️ إجراءات الأمان المطبقة

- ✅ **تشفير كلمات المرور** - bcryptjs مع Salt Rounds = 10
- ✅ **JWT Authentication** - JSON Web Tokens
- ✅ **Session Management** - إدارة جلسات آمنة
- ✅ **Device Binding** - ربط الحساب بجهاز واحد
- ✅ **SQL Injection Prevention** - Prepared Statements
- ✅ **XSS Protection** - Input Validation & Sanitization
- ✅ **CORS Configuration** - سياسة CORS محددة
- ✅ **Rate Limiting** - منع الهجمات
- ✅ **Content Protection** - منع نسخ وتحميل الفيديوهات
- ✅ **API Authentication** - جميع المسارات محمية

---

## 📊 نظام السنوات الدراسية | Academic Year System

المنصة تدعم **نظام السنوات الديناميكي** حيث يتم إنشاء جداول منفصلة لكل سنة دراسية


