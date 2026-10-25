# Defense

This file answers the question the other files left open: how the
device is defended, and what a breach costs. The promise lives in
CONCEPT and HOW-IT-WORKS; the machinery — in MECHANISM. Here are
the walls.

## The enemy is not the thief. It is the liar.

A thief who steals a drive steals one carrier — one thing, like a
stolen book. The deeper enemy is different: a device persuaded to
lie — to claim it erased a license while keeping it, to claim a
transfer never happened, to claim the signature checked out.

Every copy protection in history died this way: not from broken
cryptography, but from a machine talked into betraying its rules.

The model answers with three walls: physics, the lease, the
refusal — and with an economy that makes the whole affair
unprofitable.

## Wall one — physics

The secure element is a chip inside the device that holds the
device's private key and will not give it out. Not «protected by
law» — cannot: there is no instruction that reads it out, no wire
that carries it away. The key can sign from inside; it cannot be
read.

What this buys:

- a forged carrier has no genuine signature — and the device
  checks the signature before accepting anything;
- a cloned device cannot pretend to be the original: it holds no
  key, because the key never leaves the first chip.

The physics does not say «impossible to hack». It says: hacking
one device yields that one device — and nothing more. The price
of «nothing more» is counted below.

## Wall two — the lease

In Mode A the right lives on the drive; the device holds a signed
lease with a term. The timer lives in the drive's own secure
element — a second chip, outside the device. The device cannot lie
to it about time, because the clock that matters is not the
device's.

Why this matters: the classic trick of a hacked device is to lie
about state — «nothing changed», «this transfer never happened»,
«this is day one of sixty». With the lease, time itself is
witnessed by a chip the hacker does not hold. The drive becomes a
witness the device cannot bribe.

## Wall three — the refusal

The secure element holds the hash of the current firmware. Before
any transfer, the element compares. Altered firmware — the element
goes silent for transfers. The device keeps playing; it stops
being a door.

The design choice matters:

- the device is not bricked — a brick strikes the honest owner and
  teaches the hacker nothing;
- the function is refused, not the thing — the door closes, the
  house stays open;
- the refusal is automatic and silent — there is no dialog to
  argue with, no setting to switch back.

## The economics of a breach

Cryptography is not broken for fun; it is broken for money. So the
question is not «can it be broken» but «what does breaking one
device buy».

- the device's key is born inside its own secure element — a
  breach yields one device's key, not a master key;
- a master key would mean breaking the store's or the platform
  owner's key — kept offline, used for signing, not for the
  everyday run;
- one hacked device can lie only about its own licenses — every
  other device and the register still check everything against
  signatures;
- the cost of the breach — laboratory equipment, months of work,
  one generation of chips — stands against the value of one
  device's licenses. The profit does not close.

This is the same economics that keeps payment cards and modern
consoles honest enough: not that breaking is impossible — that
breaking one does not open all.

## What defense does not promise

- It does not promise the device cannot ever be broken. Physics
  bends slowly; the walls buy time and price, not eternity.
- It does not promise that no one ever plays anything on a hacked
  device. The refusal closes the door through which rights leave;
  it does not patrol the house.
- It does not rely on secrecy. The rules are public; the defense
  rests on keys, physics and economics — not on hiding.

----------------------------------------------------------------------

# Защита

Этот файл отвечает на вопрос, который остальные файлы оставили
открытым: как защищено устройство и какой ценой достаётся взлом.
Обещание живёт в CONCEPT и HOW-IT-WORKS; механика — в MECHANISM.
Здесь — стены.

## Враг — не вор. Враг — лжец.

Вор, укравший флешку, украл один носитель — одну вещь, как крадут
книгу. Враг глубже — другое: устройство, которое уговорили лгать —
сказать, что лицензия стёрта, хотя она осталась; что передачи не
было; что подпись сошлась.

Вся защита копий в истории умирала одинаково: не от сломанной
криптографии — от машины, которую уговорили предать её правила.

Модель отвечает тремя стенами: физикой, арендой, отказом — и
экономикой, которая делает всё это дело невыгодным.

## Стена первая — физика

Защищённый элемент — чип внутри устройства, который держит закрытый
ключ устройства и не отдаёт его. Не «охраняется законом» — не может:
нет команды, которая прочитала бы его наружу, нет провода, который
унёс бы его. Ключ может подписывать изнутри — читать его нельзя.

Что это покупает:

- у подделки нет настоящей подписи — и устройство проверяет подпись,
  прежде чем принять что-либо;
- клон не выдаст себя за оригинал: у него нет ключа, потому что
  ключ не покидает первый чип.

Физика не говорит «взломать невозможно». Она говорит: взлом одного
устройства даёт это одно устройство — и больше ничего. Цена этого
«больше ничего» подсчитана ниже.

## Стена вторая — аренда

В режиме А право живёт на флешке; устройство держит подписанную
аренду со сроком. Таймер живёт в собственном защищённом элементе
флешки — втором чипе, вне устройства. Устройство не может солгать
ему о времени, потому что часы, которые важны, — не в устройстве.

Почему это важно: классический трюк взломанного устройства — лгать
о состоянии — «ничего не менялось», «передачи не было», «сегодня
первый день из шестидесяти». С арендой само время засвидетельствовано
чипом, которого у взломщика нет. Флешка становится свидетелем,
которого устройству не подкупить.

## Стена третья — отказ

Защищённый элемент хранит хеш текущей прошивки. Перед любой
передачей элемент сверяет. Прошивка изменена — элемент умолкает для
передач. Устройство продолжает играть; оно перестаёт быть дверью.

Выбор конструкции важен:

- устройство не превращают в кирпич — кирпич бьёт по честному
  владельцу и не учит взломщика ничему;
- отказана функция, а не вещь — дверь закрыта, дом открыт;
- отказ автоматичен и молчалив — нет диалога, с которым можно
  спорить, нет настройки, которую можно вернуть.

## Экономика взлома

Криптографию ломают не ради забавы — ради денег. Поэтому вопрос не
«можно ли сломать», а «что покупает взлом одного устройства».

- ключ устройства рождается внутри его собственного защищённого
  элемента — взлом даёт ключ одного устройства, а не мастер-ключ;
- мастер-ключ означал бы взлом ключа магазина или владельца
  платформы — а они хранятся офлайн и служат для подписания, а не
  для повседневной работы;
- одно взломанное устройство может лгать только о своих собственных
  лицензиях — все остальные устройства и реестр по-прежнему сверяют
  всё с подписями;
- цена взлома — лабораторное оборудование, месяцы работы, одно
  поколение чипов — против ценности лицензий одного устройства.
  Прибыль не сходится.

Это та же экономика, которая держит банковские карты и современные
приставки достаточно честными: не в том сила, что взломать
невозможно, — в том, что взлом одного не открывает всё.

## Чего защита не обещает

- Она не обещает, что устройство нельзя сломать никогда. Физика
  поддаётся медленно; стены покупают время и цену, а не вечность.
- Она не обещает, что на взломанном устройстве никто никогда ничего
  не сыграет. Отказ закрывает дверь, через которую уходят права;
  обходить дом он не обязан.
- Она не опирается на секретность. Правила публичны; защита стоит
  на ключах, физике и экономике — не на прятках.
