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
ms.openlocfilehash: aba61d4acf7c1f9a5d91fa15f1ca6b16f173bcb2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426137"
---
# <a name="imsgserviceadmin--iunknown"></a>IMsgServiceAdmin : IUnknown

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Вносит изменения в службу сообщений в профиле.
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |MapiX.h  <br/> |
|Подвергается:  <br/> |Объекты администрирования службы сообщений  <br/> |
|Реализовано в:  <br/> |MAPI  <br/> |
|Вызывающая сторона:  <br/> |Клиентские приложения  <br/> |
|Идентификатор интерфейса:  <br/> |IID_IMsgServiceAdmin  <br/> |
|Тип указателя:  <br/> |LPSERVICEADMIN  <br/> |
   
## <a name="vtable-order"></a>Заказ Vtable

|||
|:-----|:-----|
|[GetLastError](imsgserviceadmin-getlasterror.md) <br/> |Возвращает структуру [MAPIERROR, которая](mapierror.md) содержит сведения о последней ошибке, порожденной объектом администрирования службы сообщений.  <br/> |
|[GetMsgServiceTable](imsgserviceadmin-getmsgservicetable.md) <br/> |Предоставляет доступ к таблице служб сообщений, списку служб сообщений в профиле.  <br/> |
|[CreateMsgService](imsgserviceadmin-createmsgservice.md) <br/> |Добавляет службу сообщений в текущий профиль.  <br/> <br/>**ПРИМЕЧАНИЕ.** Этот метод не используется. Вместо [этого используйте IMsgServiceAdmin2::CreateMsgServiceEx.](imsgserviceadmin2-createmsgserviceex.md)           |
|[DeleteMsgService](imsgserviceadmin-deletemsgservice.md) <br/> |Удаляет службу сообщений из профиля.  <br/> |
|[CopyMsgService](imsgserviceadmin-copymsgservice.md) <br/> |Копирует службу сообщений в профиль.  <br/> |
|[ПереименованиеMsgService](imsgserviceadmin-renamemsgservice.md) <br/> |Устарело. Назначает новое имя службе сообщений.  <br/> |
|[НастройкаMsgService](imsgserviceadmin-configuremsgservice.md) <br/> |Перенастройка службы сообщений.  <br/> |
|[OpenProfileSection](imsgserviceadmin-openprofilesection.md) <br/> |Открывает раздел текущего профиля и возвращает указатель [IProfSect](iprofsectimapiprop.md) для дальнейшего доступа.  <br/> |
|[MsgServiceTransportOrder](imsgserviceadmin-msgservicetransportorder.md) <br/> |Задает порядок, в котором операторы транспорта вызваны для доставки сообщения.  <br/> |
|[AdminProviders](imsgserviceadmin-adminproviders.md) <br/> |Возвращает указатель, который предоставляет доступ к объекту администрирования поставщика.  <br/> |
|[SetPrimaryIdentity](imsgserviceadmin-setprimaryidentity.md) <br/> |Назначает службу сообщений поставщиком основного удостоверения для профиля.  <br/> |
|[GetProviderTable](imsgserviceadmin-getprovidertable.md) <br/> |Предоставляет доступ к таблице поставщиков, списку поставщиков услуг в профиле.  <br/> |
   
## <a name="remarks"></a>Примечания

Реализация может получить указатель на интерфейс **IMsgServiceAdmin** двумя способами: вызовом метода [IMAPISession::AdminServices](imapisession-adminservices.md) или методом [IProfAdmin::AdminServices.](iprofadmin-adminservices.md) Для клиентов, в основном заинтересованных в конфигурации профиля, **IProfAdmin::AdminServices** является предпочтительным способом получения **интерфейса IMsgServiceAdmin,** так как он не входит в систему поставщиков для сеанса MAPI. Если клиенту требуется возможность внести изменения в активный профиль, для получения указателя **IMsgServiceAdmin** следует вызволить **IMAPISession::AdminServices.** Следует помнить, что несмотря на то, что MAPI не разрешает удаление используемого профиля, нет никаких гарантий, препятствующих удаляемому клиентом всем службам сообщений в профиле. 
  
## <a name="see-also"></a>См. также



[Интерфейсы MAPI](mapi-interfaces.md)

