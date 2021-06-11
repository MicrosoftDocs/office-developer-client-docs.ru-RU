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

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Позволяет подсистеме MAPI информировать поставщика MAPI о быстром закрытии клиента MAPI, чтобы поставщик MAPI отвечал на отключение.
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapidefs.h  <br/> |
|Подвергается:  <br/> |Объекты поставщика: [IXPProvider,](ixpprovideriunknown.md) [IABProvider](iabprovideriunknown.md)или [IMSProvider](imsprovideriunknown.md) <br/> |
|Реализовано в:  <br/> |Поставщик MAPI  <br/> |
|Вызывающая сторона:  <br/> |Подсистема MAPI  <br/> |
|Идентификатор интерфейса:  <br/> |IID_IMAPIProviderShutdown  <br/> |
|Тип указателя:  <br/> |LPMAPIPROVIDERSHUTDOWN  <br/> |
   
## <a name="vtable-order"></a>Заказ Vtable

|||
|:-----|:-----|
|[QueryFastShutdown](imapiprovidershutdown-queryfastshutdown.md) <br/> |Запрашивает поставщика MAPI для поддержки быстрого отключения.  <br/> |
|[NotifyProcessShutdown](imapiprovidershutdown-notifyprocessshutdown.md) <br/> |Указывает поставщику MAPI, что клиент MAPI собирается сделать быстрое отключение, чтобы поставщик может принять меры для предотвращения потери данных.  <br/> |
|[DoFastShutdown](imapiprovidershutdown-dofastshutdown.md) <br/> |Указывает поставщику MAPI, что клиент MAPI немедленно выходит, чтобы поставщик MAPI сохранял изменения, чтобы предотвратить потерю данных.  <br/> |
   
## <a name="remarks"></a>Примечания

Быстрое отключение позволяет клиенту MAPI выйти из процесса в течение короткого времени, надеюсь, после того, как клиент и загруженные поставщики MAPI сохранили параметры и данные MAPI. Клиент MAPI всегда инициирует быстрое отключение и должен запрашивать подсистему MAPI для быстрой поддержки отключения от загруженных поставщиков MAPI. Администратор может задать реестр Windows на уровне пользователя, чтобы указать уровень поддержки поставщика, необходимой для быстрого отключения всех клиентов MAPI. Дополнительные сведения о параметрах реестра см. в меню [Fast Shutdown User Options.](fast-shutdown-user-options.md) Однако, чтобы быстрое отключение успешно произошло без потери данных, поставщики MAPI должны реализовать **интерфейс IMAPIProviderShutdown.** 
  
Поставщик MAPI, который должен поддерживать быстрое отключение клиента, должен возвращать S_OK в подсистему MAPI в **методе IMAPIProviderShutdown::QueryFastShutdown.** Если подсистема MAPI впоследствии вызывает методы **IMAPIProviderShutdown::NotifyProcessShutdown** и **IMAPIProviderShutdown::D FastShutdown,** поставщик MAPI должен принять необходимые меры для сохранения параметров MAPI и данных и подготовки к выходу клиента. 
  
Поставщики MAPI, которые не нуждаются в поддержке быстрого отключения клиента, по-прежнему должны реализовать интерфейс **IMAPIProviderShutdown** и иметь метод **IMAPIProviderShutdown::QueryFastShutdown** MAPI_E_NO_SUPPORT. Для Outlook клиента MAPI это Outlook ожидание выпуска всех внешних ссылок до его выхода. 
  
В зависимости от параметра Windows реестра для быстрого отключения, не реализация интерфейса **IMAPIProviderShutdown** не обязательно препятствует быстрому отключению клиента. 
  
Дополнительные сведения о процессе быстрого отключения см. в [обзоре быстрого отключения.](fast-shutdown-overview.md) Сведения о том, как успешно выполнять быстрое отключение, см. в см. в руб. "Лучшие практики [для быстрого отключения".](best-practices-for-fast-shutdown.md)
  
## <a name="see-also"></a>См. также



[Интерфейсы MAPI](mapi-interfaces.md)
  
[Завершение работы клиента в MAPI](client-shutdown-in-mapi.md)

