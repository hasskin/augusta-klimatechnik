# Augusta Klimatechnik — сайт и домен

## Текущее состояние
- Код: https://github.com/hasskin/augusta-klimatechnik (пуш в `main` = автодеплой)
- Сайт: https://hasskin.github.io/augusta-klimatechnik/ → после подключения домена
  будет жить на https://augusta-klimatechnik.de/
- Один файл `index.html` + `favicon.svg`, хостинг GitHub Pages (бесплатно)

## Подключение домена augusta-klimatechnik.de (после покупки)
В панели регистратора (IONOS / Strato / All-inkl / Cloudflare) открыть управление
DNS домена и создать записи:

| Тип   | Имя (Host)      | Значение                    |
|-------|-----------------|-----------------------------|
| A     | @               | 185.199.108.153             |
| A     | @               | 185.199.109.153             |
| A     | @               | 185.199.110.153             |
| A     | @               | 185.199.111.153             |
| CNAME | www             | hasskin.github.io           |

(если у регистратора уже стоят свои A/AAAA-записи «парковки» на @ — удалить их;
AAAA для @ можно опционально добавить: 2606:50c0:8000::153, :8001::153,
:8002::153, :8003::153)

Дальше ничего делать не надо: кастом-домен в GitHub Pages уже прописан (файл
`CNAME` в репозитории). Через 15–60 минут после смены DNS GitHub сам выпустит
Let's-Encrypt-сертификат; затем включаем «Enforce HTTPS».

## Почта info@augusta-klimatechnik.de
Почта НЕ у GitHub — её даёт регистратор (у IONOS/Strato обычно входит в тариф).
MX-записи регистратор ставит сам, A/CNAME-записи выше им не мешают.

## Перед «настоящим» запуском заменить
- Телефон 0821 000 00 00 (index.html: шапка, блок Notdienst, контакты; impressum/)
- В impressum/index.html: имя Geschäftsführer (2 места), HRB-номер, USt-IdNr
  (выделены жёлтым на странице)
- Datenschutzerklärung — ещё не создана (обязательно по немецкому праву!)
- Адрес уже настоящий: Barthshof 5, 86150 Augsburg (обновлён 2026-09-21)
