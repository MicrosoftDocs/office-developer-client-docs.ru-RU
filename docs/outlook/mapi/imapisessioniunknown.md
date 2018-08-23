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
ms.openlocfilehash: 163bce38d665a8566fd703420ff1f7b2f44f7c63
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22571810"
---
# <a name="imapisession--iunknown"></a>IMAPISession : IUnknown

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Управляет объекты, связанные с сеанса входа MAPI.
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapix.h  <br/> |
|Предоставляемые:  <br/> |Объекты сеанса  <br/> |
|Реализованный:  <br/> |MAPI  <br/> |
|Вызывается:  <br/> |Клиентские приложения и MAPI  <br/> |
|Идентификатор интерфейса:  <br/> |IID_IMAPISession  <br/> |
|Тип указателя:  <br/> |LPMAPISESSION  <br/> |
   
## <a name="vtable-order"></a>Порядке vtable

|||
|:-----|:-----|
|[GetLastError](imapisession-getlasterror.md) <br/> |Возвращает структуру [MAPIERROR](mapierror.md) , которая содержит сведения об ошибке предыдущего сеанса.  <br/> |
|[GetMsgStoresTable](imapisession-getmsgstorestable.md) <br/> |Предоставляет доступ к таблице хранилища сообщений, который содержит сведения о всех хранилищ сообщений в профиле сеанса.  <br/> |
|[OpenMsgStore](imapisession-openmsgstore.md) <br/> |Открывает хранилища сообщений и возвращает указатель [IMsgStore](imsgstoreimapiprop.md) для дальнейшей доступа.  <br/> |
|[OpenAddressBook](imapisession-openaddressbook.md) <br/> |Открывает интегрированной адресной книги MAPI, возвращает указатель [IAddrBook](iaddrbookimapiprop.md) для дальнейшей доступа.  <br/> |
|[OpenProfileSection](imapisession-openprofilesection.md) <br/> |Откроется раздел текущего профиля и возвращает указатель [IProfSect](iprofsectimapiprop.md) для дальнейшей доступа.  <br/> |
|[GetStatusTable](imapisession-getstatustable.md) <br/> |Предоставляет доступ к таблице состояния, таблицу, содержащую сведения обо всех ресурсах MAPI в сеансе.  <br/> |
|[OpenEntry](imapisession-openentry.md) <br/> |Открывает объект и возвращает указатель интерфейса для дальнейшей доступа.  <br/> |
|[CompareEntryIDs](imapisession-compareentryids.md) <br/> |Сравнение двух идентификаторы записей для определения, является ли они ссылаются на тот же объект.  <br/> |
|[Уведомить](imapisession-advise.md) <br/> |Регистрация для получения уведомлений о указанного события, которые влияют на сеанс.  <br/> |
|[Unadvise](imapisession-unadvise.md) <br/> |Показано, как отменить отправку уведомлений, ранее настройка с помощью вызова метода **уведомлений** .  <br/> |
|**Параметры сообщения** <br/> | *Не поддерживается, документированных.*  <br/> |
|**QueryDefaultMessageOpt** <br/> | *Не поддерживается, документированных.*  <br/> |
|[EnumAdrTypes](imapisession-enumadrtypes.md) <br/> |Рекомендуется использовать. Возвращает типы адресов, которые могут быть обработаны всеми поставщиками транспорта в сеансе.  <br/> |
|[QueryIdentity](imapisession-queryidentity.md) <br/> |Возвращает идентификатор записи объекта, который содержит основной идентификатор для этого сеанса.  <br/> |
|[Выход из системы](imapisession-logoff.md) <br/> |Завершение сеанса MAPI.  <br/> |
|[SetDefaultStore](imapisession-setdefaultstore.md) <br/> |Устанавливает хранилище сообщений в качестве хранилища сообщений по умолчанию для сеанса.  <br/> |
|[AdminServices](imapisession-adminservices.md) <br/> |Возвращает указатель [IMsgServiceAdmin](imsgserviceadminiunknown.md) для внесения изменений в службы сообщений.  <br/> |
|[ShowForm](imapisession-showform.md) <br/> |Отображает форму.  <br/> |
|[PrepareForm](imapisession-prepareform.md) <br/> |Создает числовое маркера, который использует метод **ShowForm** для доступа к сообщению.  <br/> |
   
## <a name="see-also"></a>См. также



[Интерфейсы MAPI](mapi-interfaces.md)

