Всё что нужно знать о паролях и защиты личных учётных записей (аккаунтов)

<h2 align="center">🛡 Pass</h2>

- Используйте [мнемонику](https://safe.roskomsvoboda.org/passwords/) или строчки песен для создания паролей (безопасность данного метода под вопросом)
- Используйте [парольные карточки](https://habr.com/ru/articles/534494/)/[матрицы](https://rjfelix.github.io/password-matrix/) или хэш файлов (безопасность под вопросом)
- Используйте шифр виженера для паролей[^14]
- Используйте числа константы или цветовые кода HEX для создания PIN кодов (чтобы нигде не хранить их в явном виде)
- Испоьзуйте математические выражения с константами для создания PIN кодов
- Важные пароли всё же лучше хранить исключительно в голове, чтобы они НИГДЕ не была записаны (пароли высокой степени важности)[^2]
- Использовать знак [нулевой ширины](https://symbl.cc/ru/200B/)[^12]

### <img width=20px src="https://site-iota-coral.vercel.app/censor/bitwarden.png"></img> [Bitwarden](https://bitwarden.com/download/)

✔ В отличии от LastPass Bitwarden не хранит адреса в открытом формате, и не следит за пользователем[^8]
<br>
✔ По состоянию на май 2023 года Bitwarden были пройдены требования SOC 2 Тип 2 и SOC 3, а также тесты от компании Cure53[^7]
<br>
❌ Имеет некоторые проблемы, которые позже исправили[^5]
<br>
❌ Bitwarden использует сторонние уязвимые сервера Microsoft Azure[^6]
<br>
❌ Автозаполнение лучше выключить[^1]

<img width=20px src="https://site-iota-coral.vercel.app/censor/proton.webp"></img>  https://proton.me/pass (❌ *В России не работает без VPN! Синхронизация сломана!*) 
<br> 
<img width=20px src="https://site-iota-coral.vercel.app/censor/keepassxc.png"></img> https://github.com/keepassxreboot/keepassxc
<br>
<img width=20px src="https://raw.githubusercontent.com/Kunzisoft/KeePassDX/master/art/icon.png"></img> https://github.com/Kunzisoft/KeePassDX
<br>
<img width=20px src="https://site-iota-coral.vercel.app/censor/lesspass.png"></img> https://lesspass.com

<h2 align="center">2FA (TOTP / HOTP) </h2> 

Пароли не взламывает только ленивый. Недавняя массовая утечка учетных записей из Yahoo только подтверждает тот факт, что одного лишь пароля — и совершенно неважно, какой он будет длины и сложности, — уже недостаточно для надежной защиты. Двухфакторная аутентификация — это то, что обещает дать такую защиту, добавляя дополнительный уровень безопасности.[^10]

### ❌ Недостатки 2FA SMS
Получение OTP-кодов по СМС или электронной почте - один из самых слабых способов защиты учетных записей с помощью MFA. Получение кода по электронной почте или СМС невилирует принцип "что-то, что у вас есть", поскольку существует множество способов, которыми хакер может завладеть вашим телефонным номером или получить доступ к вашей электронной почте, не имея физического доступа ни к одному из ваших устройств. Если злоумышленник получит доступ к вашей электронной почте, то он сможет использовать этот доступ как для сброса пароля, так и для получения кода аутентификации, что даст ему полный доступ к вашей учетной записи.[^11]

- СМС могут быть перехвачены как на уровне провайдера, так и заменой или клонированием SIM-карты
- Физический доступ к SIM-карте никак не обезопасит от данного рода защиты (единственное решение - установка PIN, который не очень безопасен)
- Возможный перевыпуск SIM-карт и подмена номера телефона злоумышленниками

### ❗ Возможные варианты взлома 2FA TOTP
- Получение ROOT доступа и извлечение секрета из приложения
- Разблокирование загрузчика также позволяет получить данные любых приложений (единственное решение - активировать шифрование в настройках приложения, все представленные ниже приложения позволяют это сделать)
- Разблокировка по местоположению, по фотографии лица и подобные также позволяет получить данные
- Использование TOTP внутри менеджера паролей (что небезопасно и является ложением яиц в одну корзину)

<img width=20px src="https://raw.githubusercontent.com/beemdevelopment/Aegis/master/metadata/en-US/images/icon.png"></img> https://github.com/beemdevelopment/Aegis
<br>
<img width=20px src="https://i.imgur.com/R46JaVd.png"></img> https://play.google.com/store/apps/details?id=com.authenticator.authservice2
<br>
<img width=20px src="https://raw.githubusercontent.com/andOTP/andOTP/master/assets/logo.png"></img> https://github.com/andOTP/andOTP
<br>
<img width=20px src="https://i.imgur.com/z4kcqp9.png"></img> https://totp.danhersam.com/
<br>
<img width=20px src="https://github.com/winauth/winauth/blob/master/WinAuth/Resources/WinAuthIcon.png"></img> https://github.com/winauth/winauth
<br>
https://github.com/tobysmith568/totp-online
<br>
https://totp.app
<br>
https://github.com/anrcry/totp-generator

<h3> <img width=20px src="https://site-iota-coral.vercel.app/censor/authy.png"></img> <a href="https://authy.com">Authy - suck!</a> </h3>

❌ Зависимая эко-система
<br>
❌ Синхронизация и хранение на их серверах не является безопасным
<br>
❌ Регистрация по номеру телефона
<br>
❌ Некоторые сервисы навязывают использовать Authy, вместо других TOTP приложений[^3]
<br>
❌ Настольные приложения для TOTP кодов не являются безопасными, и рушат весь принцип двухфакторной аутентификации[^4]

[^10]: https://xakep.ru/2017/01/17/two-factor-authentication-hacking/
[^11]: https://www.privacyguides.org/ru/basics/multi-factor-authentication/
[^3]: https://www.reddit.com/r/Twitch/comments/9phayo/why_is_twitch_forcing_us_to_use_authy_as_the_2fa/
[^4]: https://securelist.com/how-to-steal-a-million-of-your-data/91855/
[^5]: https://bauinvest.su/opublikovany-rezultaty-audita-bezopasnosti/
[^6]: https://community.bitwarden.com/t/recent-ms-azure-server-vulnerabilities-and-bitwarden-data/49499
[^7]: https://bitwarden.com/help/is-bitwarden-audited/#2023-network-security-assessment
[^8]: https://www.reddit.com/r/Bitwarden/comments/104uuqx/moved_to_bitwarden_if_i_am_not_self_hosting_how/
[^1]: https://startpack.ru/articles/20230310-bitwarden
[^2]: https://book.cyberyozh.com/ru/sozdanie-nadezhnogo-parolya/
[^12]: https://book.cyberyozh.com/ru/sekretyi-nadezhnogo-parolya/
[^14]: https://findhow.org/5076-shifr-vizhenera-onlajn.html
