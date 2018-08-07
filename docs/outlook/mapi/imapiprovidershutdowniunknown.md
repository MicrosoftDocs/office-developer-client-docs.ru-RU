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
ms.openlocfilehash: a679d04f7697abbe0172105febf87082c0cd9946
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809081"
---
# <a name="imapiprovidershutdown--iunknown"></a>IMAPIProviderShutdown : IUnknown

  
  
**Относится к**: Outlook 
  
Разрешает подсистемы MAPI для оповещения Поставщик MAPI быстрое завершение работы клиент MAPI, чтобы поставщик MAPI могут отвечать на завершение работы.
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapidefs.h  <br/> |
|Предоставляемые:  <br/> |Объекты поставщика: [IXPProvider](ixpprovideriunknown.md), [IABProvider](iabprovideriunknown.md)или [IMSProvider](imsprovideriunknown.md) <br/> |
|Реализованный:  <br/> |Поставщик MAPI  <br/> |
|Вызывается:  <br/> |Подсистема MAPI  <br/> |
|Идентификатор интерфейса:  <br/> |IID_IMAPIProviderShutdown  <br/> |
|Тип указателя:  <br/> |LPMAPIPROVIDERSHUTDOWN  <br/> |
   
## <a name="vtable-order"></a>Порядке vtable

|||
|:-----|:-----|
|[QueryFastShutdown](imapiprovidershutdown-queryfastshutdown.md) <br/> |Запросы, которые поддерживают поставщика MAPI для быстрое завершение работы.  <br/> |
|[NotifyProcessShutdown](imapiprovidershutdown-notifyprocessshutdown.md) <br/> |Указывает поставщика MAPI, что клиент MAPI требуется выполнить быстрое завершение работы, чтобы поставщик можно выполнять действия, чтобы предотвратить потерю данных.  <br/> |
|[DoFastShutdown](imapiprovidershutdown-dofastshutdown.md) <br/> |Указывает поставщика MAPI немедленно, выходе клиент MAPI, чтобы поставщик MAPI будут сохранены и отобразятся изменения, чтобы предотвратить потерю данных.  <br/> |
   
## <a name="remarks"></a>Замечания

Быстрое завершение работы позволяет клиент MAPI выйти из своего процесса в течение короткого времени, как кажется после клиента и загруженных поставщики MAPI сохранения параметров MAPI и данных. Клиент MAPI всегда инициирует быстрое завершение работы и необходимо запросить подсистемы MAPI для поддержки быстрое завершение работы из загруженных поставщики MAPI. Администратор может установить реестра Windows на уровне пользователя, чтобы указать уровень поддержки поставщика, который необходимо разрешить быстрое завершение работы всех клиентов MAPI. Дополнительные сведения о параметрах реестра видеть [Fast параметры завершения работы пользователя](fast-shutdown-user-options.md). Тем не менее быстрое завершение работы будет успешно выполнена без потери данных поставщики MAPI следует реализовать интерфейс **IMAPIProviderShutdown** . 
  
Поставщик MAPI, должна поддерживать быстрое завершение работы клиента должен возвращать значение S_OK в подсистему MAPI в методе **IMAPIProviderShutdown::QueryFastShutdown** . При последующем подсистемы MAPI вызывает методы **IMAPIProviderShutdown::NotifyProcessShutdown** и **IMAPIProviderShutdown::DoFastShutdown** , поставщика MAPI должен выполнять действия, необходимые для сохранения параметров MAPI и данных и Подготовка к выхода клиента. 
  
Поставщики MAPI, которые не должны поддерживать быстрое завершение работы клиента следует по-прежнему реализовать интерфейс **IMAPIProviderShutdown** и метод **IMAPIProviderShutdown::QueryFastShutdown** возвращает MAPI_E_NO_SUPPORT. Для Outlook как клиент MAPI в результате Outlook вынуждены ждать освобождения всех внешних ссылок освободить до его завершения. 
  
В зависимости от реестра Windows пользователя политика для быстрое завершение работы не реализация интерфейса **IMAPIProviderShutdown** не обязательно быстрое завершение работы клиента. 
  
Дополнительные сведения о процессе быстрое завершение работы см [быстрое завершение работы](fast-shutdown-overview.md). Сведения о том, как успешно выполнить быстрое завершение работы, [рекомендации](best-practices-for-fast-shutdown.md)по быстрое завершение работы.
  
## <a name="see-also"></a>См. также



[Интерфейсы MAPI](mapi-interfaces.md)
  
[Завершение работы клиента в MAPI](client-shutdown-in-mapi.md)

