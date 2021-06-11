---
title: IMSProvider IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMSProvider
api_type:
- COM
ms.assetid: 0f17aa44-abcb-4732-b013-d91652847cf6
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: c5305ddd20b690f5c2e5807fb7ce2410549f7124
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412865"
---
# <a name="imsprovider--iunknown"></a>IMSProvider : IUnknown

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Предоставляет доступ к поставщику хранения сообщений через объект поставщика магазина сообщений. Этот объект поставщика хранения сообщений возвращается в логотипе поставщика функцией точки входа [поставщика msProviderInit](msproviderinit.md) поставщика сообщений. Объект поставщика хранилища сообщений используется в основном клиентские приложения и пульпер MAPI для открытия магазинов сообщений. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapispi.h  <br/> |
|Подвергается:  <br/> |Объекты поставщиков хранилищ сообщений  <br/> |
|Реализовано в:  <br/> |Поставщики магазинов сообщений  <br/> |
|Вызывающая сторона:  <br/> |MAPI и шпалер MAPI  <br/> |
|Идентификатор интерфейса:  <br/> |IID_IMSProvider  <br/> |
|Тип указателя:  <br/> |LPMSPROVIDER  <br/> |
   
## <a name="vtable-order"></a>Заказ Vtable

|||
|:-----|:-----|
|[Shutdown](imsprovider-shutdown.md) <br/> |Закрывает поставщика магазина сообщений упорядоченным способом.  <br/> |
|[Logon](imsprovider-logon.md) <br/> |Журнал MAPI для одного экземпляра поставщика магазина сообщений.  <br/> |
|[SpoolerLogon](imsprovider-spoolerlogon.md) <br/> |Регистрирую пульпер MAPI в хранилище сообщений.  <br/> |
|[CompareStoreIDs](imsprovider-comparestoreids.md) <br/> |Сравнивает два идентификатора входа в хранилище сообщений, чтобы определить, относятся ли они к одному объекту магазина.  <br/> |
   
## <a name="remarks"></a>Примечания

MAPI использует один объект поставщика хранилища сообщений в сеансе независимо от того, сколько магазинов сообщений открывается поставщиком. Если второй сеанс MAPI входит в открытые магазины, MAPI вызывает **MSProviderInit** во второй раз, чтобы создать новый объект поставщика хранилища сообщений для этого сеанса. 
  
Объект поставщика хранения сообщений должен содержать следующие данные, чтобы правильно работать:
  
- Обычный  _указатель памяти lpMalloc_ для использования во всех магазинах, открытых с помощью этого объекта-поставщика. 
    
- Плановые указатели _lpfAllocateBuffer_, _ lpfAllocateMore _и _lpfFreeBuffer_ на функции распределения памяти [MAPIAllocateBuffer,](mapiallocatebuffer.md) [MAPIAllocateMore](mapiallocatemore.md)и [MAPIFreeBuffer.](mapifreebuffer.md) 
    
- Связанный список всех магазинов, открытых с помощью этого объекта-поставщика и еще не закрытых.
    
## <a name="see-also"></a>См. также



[Интерфейсы MAPI](mapi-interfaces.md)

