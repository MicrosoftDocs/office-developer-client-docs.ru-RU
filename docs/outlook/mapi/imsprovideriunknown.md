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
ms.openlocfilehash: 1c00e54d02ba494c94c9826eabe142e1bd3b9a80
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22579629"
---
# <a name="imsprovider--iunknown"></a>IMSProvider : IUnknown

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Предоставляет доступ к поставщику хранилища сообщений через объект поставщика хранилища сообщений. Этот объект поставщика хранилища сообщений возвращается при входе в систему поставщика функции точки входа [MSProviderInit](msproviderinit.md) поставщика хранилища сообщений. Объект поставщика хранилища сообщений в основном используется для открытия хранилищ сообщений с клиентскими приложениями и диспетчер очереди MAPI. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapispi.h  <br/> |
|Предоставляемые:  <br/> |Объекты поставщика хранилища сообщений  <br/> |
|Реализованный:  <br/> |Поставщики хранилища сообщений  <br/> |
|Вызывается:  <br/> |MAPI и диспетчер очереди MAPI  <br/> |
|Идентификатор интерфейса:  <br/> |IID_IMSProvider  <br/> |
|Тип указателя:  <br/> |LPMSPROVIDER  <br/> |
   
## <a name="vtable-order"></a>Порядке vtable

|||
|:-----|:-----|
|[Shutdown](imsprovider-shutdown.md) <br/> |Закрывает поставщика хранилища сообщений определенным образом.  <br/> |
|[Вход в систему](imsprovider-logon.md) <br/> |Журналы MAPI на один экземпляр поставщика хранилища сообщений.  <br/> |
|[SpoolerLogon](imsprovider-spoolerlogon.md) <br/> |Журналы очереди MAPI вход в систему хранения сообщений.  <br/> |
|[CompareStoreIDs](imsprovider-comparestoreids.md) <br/> |Сравнение двух сообщений идентификаторы хранилища записей для определения, является ли они ссылаются на тот же объект хранилища.  <br/> |
   
## <a name="remarks"></a>Замечания

MAPI использует один объект поставщика хранилища сообщений на сеанс, независимо от того, сколько сообщений хранилищ открываются поставщиком хранилища. Если второй журналы сеанса MAPI на любой open хранилищ, MAPI вызывает **MSProviderInit** еще раз для создания нового объекта поставщика хранилища сообщений для данного сеанса для использования. 
  
Объект поставщика хранилища сообщений, должна содержать следующие действия, чтобы обеспечить правильное функционирование:
  
- _LpMalloc_ выделение памяти выполнять рутинные указатель для использования сервером все открыто с помощью этого объекта поставщика хранилища. 
    
- _LpfAllocateBuffer_, _ lpfAllocateMore _ и _lpfFreeBuffer_ процедуры указатели на [MAPIAllocateBuffer](mapiallocatebuffer.md), [MAPIAllocateMore](mapiallocatemore.md)и [MAPIFreeBuffer](mapifreebuffer.md) функций выделения памяти. 
    
- Связанный список всех хранилищ открыто с помощью этого объекта поставщика и еще не закрытый.
    
## <a name="see-also"></a>См. также



[Интерфейсы MAPI](mapi-interfaces.md)

