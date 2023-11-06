Всё что нужно знать о паролях и защиты личных учётных записей (аккаунтов)

<h2 align="center">🛡 Pass</h2>

<img width=20px src="https://site-iota-coral.vercel.app/censor/bitwarden.png"></img> https://bitwarden.com
<br>
<img width=20px src="https://site-iota-coral.vercel.app/censor/proton.webp"></img>  https://proton.me/pass (❌ *В России не работает без VPN! Синхронизация сломана!*) 
<br> 
<img width=20px src="https://site-iota-coral.vercel.app/censor/keepassxc.png"></img> https://github.com/keepassxreboot/keepassxc
<br>
<img width=20px src="https://raw.githubusercontent.com/Kunzisoft/KeePassDX/master/art/icon.png"></img> https://github.com/Kunzisoft/KeePassDX
<br>
<img width=20px src="https://site-iota-coral.vercel.app/censor/lesspass.png"></img> https://lesspass.com

<h2 align="center">2FA (TOTP / HOTP) </h2> 

Пароли не взламывает только ленивый. Недавняя массовая утечка учетных записей из Yahoo только подтверждает тот факт, что одного лишь пароля — и совершенно неважно, какой он будет длины и сложности, — уже недостаточно для надежной защиты. Двухфакторная аутентификация — это то, что обещает дать такую защиту, добавляя дополнительный уровень безопасности.[^1]

[^1]: https://xakep.ru/2017/01/17/two-factor-authentication-hacking/

### ❌ Недостатки 2FA SMS
Получение OTP-кодов по СМС или электронной почте - один из самых слабых способов защиты учетных записей с помощью MFA. Получение кода по электронной почте или СМС невилирует принцип "что-то, что у вас есть", поскольку существует множество способов, которыми хакер может завладеть вашим телефонным номером или получить доступ к вашей электронной почте, не имея физического доступа ни к одному из ваших устройств. Если злоумышленник получит доступ к вашей электронной почте, то он сможет использовать этот доступ как для сброса пароля, так и для получения кода аутентификации, что даст ему полный доступ к вашей учетной записи.[^2]

[^2]: https://www.privacyguides.org/ru/basics/multi-factor-authentication/

- СМС могут быть перехвачены как на уровне провайдера, так и заменой или клонированием SIM-карты
- Физический доступ к SIM-карте никак не обезопасит от данного рода защиты (единственное решение - установка PIN, который не очень безопасен)
- Возможный перевыпуск SIM-карт и подмена номера телефона злоумышленниками

### ❗ Возможные варианты взлома 2FA TOTP
- Получение ROOT доступа и извлечение секрета из приложения
- Разблокирование загрузчика также позволяет получить данные любых приложений (единственное решение - активировать шифрование в настройках приложения, все представленные ниже приложения позволяют это сделать)
- Разблокировка по местоположению, по фотографии лица и подобные также позволяет получить данные

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

<h3> <img width=20px src="https://site-iota-coral.vercel.app/censor/authy.png"></img> <a href="https://authy.com">Authy</a> </h3>

❌ Зависимая эко-система
<br>
❌ Синхронизация и хранение на их серверах не является безопасным
<br>
❌ Регистрация по номеру телефона
<br>
❌ Некоторые сервисы навязывают использовать Authy, вместо других TOTP приложений[^3]

[^3]: https://www.reddit.com/r/Twitch/comments/9phayo/why_is_twitch_forcing_us_to_use_authy_as_the_2fa/
