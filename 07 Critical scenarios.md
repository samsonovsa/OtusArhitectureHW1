# Критические сценарии и критические характеристики

## Критичные функциональные сценарии
- **Процесс бронирования.**
  
  Клиент (гость) должен иметь возможность легко зарегистрироваться в системе, выбрать и забронировать номер.
  Процесс регистрации и бронирования должен обеспечиваться по следующим каналам: 
   - веб
   - мобильный телефон
   - телефон
   - посещение офиса/отеля. 
  
  У гостей должна быть возможность просмотреть и выбрать определенные номера на основе фотографий и местоположения в отеле или выбрать тип номера (стандартный, делюкс, люкс). Критические характеристики включают удобный интерфейс, простой процесс регистрации и выбор комнаты.


- **Обновление статуса номеров в режиме реального времени.**
  
  Статус номеров должны обновляться в режиме реального времени, в том числе на основании информации от устройств с тележек для уборки. Этот сценарий имеет решающее значение для персонала отеля, чтобы эффективно управлять распределением номеров, определять приоритетность задач по уборке и обслуживанию. Также этот сценарий необходим отделу продаж для предоставления точной информации клиентам.

- **Управление ресурсами.**
  
  Система должна иметь расширенные функции управления, позволяющие назначать задачи по уборке и техническому обслуживанию в зависимости от приоритета и потребностей в резервировании. Этот сценарий необходим для оптимизации распределения ресурсов и обеспечения своевременной подготовки номеров для гостей. Критические характеристики включают приоритизацию задач, интеграцию с устройствами на тележках для уборки и отслеживание выполнения задач в реальном времени.

## Нефункциональные характеристики.

- **Интеграция с существующей системой бронирования**
  Интеграция с существующей системой бронирования для использования стандартных функций бронирования, включая обработку платежей и регистрационную информацию является требованием заказчика. Критические характеристики включают согласованность данных между системами, безопасность передачи даннных, надежное хранение данных.

  Сценарий 1: новый клиент зашел на сайт и зарегистрировался. Информация о регистрации передана в существующую систему хранения.

  Сценарий 2: клиент выбрал номер и перешел к оформелнию бронирования. На этапе оплаты используется существующий функционал обработки платежей.

- **Безопасность и защита данных.**
  Система должна обеспечивать защиту информации о гостях, платежных данных и конфиденциальных данных. Чувствительная информация должна храниться в зашифрованном виде, платежные и конфиденциальные данные должны передаваться между системами по безопасному каналу связи. Необходимы современные безопасные механизмы аутентификации и авторизации.

  Сценарий 1: без регистрации клиент может посмотреть фотографии номеров, информацию о наличии свободных номерах, но не может забронировать номер.

  Сценарий 2: клиен пытается восстановить забытый пароль и выполняет несколько попыток. После 5 неудачных попыток, система выводит предупреждение и выполняет задержку на повторение аутентификации.

  Сценарий 3: злоумышленник получил доступ к БД. Конфиденциальная и чувствительная информация зашифрована, пароли хранятся в виде хешей.

- **Круглосуточная доступность и надежность**
  Система должна быть доступна и надежна в любое время. Гости должны иметь доступ к системе и бронировать номера в любое время, а персонал отеля должен полагаться на точную и актуальную информацию.

  Сценарий 1: Технический сбой сервиса приложения или БД. Трафик автоматически переключается на резервные сервисы.

  Сценарий 2: Время доступа и время выполнения основных функций системы увеличилось. На основании существующих систем мониторинга и логгирования ошибок информация своевременно, до жалоб клиентов, поступает в службу технической поддержки. Поддержка оперативно устраняет проблемы.

- Масштабируемость и производительность.
  Система должна обрабатывать несколько сотен одновременных подключений пользователей. Надо учитываеть периоды пиковой нагрузки. Система должна обеспечивать быстрое время отклика и эффективно масштабироваться, чтобы соответствовать возросшим требованиям без ущерба для производительности. 
  
  Сценарий 1: В разгар летнего сезона резко увеличилось колличество одновременных подключений. При превышении порога TTFB в 200 мс, разворачивается дополнительный микросервис, обслуживающий взаимодействие с клиентами.

- Скорость разработки (time to maret). 
  Разработка системы должна осуществляться с высокой скоростью, чтобы успеть выпустить продукт до предстоящего пикового сезона.