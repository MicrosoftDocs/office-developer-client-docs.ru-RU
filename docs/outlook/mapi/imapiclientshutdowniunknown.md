---
title: IMAPIClientShutdown IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIClientShutdown
api_type:
- COM
ms.assetid: b6a5096f-ad27-48b3-b569-f33efc20fa72
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 279d6109e8c29de204c4fb58da51de84b4fbe183
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435336"
---
# <a name="imapiclientshutdown--iunknown"></a>IMAPIClientShutdown : IUnknown

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Позволяет клиенту MAPI выполнять быстрое завершение клиентского процесса. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapidefs.h  <br/> |
|Подвергается:  <br/> |[Объект IMAPISession](imapisessioniunknown.md)  <br/> |
|Реализовано в:  <br/> |Подсистема MAPI  <br/> |
|Вызывающая сторона:  <br/> |Клиент MAPI  <br/> |
|Идентификатор интерфейса:  <br/> |IID_IMAPIClientShutdown  <br/> |
|Тип указателя:  <br/> |LPMAPICLIENTSHUTDOWN  <br/> |
   
## <a name="vtable-order"></a>Заказ Vtable

|||
|:-----|:-----|
|[QueryFastShutdown](imapiclientshutdown-queryfastshutdown.md) <br/> |Запрашивает подсистему MAPI для поддержки быстрого отключения, предоставляемую загруженными поставщиками MAPI.  <br/> |
|[NotifyProcessShutdown](imapiclientshutdown-notifyprocessshutdown.md) <br/> |Указывает намерение клиента MAPI приступить к закрытию.  <br/> |
|[DoFastShutdown](imapiclientshutdown-dofastshutdown.md) <br/> |Указывает намерение клиента MAPI немедленно выйти из клиентского процесса.  <br/> |
   
## <a name="remarks"></a>Примечания

Целью быстрого отключения является разрешение клиенту MAPI и любому загруженного поставщика MAPI, с которым клиент MAPI имеет активный сеанс MAPI для сохранения параметров и данных MAPI. Это позволяет клиенту MAPI отключить все внешние ссылки и выйти, не вызывая потери данных. Клиент MAPI, который должен выполнить быстрое отключение, должен использовать **интерфейс IMAPIClientShutdown.** Клиент MAPI может получить указатель на этот интерфейс, позвонив методу IUnknown::QueryInterface на любом [объекте IMAPISession.](imapisessioniunknown.md) 
  
Клиент MAPI всегда инициирует быстрое отключение, вызывая **метод IMAPIClientShutdown::QueryFastShutdown.** Подсистема MAPI отвечает на запрос клиента MAPI, проверяя, поддерживают ли загруженные поставщики MAPI быструю остановку клиента. Администратор может использовать Windows реестра, чтобы определить уровень поддержки поставщика, необходимой клиентам MAPI для быстрого отключения. Дополнительные сведения см. в [меню Fast Shutdown User Options.](fast-shutdown-user-options.md)
  
Чтобы перейти к быстрому отключению, клиент вызывает **метод IMAPIClientShutdown::NotifyProcessShutdown,** чтобы указать подсистеме MAPI намерение закрыться. Затем клиент вызывает **метод IMAPIClientShutdown::D FastShutdown,** чтобы указать, что клиентский процесс немедленно выходит. 
  
Дополнительные сведения о быстром закрытии см. в [обзоре быстрого отключения.](fast-shutdown-overview.md) Сведения о том, как успешно выполнить быстрое отключение, см. в см. в руб. "Лучшие практики [для быстрого отключения".](best-practices-for-fast-shutdown.md)
  
## <a name="see-also"></a>См. также



[Интерфейсы MAPI](mapi-interfaces.md)
  
[Завершение работы клиента в MAPI](client-shutdown-in-mapi.md)

