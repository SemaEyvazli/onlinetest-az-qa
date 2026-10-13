# Negative Test Cases
| ID | Başlıq | Priority | Preconditions | Steps | Expected | Actual | Status |
|---|---|---|---|---|---|---|---|
| TC_NEG_001 | Çox uzun mətn (500+ simvol) | Medium | | 1. Sahəyə uzun mətn yaz | Limit və ya xəta mesajı | | Not Run |
| TC_NEG_002 | Xüsusi simvollar | Medium | | 1. Xüsusi simvollar daxil et (!@#$%^&*) | Düzgün işlənir | | Not Run |
| TC_NEG_003 | Yalnız boşluq | Medium | | 1. Boşluq daxil et | Required xətası | | Not Run |
| TC_NEG_004 | İnternet kəsilməsi test zamanı | High | Test gedir | 1. Şəbəkəni kəs 2. Bərpa et | Cavablar itmir / xəbərdarlıq | | Not Run |
| TC_NEG_005 | Eyni anda iki brauzerdə login | Medium | | 1. Eyni hesabla 2 yerdə daxil ol | Gözlənilən davranış | | Not Run |
| TC_NEG_006 | Sürətli təkrar klik (double submit) | Medium | | 1. Submit-ə tez-tez bas | Dublikat yaranmır | | Not Run |
