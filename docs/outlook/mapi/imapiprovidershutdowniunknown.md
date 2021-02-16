---
title: IMAPIProviderShutdown IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIProviderShutdown
api_type:
- COM
ms.assetid: fd86c8a5-f251-46c3-ace9-515e94e504ac
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 92067b5badfb2aab40f3b3735a164bc09321702c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409659"
---
# <a name="imapiprovidershutdown--iunknown"></a>IMAPIProviderShutdown : IUnknown

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Позволяет подсистеме MAPI сообщить поставщику MAPI о быстром закрытии клиента MAPI, чтобы поставщик MAPI ответил на завершение работы.
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapidefs.h  <br/> |
|Выставим:  <br/> |Объекты поставщика: [IXPProvider,](ixpprovideriunknown.md) [IABProvider](iabprovideriunknown.md)или [IMSProvider](imsprovideriunknown.md) <br/> |
|Реализовано в:  <br/> |Поставщик MAPI  <br/> |
|Вызывающая сторона:  <br/> |Подсистема MAPI  <br/> |
|Идентификатор интерфейса:  <br/> |IID_IMAPIProviderShutdown  <br/> |
|Тип указателя:  <br/> |LPMAPIPROVIDERSHUTDOWN  <br/> |
   
## <a name="vtable-order"></a>Порядок ветвей

|||
|:-----|:-----|
|[QueryFastShutdown](imapiprovidershutdown-queryfastshutdown.md) <br/> |Запрашивает у поставщика MAPI поддержку быстрого завершения работы.  <br/> |
|[NotifyProcessShutdown](imapiprovidershutdown-notifyprocessshutdown.md) <br/> |Указывает поставщику MAPI, что клиент MAPI собирается быстро закрыть работу, чтобы поставщик может принять меры для предотвращения потери данных.  <br/> |
|[DoFastShutdown](imapiprovidershutdown-dofastshutdown.md) <br/> |Указывает поставщику MAPI, что клиент MAPI немедленно выходит, чтобы поставщик MAPI сохранял изменения, чтобы предотвратить потерю данных.  <br/> |
   
## <a name="remarks"></a>Примечания

Быстрое завершение работы позволяет клиенту MAPI выйти из процесса в течение короткого времени, надеемся, после того как клиент и загруженные поставщики MAPI сэкономят параметры и данные MAPI. Клиент MAPI всегда инициирует быстрое завершение работы и должен запрашивать поддержку быстрого завершения работы подсистемы MAPI от загруженных поставщиков MAPI. Администратор может задать реестр Windows на уровне пользователя, чтобы указать уровень поддержки поставщика, необходимый для быстрого завершения работы всех клиентов MAPI. Дополнительные сведения о параметрах реестра см. в параметрах пользователей быстрого [завершения работы.](fast-shutdown-user-options.md) Однако для успешного завершения работы без потери данных поставщики MAPI должны реализовать интерфейс **IMAPIProviderShutdown.** 
  
Поставщик MAPI, который должен поддерживать быстрое завершение работы клиента, должен возвращать S_OK подсистеме MAPI в **методе IMAPIProviderShutdown::QueryFastShutdown.** Когда подсистема MAPI впоследствии вызывает методы **IMAPIProviderShutdown::NotifyProcessShutdown** и **IMAPIProviderShutdown::D oFastShutdown,** поставщик MAPI должен принять необходимые действия для сохранения параметров и данных MAPI и подготовки к выходу клиента. 
  
Поставщики MAPI, которые не нуждаются в поддержке быстрого завершения работы клиента, по-прежнему должны реализовать интерфейс **IMAPIProviderShutdown,** а метод **IMAPIProviderShutdown::QueryFastShutdown** должен возвращать MAPI_E_NO_SUPPORT. Для Outlook в качестве клиента MAPI это приводит к ожиданию выпуска всех внешних ссылок перед выходом из outlook. 
  
В зависимости от параметра реестра Windows пользователя для быстрого завершения работы не реализация интерфейса **IMAPIProviderShutdown** не обязательно препятствует быстрому отключению клиента. 
  
Дополнительные сведения о процессе быстрого завершения работы см. в обзоре [быстрого завершения работы.](fast-shutdown-overview.md) Сведения о том, как успешно выполнить быстрое завершение работы, см. в лучших [методиках быстрого завершения работы.](best-practices-for-fast-shutdown.md)
  
## <a name="see-also"></a>См. также



[Интерфейсы MAPI](mapi-interfaces.md)
  
[Завершение работы клиента в MAPI](client-shutdown-in-mapi.md)

