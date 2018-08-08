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
ms.openlocfilehash: e68211049bc0f958ae24975f4ab4063953eef567
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808841"
---
# <a name="imapiclientshutdown--iunknown"></a>IMAPIClientShutdown : IUnknown

  
  
**Относится к**: Outlook 
  
Включение клиент MAPI выполнить быстрое завершение работы процесса клиента. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapidefs.h  <br/> |
|Предоставляемые:  <br/> |Объект [IMAPISession](imapisessioniunknown.md)  <br/> |
|Реализованный:  <br/> |Подсистема MAPI  <br/> |
|Вызывается:  <br/> |Клиент MAPI  <br/> |
|Идентификатор интерфейса:  <br/> |IID_IMAPIClientShutdown  <br/> |
|Тип указателя:  <br/> |LPMAPICLIENTSHUTDOWN  <br/> |
   
## <a name="vtable-order"></a>Порядке vtable

|||
|:-----|:-----|
|[QueryFastShutdown](imapiclientshutdown-queryfastshutdown.md) <br/> |Запросы в подсистеме MAPI для быстрое завершение работы поддерживают, предоставленные загруженных поставщики MAPI.  <br/> |
|[NotifyProcessShutdown](imapiclientshutdown-notifyprocessshutdown.md) <br/> |Показывает завершена намерения клиент MAPI для продолжения.  <br/> |
|[DoFastShutdown](imapiclientshutdown-dofastshutdown.md) <br/> |Указывает намерения клиент MAPI, чтобы выйти из клиентского процесса немедленно.  <br/> |
   
## <a name="remarks"></a>Замечания

Быстрое завершение работы это позволяет клиент MAPI и любые загруженных поставщика MAPI, с которым клиент MAPI имеет активного сеанса MAPI для сохранения параметров MAPI и данных. Это позволяет клиент MAPI для отключения всех внешних ссылок и выйдите из без причиной потери данных. Клиент MAPI, которую необходимо выполнить быстрое завершение работы необходимо использовать интерфейс **IMAPIClientShutdown** . Клиент MAPI можно получить путем вызова метода IUnknown::QueryInterface для любого объекта [IMAPISession](imapisessioniunknown.md) указатель на этот интерфейс. 
  
Клиент MAPI всегда инициирует быстрое завершение работы путем вызова метода **IMAPIClientShutdown::QueryFastShutdown** . Подсистема MAPI отвечает на запрос клиент MAPI, проверяя, поддерживает ли загруженных поставщики MAPI быстрое завершение работы клиента. Администратор может использовать параметры реестра Windows для определения уровень поддержки поставщика, которая требуется для клиентов MAPI продолжить работу быстрое завершение работы. Для получения дополнительных сведений см [Fast параметры завершения работы пользователя](fast-shutdown-user-options.md).
  
Для продолжения быстрое завершение работы клиента вызывает метод **IMAPIClientShutdown::NotifyProcessShutdown** для указания подсистемы MAPI намерения завершить работу. Клиент затем вызывает метод **IMAPIClientShutdown::DoFastShutdown** для указания, что процесс клиента завершает работу сразу же. 
  
Дополнительные сведения о быстрое завершение работы см [быстрое завершение работы](fast-shutdown-overview.md). Сведения о том, как успешно выполнить быстрое завершение работы, [рекомендации](best-practices-for-fast-shutdown.md)по быстрое завершение работы.
  
## <a name="see-also"></a>См. также



[Интерфейсы MAPI](mapi-interfaces.md)
  
[Завершение работы клиента в MAPI](client-shutdown-in-mapi.md)

