# Keenetic Game Data

## Русский

Подписанные данные для локального кандидата Keenetic. Ветка `games-data` содержит только публичный ключ, manifest, подпись и список адресов. Начальный sequence 1 намеренно пуст: реальные игровые адреса ещё не прошли проверку. Это проверка канала доставки, а не обещание поддержки всех игр.

Клиент должен использовать заранее закреплённый публичный ключ из установочного комплекта. Нельзя доверять ключу, просто скачанному вместе с данными. Проверяются Ed25519, точные байты manifest, SHA256, срок действия и возрастающий sequence. При ошибке сохраняется рабочий локальный список. Бинарники, домашняя конфигурация и приватный ключ здесь не публикуются.

Автоматическая доставка ещё не включена в кандидат. Срок действия bootstrap указан в manifest; истёкшие данные не принимаются. Обновления пока подписываются локально после проверки источников адресов.

## English

Signed data for the local Keenetic candidate. The `games-data` branch contains a public key, manifest, detached signature and one address list. Initial sequence 1 is deliberately empty: no real game addresses have been reviewed. This bootstraps the delivery channel, not comprehensive game coverage.

Clients must pin the public key from their installation kit, never trust a key downloaded alongside a feed. Verify Ed25519, exact manifest bytes, payload SHA256, validity and increasing sequence. Failures preserve the local cache. No binaries, home-network configuration or private keys are published.

Automatic delivery is not enabled in the candidate yet. Bootstrap validity is in the manifest; expired artifacts must be rejected. Updates are signed locally after source review.
