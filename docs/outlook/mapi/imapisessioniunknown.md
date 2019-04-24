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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328289"
---
# <a name="imapisession--iunknown"></a>IMAPISession : IUnknown

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Управляет объектами, связанными с сеансом входа MAPI.
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Мапикс. h  <br/> |
|Предоставлено:  <br/> |Объекты Session  <br/> |
|Реализовано в:  <br/> |MAPI  <br/> |
|Вызывающая сторона:  <br/> |Клиентские приложения и MAPI  <br/> |
|Идентификатор интерфейса:  <br/> |Иид_имаписессион  <br/> |
|Тип указателя:  <br/> |ЛПМАПИСЕССИОН  <br/> |
   
## <a name="vtable-order"></a>Заказ vtable

|||
|:-----|:-----|
|[GetLastError](imapisession-getlasterror.md) <br/> |Возвращает структуру [мапиеррор](mapierror.md) , содержащую сведения об ошибке предыдущего сеанса.  <br/> |
|[Жетмсгсторестабле](imapisession-getmsgstorestable.md) <br/> |Предоставляет доступ к таблице хранилища сообщений, в которой содержатся сведения обо всех хранилищах сообщений в профиле сеанса.  <br/> |
|[Опенмсгсторе](imapisession-openmsgstore.md) <br/> |Открывает хранилище сообщений и возвращает указатель [IMsgStore](imsgstoreimapiprop.md) для получения доступа.  <br/> |
|[Опенаддрессбук](imapisession-openaddressbook.md) <br/> |Открывает интегрированную адресную книгу MAPI, возвращая указатель [IAddrBook](iaddrbookimapiprop.md) для получения доступа.  <br/> |
|[Опенпрофилесектион](imapisession-openprofilesection.md) <br/> |Открывает раздел текущего профиля и возвращает указатель [ипрофсект](iprofsectimapiprop.md) для получения дальнейших прав.  <br/> |
|[Жетстатустабле](imapisession-getstatustable.md) <br/> |Предоставляет доступ к таблице Status (таблица), в которой содержатся сведения обо всех ресурсах MAPI в сеансе.  <br/> |
|[OpenEntry](imapisession-openentry.md) <br/> |Открывает объект и возвращает указатель интерфейса для получения дальнейших прав.  <br/> |
|[CompareEntryIDs](imapisession-compareentryids.md) <br/> |Сравнивает два идентификатора записи, чтобы определить, ссылаются ли они на один и тот же объект.  <br/> |
|[Рекомендуем](imapisession-advise.md) <br/> |Регистрируется для получения уведомлений об указанных событиях, влияющих на сеанс.  <br/> |
|[Unadvise](imapisession-unadvise.md) <br/> |ОтМеняет отправку уведомлений, ранее настроенных с помощью вызова метода **advise** .  <br/> |
|**Мессажеоптионс** <br/> | *Не поддерживается или не задокументировано.*  <br/> |
|**Куеридефаултмессажеопт** <br/> | *Не поддерживается или не задокументировано.*  <br/> |
|[Енумадртипес](imapisession-enumadrtypes.md) <br/> |Устаревшие. Возвращает типы адресов, которые могут обрабатываться всеми поставщиками транспорта в сеансе.  <br/> |
|[Куеридентити](imapisession-queryidentity.md) <br/> |Возвращает идентификатор записи объекта, который предоставляет основной идентификатор для сеанса.  <br/> |
|[Logoff](imapisession-logoff.md) <br/> |Завершает сеанс MAPI.  <br/> |
|[Сетдефаултсторе](imapisession-setdefaultstore.md) <br/> |Устанавливает хранилище сообщений в качестве хранилища сообщений по умолчанию для данного сеанса.  <br/> |
|[Админсервицес](imapisession-adminservices.md) <br/> |Возвращает указатель [имсгсервицеадмин](imsgserviceadminiunknown.md) для внесения изменений в службы сообщений.  <br/> |
|[Шовформ](imapisession-showform.md) <br/> |Отображает форму.  <br/> |
|[Препареформ](imapisession-prepareform.md) <br/> |Создает числовой маркер, который метод **шовформ** использует для доступа к сообщению.  <br/> |
   
## <a name="see-also"></a>См. также



[Интерфейсы MAPI](mapi-interfaces.md)

