# Login Test Cases
| ID | Başlıq | Priority | Preconditions | Steps | Expected | Actual | Status |
|---|---|---|---|---|---|---|---|
| TC_010 | Düzgün məlumatlarla login | High | Hesab mövcuddur | 1. Email və parol daxil et 2. Login | İstifadəçi sistemə daxil olur | | Not Run |
| TC_011 | Yanlış parol | High | | 1. Düzgün email, yanlış parol | Xəta mesajı göstərilir | | Not Run |
| TC_012 | Mövcud olmayan istifadəçi | High | | 1. Qeydiyyatsız email daxil et | Xəta mesajı | | Not Run |
| TC_013 | Boş sahələr | Medium | | 1. Login-ə boş klik | Required mesajları | | Not Run |
| TC_014 | Logout | High | Login olunub | 1. Logout düyməsi | Sessiya bitir, login səhifəsinə yönləndirilir | | Not Run |
| TC_015 | Parolun bərpası | Medium | | 1. "Parolu unutdum" 2. Email daxil et | Bərpa linki göndərilir | | Not Run |
| TC_016 | Logout-dan sonra Back düyməsi | Medium | Logout olunub | 1. Brauzerdə Back | Qorunan səhifə açılmamalıdır | | Not Run |
