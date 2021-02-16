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

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Позволяет клиенту MAPI выполнять быстрое завершение клиентского процесса. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapidefs.h  <br/> |
|Выставим:  <br/> |[Объект IMAPISession](imapisessioniunknown.md)  <br/> |
|Реализовано в:  <br/> |Подсистема MAPI  <br/> |
|Вызывающая сторона:  <br/> |Клиент MAPI  <br/> |
|Идентификатор интерфейса:  <br/> |IID_IMAPIClientShutdown  <br/> |
|Тип указателя:  <br/> |LPMAPICLIENTSHUTDOWN  <br/> |
   
## <a name="vtable-order"></a>Порядок ветвей

|||
|:-----|:-----|
|[QueryFastShutdown](imapiclientshutdown-queryfastshutdown.md) <br/> |Запрашивает поддержку быстрого завершения работы подсистемы MAPI, предоставляемую загруженными поставщиками MAPI.  <br/> |
|[NotifyProcessShutdown](imapiclientshutdown-notifyprocessshutdown.md) <br/> |Указывает на намерение клиента MAPI продолжить завершение работы.  <br/> |
|[DoFastShutdown](imapiclientshutdown-dofastshutdown.md) <br/> |Указывает на намерение клиента MAPI немедленно выйти из клиентского процесса.  <br/> |
   
## <a name="remarks"></a>Примечания

Быстрое завершение работы позволяет клиенту MAPI и любому загруженном поставщику MAPI, с которым у клиента MAPI есть активный сеанс MAPI, для сохранения параметров и данных MAPI. Это позволяет клиенту MAPI отключать все внешние ссылки и выходить из нее без потери данных. Клиент MAPI, который должен выполнять быстрое завершение работы, должен использовать интерфейс **IMAPIClientShutdown.** Клиент MAPI может получить указатель на этот интерфейс, вызывая метод IUnknown::QueryInterface для любого объекта [IMAPISession.](imapisessioniunknown.md) 
  
Клиент MAPI всегда инициирует быстрое завершение работы, вызывая метод **IMAPIClientShutdown::QueryFastShutdown.** Подсистема MAPI отвечает на запрос клиента MAPI, проверяя, поддерживают ли загруженные поставщики MAPI быстрое завершение работы клиента. Администратор может использовать параметры реестра Windows, чтобы определить уровень поддержки поставщика, необходимый клиентам MAPI для быстрого завершения работы. Дополнительные сведения см. в параметрах пользователей быстрого [завершения работы.](fast-shutdown-user-options.md)
  
Чтобы продолжить быстрое завершение работы, клиент вызывает метод **IMAPIClientShutdown::NotifyProcessShutdown,** чтобы указать подсистеме MAPI намерение закрыть работу. Затем клиент вызывает метод **IMAPIClientShutdown::D oFastShutdown,** чтобы указать, что клиентский процесс немедленно выходит из процесса. 
  
Дополнительные сведения о быстром отключении см. в [обзоре быстрого завершения работы.](fast-shutdown-overview.md) Сведения о том, как успешно выполнить быстрое завершение работы, см. в ["Best Practices for Fast Shutdown".](best-practices-for-fast-shutdown.md)
  
## <a name="see-also"></a>См. также



[Интерфейсы MAPI](mapi-interfaces.md)
  
[Завершение работы клиента в MAPI](client-shutdown-in-mapi.md)

