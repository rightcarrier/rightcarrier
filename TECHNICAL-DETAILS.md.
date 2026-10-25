# Mechanism

This file answers the question the other files left open: how it
works in practice. What the previous files described is the promise.
This file describes the machinery behind the promise.

## The foundation — cryptography

The whole model stands on asymmetric cryptography, the same family
of tools that protects payments and messages today. Each party holds
a pair of keys: a private key, kept secret, and a public key, open
to everyone. What one key signs, the other verifies — without secrets,
without trust in words.

Three pairs of keys matter:

- the store's pair: the store signs every carrier it issues;
- the platform owner's pair: it signs the rules — the list of
  supported devices and drives, the terms of transfer;
- the device's pair: every supported device holds its own key,
  sewn into it at the factory, in protected memory that cannot be
  read or rewritten from outside.

A signature is the heart of the model. A forged carrier has no
genuine signature; a device checks the signature before accepting
anything. Trust is not asked — it is verified.

## The birth of a carrier

When you buy a game, the store creates the carrier in three steps:

1. The store generates a unique identity for the carrier — a number
   that has never existed before and will never exist again.
2. The store writes the license record: what the right is, when it
   was born, what it allows — use, copy for personal use, give,
   sell, inherit.
3. The store signs the whole record with its private key. Now the
   record cannot be changed by anyone without breaking the signature.

The record is added to the register: the public list of carriers and
their rights. The register holds no content and no secrets — only
facts: this identity exists, it holds this right, it was signed by
this store.

## How the carrier reaches a device

The signed record is small — kilobytes, not gigabytes. It can arrive
in two ways:

- over the internet, onto a supported device, as downloads work
  today;
- through a supported drive: the device writes the signed record
  into the drive's protected area — a part of the drive's memory
  that ordinary reading and writing cannot touch. Only the transfer
  procedure can write there, and only by the rules.

The content — the game, the film, the album — is not signed by hand
and not hidden in the carrier. It is downloaded from official sources
and checked against a hash: a fingerprint of the file that the store
signs together with the license. If a single byte of the content
changes, the fingerprint stops matching, and the device refuses it.
Fake content cannot pretend to be the bought one.

## Two modes of storage

The user chooses where the right lives — and with the choice, its
price.

**Mode B — the device holds the right. No drive.**

The license is written into the device's protected memory —
permanently, without a term. Verification is local; the network is
needed once, at purchase. This is convenience: buy and live, as
digital purchases work today — only honest.

The price, chosen openly:

- a broken device takes the right with it — as a burned disc did;
- against a lying device there is no second line: everything rests
  on the physics of the secure element and the economics of breach.

**Mode A — the drive holds the right. The device holds a lease.**

The right lives on the drive; the device holds a signed lease with
an expiry. Insert the drive — the device is bound for the term. The
term ends — access fades; insert the drive — it renews.

The rules of the term:

- the timer lives in the drive's secure element — the device cannot
  lie to it about time;
- the term itself is set by the platform owner as a rule; the user
  can only shorten it — useful when selling: «free in a week»;
  lengthening is not permitted;
- renewal always requires the drive — the ritual of possession.

The price, chosen openly:

- the drive must be kept and inserted on time;
- a lost drive, before the end of support, is a lost access.

Transitions between the modes are the same transfer procedure: erase
at the old place, write at the new one. And sale or gift always goes
through the drive, from either mode: to move a right, it must first
be placed on the drive — the thing is transferred as a thing.

## The sixty-day rule

A fresh purchase cannot travel at once. For sixty days after the
purchase, the license is locked: it can be used, but not transferred —
neither by the drive nor by the wire.

This is the anti-fraud lock. The typical fraud today: buy, download,
return or charge back — and keep the copy. With the lock, the fraud
collapses: the return window closes long before the transfer lock
opens. Sixty days is not a decoration — it is the gap between «money
can still be taken back» and «the right can start traveling».

## The transfer procedure

Transfer — by drive or by wire — is not a user action on files. It is
a procedure built into the device, and the procedure does the work:

1. The device checks the license: genuine signature, sixty days
   passed, no lock left — and its own firmware intact.
2. The device erases the license from its own memory — at once, not
   «later».
3. Only then does the license arrive at the new place: onto the
   drive's protected area, or through the wire into the other device.

The order matters: erase first, deliver second. If the delivery
fails, the procedure repeats it from the register or from the signed
record the store gave — the license is never left in two places,
never lost.

The user cannot perform this by hand. There is no menu item «copy
license», no file to drag. The rules travel inside the device, and
the device obeys the platform owner, not the person holding it.

## The refusing device — firmware integrity

Two misfortunes must not be confused:

- a broken device — the hammer, the water, the burned board: the
  honest owner's misfortune, and the right survives it on the drive;
- a hacked device — the cryptography opened: the device keeps working,
  playing, looking normal. Only one fact changed: it can be talked
  into lying about erasing.

A hacked device is not bricked and is not punished — punishment after
the theft is useless, and the brick strikes the honest owner. Instead,
the model refuses the function, not the thing:

- the secure element holds the hash of the current firmware;
- before any transfer, the element checks the firmware against the
  hash: intact — the procedure runs; altered — the element goes
  silent;
- a silent element does not kill the device: it plays, downloads,
  lives — but it can no longer hand a license to anyone, by drive or
  by wire.

A device that cannot be trusted is no longer a door through which
rights can leave. The owner loses nothing — the right lives on the
drive, and any honest device can carry it onward.

## What changes in the digital goods themselves

Not much — and that is the point. The game stays a game; the film
stays a film. What changes is the wrapper:

- the store adds a signed license record and a content fingerprint
  to every purchase;
- the device stores the license in protected memory, next to the
  content, and checks both at launch;
- nothing requires the device to be online at play time — the check
  is local, the signatures are checked on the device itself.

An old game, a film from a closed service, an album removed from
shelves — all keep working: their license is signed once and does not
need anyone's permission to exist.

## What remains of accounts

Accounts do not disappear — they lose their power. An account keeps
what accounts are good at: your personal data, your purchase history,
your receipts. It no longer holds the rights: the rights live in
carriers, outside any account.

This changes the meaning of «account transfer». There is nothing
valuable to transfer: whoever receives your account receives history,
not property. Selling an account becomes pointless — the things are
transferred by the drive and the wire, the way things are transferred,
without touching the account at all.

## The store's balance on drives

The same mechanism that carries rights can carry money. A store can
issue a balance carrier — a signed record of store credit, exactly
like the license of a game:

- the store signs the amount and issues it — onto an account or onto
  a drive;
- the balance carrier is transferable: hand over the drive, and the
  credit changes hands;
- the register confirms the balance the same way it confirms a
  license.

This is the gift card of the new model — but honest: verifiable,
transferable, alive offline. A balance given to a child, a balance
sold to a friend, a balance that survives the store itself: the
signature stands even when the store does not.

## What the rest of the story lives where

- how the device is protected — physics, the lease, the refusal,
  and what a breach costs: DEFENSE.md;
- what can be done on today's devices without new hardware:
  ROADMAP.md.

## What is still open

Honesty requires a list of open questions — and a note of what this
file already settled:

- the format of the signed record — settled in outline here:
  identity, right, birth date, allowed actions, content fingerprint,
  locks and terms;
- the wire protocol — settled in outline: mutual verification of
  support, firmware integrity on both sides, the erase-then-deliver
  order; the exact cable layer remains open;
- the register: who runs it, who mirrors it — an organizational
  question, not a technical one;
- the lying device — the hardest problem of this field. The model
  reduces it; the full picture of how, and at what price, lives in
  DEFENSE.md.

-----------------------------------------------------------------------

# Механизм

Этот файл отвечает на вопрос, который остальные файлы оставили
открытым: как это работает на практике. То, что описано в прошлых
файлах, — обещание. Здесь — механика за обещанием.

## Фундамент — криптография

Вся модель стоит на асимметричной криптографии — том же семействе
инструментов, что сегодня защищает платежи и переписку. У каждой
стороны пара ключей: закрытый, хранимый в секрете, и открытый,
доступный всем. Что один ключ подписал, другой проверяет — без
секретов, без доверия к словам.

Важны три пары ключей:

- пара магазина: магазин подписывает каждый выпущенный носитель;
- пара владельца платформы: он подписывает правила — список
  поддерживаемых устройств и флешек, условия передачи;
- пара устройства: каждое поддерживаемое устройство держит свой
  ключ, вшитый на заводе, в защищённую память, которую нельзя
  прочитать или переписать снаружи.

Подпись — сердце модели. У подделки нет настоящей подписи; устройство
проверяет подпись, прежде чем принять что-либо. Доверие не
выпрашивается — оно проверяется.

## Рождение носителя

Когда вы покупаете игру, магазин создаёт носитель в три шага:

1. Магазин генерирует уникальную личность носителя — число, которое
   не существовало никогда и не будет существовать больше никогда.
2. Магазин пишет лицензионную запись: какое это право, когда оно
   родилось, что оно разрешает — пользоваться, копировать для
   личного использования, подарить, продать, передать по наследству.
3. Магазин подписывает всю запись закрытым ключом. Теперь запись
   нельзя изменить, не сломав подпись.

Запись добавляется в реестр — открытый список носителей и их прав.
Реестр не хранит ни содержимого, ни секретов — только факты: эта
личность существует, она несёт такое-то право, она подписана таким-то
магазином.

## Как носитель попадает на устройство

Подписанная запись мала — килобайты, а не гигабайты. Она приходит
двумя путями:

- по интернету, на поддерживаемое устройство, как работает скачивание
  сегодня;
- через поддерживаемую флешку: устройство записывает подписанную
  запись в защищённую область флешки — часть памяти, куда обычное
  чтение и запись не достают. Туда пишет только процедура передачи,
  и только по правилам.

Содержимое — игра, фильм, альбом — не прячется в носитель и не
подписывается вручную. Оно скачивается из официальных источников
и сверяется с хешем — отпечатком файла, который магазин подписывает
вместе с лицензией. Если хоть один байт содержимого изменился,
отпечаток перестал сходиться — устройство отказывает. Фальшивое
содержимое не выдаст себя за купленное.

## Два режима хранения

Пользователь выбирает, где живёт право, — и вместе с выбором его цену.

**Режим Б — право в устройстве. Без флешки.**

Лицензия записывается в защищённую память устройства — постоянно,
без срока. Проверка локальна; сеть нужна один раз, при покупке.
Это удобство: купил и живёшь, как работает цифровая покупка сегодня, —
только честно.

Цена, выбранная открыто:

- сломанное устройство уносит право с собой — как сгоревший диск;
- против лгущего устройства нет второй линии: всё держится на физике
  защищённого элемента и экономике взлома.

**Режим А — право на флешке. Устройство держит аренду.**

Право живёт на флешке; устройство держит подписанную аренду со
сроком. Вставил флешку — устройство привязано на срок. Срок кончился —
доступ погас; вставил флешку — продлился.

Правила срока:

- таймер живёт в защищённом элементе флешки — устройство не может
  солгать ей о времени;
- сам срок задаёт владелец платформы как правило; пользователь может
  только укоротить его — полезно при продаже: «свободно через
  неделю»; удлинять нельзя;
- продление всегда требует флешку — ритуал владения.

Цена, выбранная открыто:

- флешку надо хранить и вовремя вставлять;
- потерянная флешка до конца поддержки — потерянный доступ.

Переходы между режимами — та же процедура передачи: стереть на старом
месте, записать на новом. И продажа или дарение всегда идут через
флешку, из любого режима: чтобы переместить право, его надо сначала
посадить на флешку — вещь передаётся как вещь.

## Правило шестидесяти дней

Свежая покупка не может путешествовать сразу. Шестьдесят дней после
покупки лицензия закрыта: ею можно пользоваться, но нельзя передать —
ни флешкой, ни проводом.

Это замок против мошенничества. Типичное мошенничество сегодня:
купил, скачал, вернул товар или оспорил платёж — а копия осталась.
С замком схема рушится: окно возврата закрывается задолго до того,
как откроется замок передачи. Шестьдесят дней — не украшение: это
зазор между «деньги ещё можно вернуть» и «право может начать
путешествовать».

## Процедура передачи

Передача — флешкой или проводом — не действие пользователя над
файлами. Это процедура, вшитая в устройство, и работу делает она:

1. Устройство проверяет лицензию: подпись подлинная, шестьдесят дней
   прошли, замков не осталось — и целостность собственной прошивки.
2. Устройство стирает лицензию из своей памяти — сразу, не «потом».
3. Только тогда лицензия приходит на новое место: в защищённую
   область флешки или по проводу в другое устройство.

Порядок важен: сначала стереть, потом доставить. Если доставка не
удалась, процедура повторяет её по реестру или по подписанной записи,
которую выдал магазин, — лицензия никогда не остаётся в двух местах
и не теряется.

Пользователь не может сделать это руками. Нет пункта меню «скопировать
лицензию», нет файла, который можно перетащить. Правила путешествуют
внутри устройства, и устройство подчиняется владельцу платформы,
а не тому, кто его держит.

## Отказывающее устройство — целостность прошивки

Две беды нельзя путать:

- сломанное устройство — молоток, вода, сгоревшая плата: беда честного
  владельца, и право переживает её на флешке;
- взломанное устройство — вскрытая криптография: устройство продолжает
  работать, играть, выглядеть обычно. Изменился один факт: его можно
  уговорить лгать о стирании.

Взломанное устройство не превращается в кирпич и не наказывается —
наказание после кражи бесполезно, а кирпич бьёт по честному владельцу.
Вместо этого модель отказывает функции, не вещи:

- защищённый элемент хранит хеш текущей прошивки;
- перед любой передачей элемент сверяет прошивку с хешем: целая —
  процедура идёт; изменённая — элемент умолкает;
- умолкший элемент не убивает устройство: оно играет, скачивает,
  живёт — но больше не может отдать лицензию никому, ни флешкой,
  ни проводом.

Устройство, которому нельзя доверять, перестаёт быть дверью, через
которую уходят права. Владелец не теряет ничего — право живёт на
флешке, и любая честная приставка донесёт его дальше.

## Что меняется в самих цифровых товарах

Немногое — и в этом смысл. Игра остаётся игрой, фильм — фильмом.
Меняется упаковка:

- магазин добавляет к каждой покупке подписанную лицензионную запись
  и отпечаток содержимого;
- устройство хранит лицензию в защищённой памяти, рядом с
  содержимым, и проверяет оба при запуске;
- ничто не требует сети во время игры — проверка локальна, подписи
  проверяются на самом устройстве.

Старая игра, фильм закрытого сервиса, альбом, исчезнувший с полок, —
всё продолжает работать: лицензия подписана один раз и не нуждается
ни в чьём разрешении, чтобы существовать.

## Что остаётся от аккаунтов

Аккаунты не исчезают — они теряют власть. Аккаунт хранит то, в чём
аккаунты хороши: ваши личные данные, историю покупок, чеки. Права
он больше не держит: права живут в носителях, вне всякого аккаунта.

Это меняет смысл «передачи аккаунта». Передавать нечего: получивший
ваш аккаунт получает историю, а не имущество. Продавать аккаунт
становится бессмысленно — вещи передаются флешкой и проводом, как
передаются вещи, не трогая аккаунт вовсе.

## Баланс магазина на флешках

Тот же механизм, что переносит права, может переносить деньги.
Магазин может выпустить носитель баланса — подписанную запись о
магазинском кредите, ровно как лицензию игры:

- магазин подписывает сумму и выдаёт её — на аккаунт или на флешку;
- носитель баланса передаётся: передал флешку — кредит сменил
  владельца;
- реестр подтверждает баланс так же, как подтверждает лицензию.

Это подарочная карта новой модели — но честная: проверяемая,
передаваемая, живущая офлайн. Баланс, подаренный ребёнку, баланс,
проданный другу, баланс, который переживёт сам магазин: подпись
стоит, даже когда магазина нет.

## Где живёт остальная история

- как устройство защищено — физика, аренда, отказ и цена взлома:
  DEFENSE.md;
- что можно сделать на нынешних устройствах без нового железа:
  ROADMAP.md.

## Что остаётся открытым

Честность требует списка открытых вопросов — и пометки о том, что
этот файл уже решил:

- формат подписанной записи — решён в очертаниях здесь: личность,
  право, дата рождения, разрешённые действия, отпечаток содержимого,
  замки и сроки;
- протокол провода — решён в очертаниях: взаимная проверка
  поддержки, целостность прошивки с обеих сторон, порядок «стереть,
  потом доставить»; кабельный слой остаётся открытым;
- реестр: кто ведёт, кто зеркалит — организационный вопрос, а не
  технический;
- лгущее устройство — труднейшая проблема всей области. Модель её
  снижает; полная картина — как и какой ценой — живёт в DEFENSE.md.
