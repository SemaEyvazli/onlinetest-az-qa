# BUG-001: Login (Daxil ol) səhifəsində canonical və Open Graph meta teqləri ana səhifəyə işarə edir

| Sahə | Dəyər |
|------|-------|
| **Bug ID** | BUG-001 |
| **Modul** | Login / Sign-in (SEO / Meta) |
| **Severity** | Minor |
| **Priority** | Low |
| **Status** | New |
| **Növ** | Frontend / SEO |
| **URL** | https://onlinetest.az/sign-in |
| **Environment** | Chrome (latest), Windows 11 |
| **Tarix** | 13.10.2026 |
| **Reporter** | Sema |
| **Assignee** | |

## Qısa təsvir
`/sign-in` səhifəsinin `<head>` hissəsində `canonical`, `og:url`, `og:title` və `twitter:title` dəyərləri login səhifəsinə yox, **ana səhifəyə** aiddir. Səhifənin `<title>` və `meta description` dəyərləri isə düzgündür ("Daxil ol | Online Test").

## Addımlar (Steps to Reproduce)
1. Brauzerdə https://onlinetest.az/sign-in səhifəsini açın.
2. Səhifədə sağ klik edib **View Page Source** seçin (və ya `Ctrl+U`).
3. `<head>` daxilində aşağıdakı teqləri tapın:
   - `<link rel="canonical">`
   - `<meta property="og:url">`
   - `<meta property="og:title">`
   - `<meta name="twitter:title">`
4. Dəyərləri `<title>` ilə müqayisə edin.

## Gözlənilən nəticə (Expected)
- `canonical` və `og:url` → `https://onlinetest.az/sign-in`
- `og:title` və `twitter:title` → "Daxil ol | Online Test" (səhifənin `<title>` dəyərinə uyğun)

## Faktiki nəticə (Actual)
| Teq | Faktiki dəyər |
|---|---|
| `<title>` | Daxil ol \| Online Test ✅ |
| `meta description` | "Online Test hesabınıza daxil olun və sınaq imtahanlarına başlayın." ✅ |
| `canonical` | `https://onlinetest.az` ❌ |
| `og:url` | `https://onlinetest.az` ❌ |
| `og:title` | "Online Test \| Onlayn Sınaq İmtahanı və Test Platforması" (ana səhifənin başlığı) ❌ |
| `twitter:title` | Ana səhifənin başlığı ❌ |

## Təsir (Impact)
- Axtarış sistemləri login səhifəsini ana səhifənin dublikatı kimi qəbul edə bilər.
- Login linki sosial şəbəkədə / mesencerdə paylaşılanda səhifə başlığı səhv ("ana səhifə" başlığı) görünür.

## Əlavə müşahidə
- `robots` meta teqi `index, follow` göstərir. Login səhifələri adətən axtarışdan çıxarılır (`noindex`). Bunu komanda ilə dəqiqləşdirmək tövsiyə olunur.

## Təklif olunan həll
Hər səhifə üçün öz `canonical`, `og:url`, `og:title`, `twitter:title` dəyərlərini dinamik təyin etmək (layout/template səviyyəsində hardcode olunmuş dəyərləri yoxlamaq). Login üçün `noindex` nəzərdən keçirilməlidir.

## Əlavələr
- Screenshot (View Source, `<head>` hissəsi): `screenshots/BUG-001/head-meta.png`
- Qeyd: Bu tapıntı səhifənin HTML mətninin oxunması ilə müəyyən edilib. Report göndərməzdən əvvəl DevTools → Elements / View Source ilə özünüz təsdiqləyin və screenshot əlavə edin.