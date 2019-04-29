---
title: Имсгсервицеадмин IUnknown
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

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Вносит изменения в службу сообщений в профиле.
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Мапикс. h  <br/> |
|Предоставлено:  <br/> |Объекты администрирования службы сообщений  <br/> |
|Реализовано в:  <br/> |MAPI  <br/> |
|Вызывающая сторона:  <br/> |Клиентские приложения  <br/> |
|Идентификатор интерфейса:  <br/> |Иид_имсгсервицеадмин  <br/> |
|Тип указателя:  <br/> |ЛПСЕРВИЦЕАДМИН  <br/> |
   
## <a name="vtable-order"></a>Заказ vtable

|||
|:-----|:-----|
|[GetLastError](imsgserviceadmin-getlasterror.md) <br/> |Возвращает структуру [мапиеррор](mapierror.md) , которая содержит сведения о последней ошибке, созданной объектом администрирования службы сообщений.  <br/> |
|[Жетмсгсервицетабле](imsgserviceadmin-getmsgservicetable.md) <br/> |Предоставляет доступ к таблице службы сообщений, списку служб сообщений в профиле.  <br/> |
|[Креатемсгсервице](imsgserviceadmin-createmsgservice.md) <br/> |Добавляет службу сообщений в текущий профиль.  <br/> <br/>**Примечание**: Этот метод является устаревшим. Используйте [IMsgServiceAdmin2:: креатемсгсервицеекс](imsgserviceadmin2-createmsgserviceex.md) .           |
|[Делетемсгсервице](imsgserviceadmin-deletemsgservice.md) <br/> |Удаляет службу сообщений из профиля.  <br/> |
|[Копимсгсервице](imsgserviceadmin-copymsgservice.md) <br/> |Копирует службу сообщений в профиль.  <br/> |
|[Ренамемсгсервице](imsgserviceadmin-renamemsgservice.md) <br/> |Устаревшие. Назначает новое имя службе сообщений.  <br/> |
|[Конфигуремсгсервице](imsgserviceadmin-configuremsgservice.md) <br/> |Перестраивает службу сообщений.  <br/> |
|[Опенпрофилесектион](imsgserviceadmin-openprofilesection.md) <br/> |Открывает раздел текущего профиля и возвращает указатель [ипрофсект](iprofsectimapiprop.md) для получения дальнейших прав.  <br/> |
|[Мсгсервицетранспортордер](imsgserviceadmin-msgservicetransportorder.md) <br/> |Задает порядок, в котором будут вызываться поставщики транспорта для доставки сообщения.  <br/> |
|[Админпровидерс](imsgserviceadmin-adminproviders.md) <br/> |Возвращает указатель, который предоставляет доступ к объекту администрирования поставщика.  <br/> |
|[Сетпримаридентити](imsgserviceadmin-setprimaryidentity.md) <br/> |Назначает службу сообщений поставщику основного удостоверения для профиля.  <br/> |
|[Жетпровидертабле](imsgserviceadmin-getprovidertable.md) <br/> |Предоставляет доступ к таблице поставщика, в которой перечислены поставщики служб в профиле.  <br/> |
   
## <a name="remarks"></a>Примечания

Реализация может получить указатель на интерфейс **имсгсервицеадмин** двумя способами: вызвав метод [IMAPISession:: админсервицес](imapisession-adminservices.md) или вызвав метод [ипрофадмин:: админсервицес](iprofadmin-adminservices.md) . Для клиентов, в основном основанных на конфигурации профиля, **ипрофадмин:: админсервицес** является предпочтительным способом получения интерфейса **имсгсервицеадмин** , так как он не выполняет вход поставщиков в сеанс MAPI. Если клиенту требуется возможность вносить изменения в активный профиль, то **IMAPISession:: админсервицес** должен вызываться для получения указателя **имсгсервицеадмин** . Имейте в виду, что хотя MAPI не разрешает удалять профиль, который используется для удаления, нет мер безопасности, препятствующих удалению клиентов удалять все службы сообщений в профиле. 
  
## <a name="see-also"></a>См. также



[Интерфейсы MAPI](mapi-interfaces.md)

