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

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Предоставляет доступ к поставщику хранилище сообщений через объект поставщика. Этот объект поставщика для хранения сообщений возвращается при входе поставщика с помощью функции точки входа [MSProviderInit](msproviderinit.md) поставщика. Объект поставщика хранилища сообщений в основном используется клиентские приложения и пулом MAPI для открытия хранилищ сообщений. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapispi.h  <br/> |
|Выставим:  <br/> |Объекты поставщиков хранилищ сообщений  <br/> |
|Реализовано в:  <br/> |Поставщики store сообщений  <br/> |
|Вызывающая сторона:  <br/> |MAPI и пулер MAPI  <br/> |
|Идентификатор интерфейса:  <br/> |IID_IMSProvider  <br/> |
|Тип указателя:  <br/> |LPMSPROVIDER  <br/> |
   
## <a name="vtable-order"></a>Порядок ветвей

|||
|:-----|:-----|
|[Shutdown](imsprovider-shutdown.md) <br/> |Закрывает поставщика store сообщений упорядоченным образом.  <br/> |
|[Logon](imsprovider-logon.md) <br/> |Занося mapI в один экземпляр поставщика хранения сообщений.  <br/> |
|[SpoolerLogon](imsprovider-spoolerlogon.md) <br/> |Занося в журнал пул MAPI в хранилище сообщений.  <br/> |
|[CompareStoreIDs](imsprovider-comparestoreids.md) <br/> |Сравнивает два идентификатора записей в хранилище сообщений, чтобы определить, относятся ли они к одному объекту store.  <br/> |
   
## <a name="remarks"></a>Примечания

MAPI использует один объект поставщика хранилища сообщений в сеансе независимо от того, сколько хранилищ сообщений открывается поставщиком хранилища. Если второй сеанс MAPI входит в какие-либо открытые хранилища, MAPI вызывает **MSProviderInit** еще раз, чтобы создать новый объект поставщика хранилища сообщений для этого сеанса. 
  
Объект поставщика для хранения сообщений должен содержать следующие данные для правильной работы:
  
- Указатель  _программы выделения памяти lpMalloc_ для использования всеми хранилищами, открытыми с помощью этого объекта поставщика. 
    
- Подпрограммные указатели _lpfAllocateBuffer_, _ lpfAllocateMore _и _lpfFreeBuffer_ на функции выделения памяти [MAPIAllocateBuffer,](mapiallocatebuffer.md) [MAPIAllocateMore](mapiallocatemore.md)и [MAPIFreeBuffer.](mapifreebuffer.md) 
    
- Связанный список всех хранилищ, открытых с помощью этого объекта поставщика и еще не закрытых.
    
## <a name="see-also"></a>См. также



[Интерфейсы MAPI](mapi-interfaces.md)

