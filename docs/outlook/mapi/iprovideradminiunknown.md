---
title: IProviderAdmin IUnknown
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
ms.openlocfilehash: 41195a49d1bf3566c81fe6e97697012209cbc5ac
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809530"
---
# <a name="iprovideradmin--iunknown"></a>IProviderAdmin : IUnknown

  
  
**Относится к**: Outlook 
  
Работа с поставщиков услуг службы сообщений. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapidefs.h  <br/> |
|Предоставляемые:  <br/> |Объекты администрирования поставщика  <br/> |
|Реализованный:  <br/> |MAPI  <br/> |
|Вызывается:  <br/> |Клиентские приложения и поставщиков услуг  <br/> |
|Идентификатор интерфейса:  <br/> |IID_IProviderAdmin  <br/> |
|Тип указателя:  <br/> |LPPROVIDERADMIN  <br/> |
   
## <a name="vtable-order"></a>Порядке vtable

|||
|:-----|:-----|
|[GetLastError](iprovideradmin-getlasterror.md) <br/> |Возвращает структуру [MAPIERROR](mapierror.md) , который содержит сведения о предыдущем ошибки, которые произошли объект администрирования поставщика.  <br/> |
|[GetProviderTable](iprovideradmin-getprovidertable.md) <br/> |Предоставляет доступ к таблице поставщика службы сообщений, список поставщиков услуг службы сообщений.  <br/> |
|[CreateProvider](iprovideradmin-createprovider.md) <br/> |Добавление поставщика услуг службы сообщений.  <br/> |
|[DeleteProvider](iprovideradmin-deleteprovider.md) <br/> |Удаляет поставщика услуг службы сообщений.  <br/> |
|[OpenProfileSection](iprovideradmin-openprofilesection.md) <br/> |Открывает профиля из текущего профиля и возвращает указатель [IProfSect](iprofsectimapiprop.md) для дальнейшей доступа.  <br/> |
   
## <a name="remarks"></a>Замечания

Клиенты могут получить указатель на интерфейс **IProviderAdmin** путем вызова метода [IMsgServiceAdmin::AdminProviders](imsgserviceadmin-adminproviders.md) ; Поставщики услуг, передаются указатель **IProviderAdmin** при вызове функции точки входа их службы сообщений. 
  
## <a name="see-also"></a>См. также



[Интерфейсы MAPI](mapi-interfaces.md)

