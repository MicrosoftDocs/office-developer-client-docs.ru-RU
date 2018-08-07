---
title: IMsgServiceAdmin IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgServiceAdmin
api_type:
- COM
ms.assetid: 5905b9e9-c462-451d-a49f-1f3a8aa506a6
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 21889bf626d7f9128d1e01b3e6a15b5fa0d2e696
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809397"
---
# <a name="imsgserviceadmin--iunknown"></a>IMsgServiceAdmin : IUnknown

  
  
**Относится к**: Outlook 
  
Вносятся изменения в службы сообщений в профиле.
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |MapiX.h  <br/> |
|Предоставляемые:  <br/> |Объекты администрирования службы сообщений  <br/> |
|Реализованный:  <br/> |MAPI  <br/> |
|Вызывается:  <br/> |Клиентские приложения  <br/> |
|Идентификатор интерфейса:  <br/> |IID_IMsgServiceAdmin  <br/> |
|Тип указателя:  <br/> |LPSERVICEADMIN  <br/> |
   
## <a name="vtable-order"></a>Порядке vtable

|||
|:-----|:-----|
|[GetLastError](imsgserviceadmin-getlasterror.md) <br/> |Возвращает структуру [MAPIERROR](mapierror.md) , который содержит сведения о последнюю ошибку, сгенерированную объектом администрирования службы сообщений.  <br/> |
|[GetMsgServiceTable](imsgserviceadmin-getmsgservicetable.md) <br/> |Предоставляет доступ к таблице службы сообщений, список служб сообщения в профиле.  <br/> |
|[CreateMsgService](imsgserviceadmin-createmsgservice.md) <br/> |Добавление службы сообщений для текущего профиля.  <br/> <br/>**Примечание**: этот метод является устаревшим. Вместо этого используйте [IMsgServiceAdmin2::CreateMsgServiceEx](imsgserviceadmin2-createmsgserviceex.md) .           |
|[DeleteMsgService](imsgserviceadmin-deletemsgservice.md) <br/> |Удаление службы сообщений из профиля.  <br/> |
|[CopyMsgService](imsgserviceadmin-copymsgservice.md) <br/> |Копирует службы сообщений в профиль.  <br/> |
|[RenameMsgService](imsgserviceadmin-renamemsgservice.md) <br/> |Рекомендуется использовать. Назначает новое имя службы сообщений.  <br/> |
|[ConfigureMsgService](imsgserviceadmin-configuremsgservice.md) <br/> |Устанавливает службы сообщений.  <br/> |
|[OpenProfileSection](imsgserviceadmin-openprofilesection.md) <br/> |Откроется раздел текущего профиля и возвращает указатель [IProfSect](iprofsectimapiprop.md) для дальнейшей доступа.  <br/> |
|[MsgServiceTransportOrder](imsgserviceadmin-msgservicetransportorder.md) <br/> |Задает порядок вызова поставщиков какие транспорта доставить сообщение.  <br/> |
|[AdminProviders](imsgserviceadmin-adminproviders.md) <br/> |Возвращает указатель, который предоставляет доступ к объекту администрирования поставщика.  <br/> |
|[SetPrimaryIdentity](imsgserviceadmin-setprimaryidentity.md) <br/> |Назначает службы сообщений быть поставщика основной идентификатор профиля.  <br/> |
|[GetProviderTable](imsgserviceadmin-getprovidertable.md) <br/> |Предоставляет доступ к таблице поставщика список поставщиков услуг в профиле.  <br/> |
   
## <a name="remarks"></a>Замечания

Реализация можно получить указатель на интерфейс **IMsgServiceAdmin** двумя способами: путем вызова метода [IMAPISession::AdminServices](imapisession-adminservices.md) или путем вызова метода [IProfAdmin::AdminServices](iprofadmin-adminservices.md) . Для клиентов, в основном беспокоятся с настройки профилей **IProfAdmin::AdminServices** является предпочтительным получить интерфейс **IMsgServiceAdmin** , так как не выполняется вход поставщиков для сеанса MAPI. Если это клиент требуется возможность вносить изменения в текущей конфигурации, **IMAPISession::AdminServices** должен быть вызван получить указатель **IMsgServiceAdmin** . Обратите внимание, что несмотря на то, что MAPI не разрешает профиля, который используется для удаления, существует не защиту клиента на удаление всех служб сообщения в профиле. 
  
## <a name="see-also"></a>См. также



[Интерфейсы MAPI](mapi-interfaces.md)

