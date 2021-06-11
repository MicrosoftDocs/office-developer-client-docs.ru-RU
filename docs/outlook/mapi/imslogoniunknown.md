---
title: IMSLogon IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMSLogon
api_type:
- COM
ms.assetid: d87093dc-f705-465f-ab3c-944ca0cd3e54
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 991e48aa458a58ad2d7d688e81dbb357ef9bda5b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428881"
---
# <a name="imslogon--iunknown"></a>IMSLogon : IUnknown

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Доступ к ресурсам в объекте logon магазина сообщений.
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapispi.h  <br/> |
|Подвергается:  <br/> |Объекты логона магазина сообщений  <br/> |
|Реализовано в:  <br/> |Поставщики магазинов сообщений  <br/> |
|Вызывающая сторона:  <br/> |MAPI  <br/> |
|Идентификатор интерфейса:  <br/> |IID_IMSLogon  <br/> |
|Тип указателя:  <br/> |LPMSLOGON  <br/> |
   
## <a name="vtable-order"></a>Заказ Vtable

|||
|:-----|:-----|
|[GetLastError](imslogon-getlasterror.md) <br/> |Возвращает структуру [MAPIERROR, которая](mapierror.md) содержит сведения о последней ошибке, которая произошла для объекта магазина сообщений.  <br/> |
|[Logoff](imslogon-logoff.md) <br/> |Журналы поставщика магазина сообщений.  <br/> |
|[OpenEntry](imslogon-openentry.md) <br/> |Открывает папку или объект сообщения и возвращает указатель на объект, чтобы обеспечить дополнительный доступ.  <br/> |
|[CompareEntryIDs](imslogon-compareentryids.md) <br/> |Сравнивает два идентификатора записи, чтобы определить, относятся ли они к одному объекту.  <br/> |
|[Консультирование](imslogon-advise.md) <br/> |Регистрирует объект с поставщиком магазина сообщений для уведомлений об изменениях в хранилище сообщений.  <br/> |
|[Unadvise](imslogon-unadvise.md) <br/> |Удаляет регистрацию объекта для уведомления об изменениях в хранилище сообщений, ранее установленных с помощью вызова метода **IMSLogon::Advise.**  <br/> |
|[OpenStatusEntry](imslogon-openstatusentry.md) <br/> |Открывает объект состояния.  <br/> |
   
## <a name="remarks"></a>Примечания

Объект logon магазина сообщений является частью поставщика магазина открытых сообщений, который вызывает MAPI напрямую. Между объектом логотипа магазина сообщений, вызываемого MAPI, и объектом магазина сообщений, вызываемого клиентских приложений, существует один к одному. вы можете думать о логотипе и хранить объекты как один объект, который предоставляет два интерфейса. Эти два объекта создаются вместе и освобождены вместе.
  
## <a name="see-also"></a>См. также



[Интерфейсы MAPI](mapi-interfaces.md)

