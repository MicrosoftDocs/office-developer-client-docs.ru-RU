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
ms.openlocfilehash: bedec72e8371d0e8aa69415d2f0dc77b4c62ff76
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437534"
---
# <a name="iprovideradmin--iunknown"></a>IProviderAdmin : IUnknown

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Работает с поставщиками услуг в службе сообщений. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapidefs.h  <br/> |
|Подвергается:  <br/> |Объекты администрирования поставщика  <br/> |
|Реализовано в:  <br/> |MAPI  <br/> |
|Вызывающая сторона:  <br/> |Клиентские приложения и поставщики услуг  <br/> |
|Идентификатор интерфейса:  <br/> |IID_IProviderAdmin  <br/> |
|Тип указателя:  <br/> |LPPROVIDERADMIN  <br/> |
   
## <a name="vtable-order"></a>Заказ Vtable

|||
|:-----|:-----|
|[GetLastError](iprovideradmin-getlasterror.md) <br/> |Возвращает структуру [MAPIERROR, которая](mapierror.md) содержит сведения о предыдущей ошибке, которая произошла с объектом администрирования поставщика.  <br/> |
|[GetProviderTable](iprovideradmin-getprovidertable.md) <br/> |Предоставляет доступ к таблице поставщиков сообщений, списку поставщиков услуг в службе сообщений.  <br/> |
|[CreateProvider](iprovideradmin-createprovider.md) <br/> |Добавляет поставщика услуг в службу сообщений.  <br/> |
|[DeleteProvider](iprovideradmin-deleteprovider.md) <br/> |Удаляет поставщика услуг из службы сообщений.  <br/> |
|[OpenProfileSection](iprovideradmin-openprofilesection.md) <br/> |Открывает раздел профилей из текущего профиля и возвращает указатель [IProfSect](iprofsectimapiprop.md) для дальнейшего доступа.  <br/> |
   
## <a name="remarks"></a>Примечания

Клиенты могут получить указатель на **интерфейс IProviderAdmin,** назвав [метод IMsgServiceAdmin::AdminProviders;](imsgserviceadmin-adminproviders.md) Поставщикам услуг передается указатель **IProviderAdmin,** когда называется функция точки входа службы сообщений. 
  
## <a name="see-also"></a>См. также



[Интерфейсы MAPI](mapi-interfaces.md)

