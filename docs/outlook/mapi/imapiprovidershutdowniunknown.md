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
  
Позволяет подсистеме MAPI сообщать поставщику MAPI быстрое завершение работы клиента MAPI, чтобы поставщик MAPI мог ответить на завершение работы.
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |MAPIDEFS. h  <br/> |
|Предоставлено:  <br/> |Объекты поставщика: [иксппровидер](ixpprovideriunknown.md), [иабпровидер](iabprovideriunknown.md)или [функцииimsprovider](imsprovideriunknown.md) <br/> |
|Реализовано в:  <br/> |Поставщик MAPI  <br/> |
|Вызывающая сторона:  <br/> |Подсистема MAPI  <br/> |
|Идентификатор интерфейса:  <br/> |IID_IMAPIProviderShutdown  <br/> |
|Тип указателя:  <br/> |лпмапипровидершутдовн  <br/> |
   
## <a name="vtable-order"></a>Заказ vtable

|||
|:-----|:-----|
|[QueryFastShutdown](imapiprovidershutdown-queryfastshutdown.md) <br/> |Запрашивает у поставщика MAPI поддержку быстрого завершения работы.  <br/> |
|[нотифипроцессшутдовн](imapiprovidershutdown-notifyprocessshutdown.md) <br/> |Указывает поставщику MAPI, что клиент MAPI планирует выполнить быстрое завершение работы, чтобы поставщик мог выполнять действия для предотвращения потери данных.  <br/> |
|[дофастшутдовн](imapiprovidershutdown-dofastshutdown.md) <br/> |Указывает поставщику MAPI, что клиент MAPI немедленно завершает работу, поэтому поставщик MAPI сохранит изменения, чтобы предотвратить потерю данных.  <br/> |
   
## <a name="remarks"></a>Примечания

Быстрое завершение работы позволяет клиенту MAPI выйти из процесса в течение короткого периода времени, надеюсь, после сохранения параметров и данных MAPI у клиента и загруженных поставщиков MAPI. Клиент MAPI всегда инициирует быстрое завершение работы и запрашивает подсистему MAPI для поддержки быстрого завершения работы от загруженных поставщиков MAPI. Администратор может настроить реестр Windows на уровне пользователя, чтобы указать уровень поддержки поставщика, который необходим для быстрого завершения работы всех клиентов MAPI. Дополнительные сведения о параметрах реестра приведены в разделе [Параметры быстрого завершения работы пользователя](fast-shutdown-user-options.md). Однако для успешного завершения работы без потери данных поставщики MAPI должны реализовать интерфейс **IMAPIProviderShutdown** . 
  
Поставщик MAPI, который должен поддерживать быстрое завершение работы клиента, должен возвратить S_OK подсистеме MAPI в методе **IMAPIProviderShutdown:: QueryFastShutdown** . Когда подсистема MAPI последовательно вызывает методы **IMAPIProviderShutdown:: нотифипроцессшутдовн** и **IMAPIProviderShutdown::D ОФАСТШУТДОВН** , поставщик MAPI должен выполнить необходимые действия для сохранения параметров и данных MAPI и подготовки к выходу клиента. 
  
Поставщики MAPI, которые не нуждаются в поддержке быстрого завершения работы клиента, по-прежнему должны реализовывать интерфейс **IMAPIProviderShutdown** и иметь метод **IMAPIProviderShutdown:: QueryFastShutdown** , возвращающий MAPI_E_NO_SUPPORT. Для Outlook в качестве клиента MAPI это приводит к тому, что Outlook ждет, пока все внешние ссылки будут сняты до завершения работы. 
  
В зависимости от параметра реестра Windows для быстрого завершения работы, отсутствие реализации интерфейса **IMAPIProviderShutdown** не обязательно препятствует быстрому завершению работы клиента. 
  
Дополнительные сведения о процессе быстрого завершения работы приведены в разделе [Обзор быстрого завершения работы](fast-shutdown-overview.md). Сведения о том, как успешно выполнить быстрое завершение работы, приведены в разделе рекомендации [по быстрому завершению работы](best-practices-for-fast-shutdown.md).
  
## <a name="see-also"></a>См. также



[Интерфейсы MAPI](mapi-interfaces.md)
  
[Завершение работы клиента в MAPI](client-shutdown-in-mapi.md)

