---
title: Ипровидерадмин IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IProviderAdmin
api_type:
- COM
ms.assetid: bdb4cdca-8dfd-4f90-9467-ec31cea3f518
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: bedec72e8371d0e8aa69415d2f0dc77b4c62ff76
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32315528"
---
# <a name="iprovideradmin--iunknown"></a>IProviderAdmin : IUnknown

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Работает с поставщиками услуг в службе сообщений. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |MAPIDEFS. h  <br/> |
|Предоставлено:  <br/> |Объекты администрирования поставщика  <br/> |
|Реализовано в:  <br/> |MAPI  <br/> |
|Вызывающая сторона:  <br/> |Клиентские приложения и поставщики услуг  <br/> |
|Идентификатор интерфейса:  <br/> |Иид_ипровидерадмин  <br/> |
|Тип указателя:  <br/> |ЛППРОВИДЕРАДМИН  <br/> |
   
## <a name="vtable-order"></a>Заказ vtable

|||
|:-----|:-----|
|[GetLastError](iprovideradmin-getlasterror.md) <br/> |Возвращает структуру [мапиеррор](mapierror.md) , которая содержит сведения о предыдущей ошибке, произошедшей для объекта администрирования поставщика.  <br/> |
|[Жетпровидертабле](iprovideradmin-getprovidertable.md) <br/> |Предоставляет доступ к таблице поставщика службы сообщений, список поставщиков служб в службе сообщений.  <br/> |
|[Креатепровидер](iprovideradmin-createprovider.md) <br/> |Добавляет поставщика услуг в службу сообщений.  <br/> |
|[Делетепровидер](iprovideradmin-deleteprovider.md) <br/> |Удаляет поставщика услуг из службы сообщений.  <br/> |
|[Опенпрофилесектион](iprovideradmin-openprofilesection.md) <br/> |Открывает раздел профиля из текущего профиля и возвращает указатель [ипрофсект](iprofsectimapiprop.md) для получения дальнейших прав.  <br/> |
   
## <a name="remarks"></a>Замечания

Клиенты могут получить указатель на интерфейс **ипровидерадмин** , вызвав метод [Имсгсервицеадмин:: админпровидерс](imsgserviceadmin-adminproviders.md) ; поставщики услуг передаются в качестве указателя **ипровидерадмин** при вызове функции точки входа для службы сообщений. 
  
## <a name="see-also"></a>См. также



[Интерфейсы MAPI](mapi-interfaces.md)

