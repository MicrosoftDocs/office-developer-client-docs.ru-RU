---
title: IMAPISession IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISession
api_type:
- COM
ms.assetid: 5650fa2a-6e62-451c-964e-363f7bee2344
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 1c1a66f61fe1533e436f4e35a542f53d938b4d01
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413383"
---
# <a name="imapisession--iunknown"></a>IMAPISession : IUnknown

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Управляет объектами, связанными с сеансом логотипа MAPI.
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapix.h  <br/> |
|Подвергается:  <br/> |Объекты сеанса  <br/> |
|Реализовано в:  <br/> |MAPI  <br/> |
|Вызывающая сторона:  <br/> |Клиентские приложения и MAPI  <br/> |
|Идентификатор интерфейса:  <br/> |IID_IMAPISession  <br/> |
|Тип указателя:  <br/> |LPMAPISESSION  <br/> |
   
## <a name="vtable-order"></a>Заказ Vtable

|||
|:-----|:-----|
|[GetLastError](imapisession-getlasterror.md) <br/> |Возвращает [структуру MAPIERROR, которая](mapierror.md) содержит сведения об ошибке предыдущего сеанса.  <br/> |
|[GetMsgStoresTable](imapisession-getmsgstorestable.md) <br/> |Предоставляет доступ к таблице хранилища сообщений, которая содержит сведения обо всех хранилищах сообщений в профиле сеанса.  <br/> |
|[OpenMsgStore](imapisession-openmsgstore.md) <br/> |Открывает хранилище сообщений и возвращает указатель [IMsgStore](imsgstoreimapiprop.md) для дальнейшего доступа.  <br/> |
|[OpenAddressBook](imapisession-openaddressbook.md) <br/> |Открывает интегрированную адресную книгу MAPI, возвращая указатель [IAddrBook](iaddrbookimapiprop.md) для дальнейшего доступа.  <br/> |
|[OpenProfileSection](imapisession-openprofilesection.md) <br/> |Открывает раздел текущего профиля и возвращает указатель [IProfSect](iprofsectimapiprop.md) для дальнейшего доступа.  <br/> |
|[GetStatusTable](imapisession-getstatustable.md) <br/> |Предоставляет доступ к таблице состояние, таблице, которая содержит сведения обо всех ресурсах MAPI в сеансе.  <br/> |
|[OpenEntry](imapisession-openentry.md) <br/> |Открывает объект и возвращает указатель интерфейса для дальнейшего доступа.  <br/> |
|[CompareEntryIDs](imapisession-compareentryids.md) <br/> |Сравнивает два идентификатора записи, чтобы определить, относятся ли они к одному объекту.  <br/> |
|[Консультирование](imapisession-advise.md) <br/> |Регистрируется для получения уведомления о указанных событиях, влияющих на сеанс.  <br/> |
|[Unadvise](imapisession-unadvise.md) <br/> |Отменяет отправку уведомлений, ранее настроенных с помощью вызова метода **Advise.**  <br/> |
|**MessageOptions** <br/> | *Не поддерживается или не документируется.*  <br/> |
|**QueryDefaultMessageOpt** <br/> | *Не поддерживается или не документируется.*  <br/> |
|[EnumAdrTypes](imapisession-enumadrtypes.md) <br/> |Устарело. Возвращает типы адресов, которые могут обрабатываться всеми поставщиками транспорта в сеансе.  <br/> |
|[QueryIdentity](imapisession-queryidentity.md) <br/> |Возвращает идентификатор входа объекта, который предоставляет основное удостоверение сеанса.  <br/> |
|[Logoff](imapisession-logoff.md) <br/> |Завершает сеанс MAPI.  <br/> |
|[SetDefaultStore](imapisession-setdefaultstore.md) <br/> |Создает хранилище сообщений как хранилище сообщений по умолчанию для сеанса.  <br/> |
|[AdminServices](imapisession-adminservices.md) <br/> |Возвращает [указатель IMsgServiceAdmin](imsgserviceadminiunknown.md) для внесения изменений в службы сообщений.  <br/> |
|[ShowForm](imapisession-showform.md) <br/> |Отображает форму.  <br/> |
|[PrepareForm](imapisession-prepareform.md) <br/> |Создает числимый маркер, который метод **ShowForm** использует для доступа к сообщению.  <br/> |
   
## <a name="see-also"></a>См. также



[Интерфейсы MAPI](mapi-interfaces.md)

