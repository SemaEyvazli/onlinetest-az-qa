# Basic Security Test Cases
| ID | Başlıq | Priority | Preconditions | Steps | Expected | Actual | Status |
|---|---|---|---|---|---|---|---|
| TC_SEC_001 | XSS yoxlaması (script tag) | High | | 1. Input sahəsinə script tag yaz | Script icra olunmur | | Not Run |
| TC_SEC_002 | SQL injection (login sahəsi) | High | | 1. Login sahəsinə SQL ifadəsi yaz | Giriş olmur | | Not Run |
| TC_SEC_003 | Parolun maskalanması | Medium | | 1. Parol yaz | Simvollar gizlidir | | Not Run |
| TC_SEC_004 | HTTPS | High | | 1. URL-ə bax | HTTPS aktivdir | | Not Run |
| TC_SEC_005 | Qorunan səhifəyə birbaşa URL ilə giriş | High | Login olunmayıb | 1. URL-i birbaşa aç | Login-ə yönləndirilir | | Not Run |
| TC_SEC_006 | Sessiya bitməsi | Medium | | 1. Uzun müddət gözlə | Sessiya bitir | | Not Run |

> Yalnız icazəniz olan mühitdə test edin.
