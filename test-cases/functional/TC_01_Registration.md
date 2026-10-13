# Registration Test Cases
| ID | Başlıq | Priority | Preconditions | Steps | Expected | Actual | Status |
|---|---|---|---|---|---|---|---|
| TC_001 | Düzgün məlumatlarla qeydiyyat | High | Qeydiyyat səhifəsi açıqdır | 1. Bütün sahələri düzgün doldur 2. Submit | Hesab yaranır, uğur mesajı göstərilir | | Not Run |
| TC_002 | Boş sahələrlə qeydiyyat | High | | 1. Sahələri boş burax 2. Submit | Required xəta mesajları göstərilir | | Not Run |
| TC_003 | Mövcud email ilə qeydiyyat | High | Email artıq qeydiyyatdadır | 1. Mövcud email daxil et 2. Submit | "Email artıq mövcuddur" xətası | | Not Run |
| TC_004 | Yanlış email formatı | Medium | | 1. "abc@" daxil et | Format xətası göstərilir | | Not Run |
| TC_005 | Zəif parol | Medium | | 1. Qısa parol daxil et | Parol tələbləri xəbərdarlığı | | Not Run |
| TC_006 | Parol təsdiqi uyğunsuzluğu | Medium | | 1. Fərqli parollar daxil et | Xəta mesajı | | Not Run |
