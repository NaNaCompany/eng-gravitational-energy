# 중력 위치에너지 계산기

무한대를 기준으로 한 천체 중력 위치에너지 계산

- Plan ID: E054
- App: https://nanalab.kr/eng-gravitational-energy/
- Repository: https://github.com/NaNaCompany/eng-gravitational-energy
- Formula: `U = −GMm/r`
- Output: 중력 위치에너지 U

## Model

M,m,r>0. 구대칭 천체 외부와 뉴턴 중력, 시험질량을 가정한다. 무한대에서 U=0이므로 결과는 음수다. 지표 근처 mgh 변화량과 구분한다.

Inputs are normalized to SI. Only one scalar is returned. Model conditions, finite numbers, physical boundaries, overflow and underflow are checked. External solver APIs and property databases are not used.

## Verification

Run `node --test tests/*.test.mjs` with Node.js 22 or later. Independent 70-digit Decimal example result: `-56943220657.1429`. Source and license notices are in [SOURCES.md](SOURCES.md) and [LICENSE](LICENSE).

## Hosting

GitHub Pages uses `main` and `/`, with the NaNaCompany domain inherited. Google GTM, GA4, AdSense, Cloudflare analytics and the gray More Apps link are included. All code, descriptions and graphics are original.

## Static languages

Korean (existing root), English (`en/`), Spanish (`es/`), Simplified Chinese (`zh/`), Japanese (`ja/`) and German (`de/`). Each page has its own canonical URL, reciprocal hreflang, localized metadata, interface, validation messages and preview image. The language links work without JavaScript. Calculation code is shared and no runtime translation API is used.

Edit `localization/*.json` for text, `src/template.html` for the shared page, and run `python scripts/build-locales.py`. Run `python scripts/build-locales.py --check` and `npm test` before publishing. Decimal commas are accepted in Spanish and German; thousands separators are not supported.
