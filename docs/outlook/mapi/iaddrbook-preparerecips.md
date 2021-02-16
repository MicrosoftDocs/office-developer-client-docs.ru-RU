---
title: IAddrBookPrepareRecips
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IAddrBook.PrepareRecips
api_type:
- COM
ms.assetid: d423f7b5-23b8-44dd-bca3-6590182dc42d
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: db1c23f33e604d6aafdd8a046566c7390c281ad8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414279"
---
# <a name="iaddrbookpreparerecips"></a>IAddrBook::PrepareRecips

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Подготавливает список получателей к дальнейшему использованию системой обмена сообщениями. 
  
```cpp
HRESULT PrepareRecips(
  ULONG ulFlags,
  LPSPropTagArray lpSPropTagArray,
  LPADRLIST lpRecipList
);
```

## <a name="parameters"></a>Параметры

 _ulFlags_
  
> [in] Битоваяmas флагов, которая управляет открытием записи. Можно установить следующий флаг:
    
MAPI_CACHE_ONLY
  
> Используйте только автономной адресной книги для разрешения имен. Например, этот флаг можно использовать, чтобы разрешить клиентской приложению открывать глобальный список адресов (GAL) в режиме кэшации обмена и получать доступ к записи в этой адресной книге из кэша без создания трафика между клиентом и сервером. Этот флаг поддерживается только поставщиком адресной книги Exchange.
    
 _lpSPropTagArray_
  
> [in] Указатель на структуру [SPropTagArray,](sproptagarray.md) которая содержит массив тегов свойств, которые указывают свойства, если таковые имеются, которые требуют обновления. Параметр  _lpSPropTagArray может_ иметь NULL. 
    
 _lpRecipList_
  
> [in] Указатель на [структуру ADRLIST,](adrlist.md) которая содержит список получателей. 
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Список получателей успешно подготовлен.
    
## <a name="remarks"></a>Примечания

Клиенты и поставщики услуг **звонят методу PrepareRecips,** чтобы сделать следующее: 
  
- Убедитесь, что все получатели в параметре  _lpRecipList_ имеют долгосрочные идентификаторы записей. 
    
- Убедитесь, что каждый получатель в параметре  _lpRecipList_ имеет свойства, указанные в параметре  _lpSPropTagArray,_ и что эти свойства отображаются в начале списка получателей. 
    
MAPI преобразует краткосрочные идентификаторы записей каждого получателя в долгосрочные идентификаторы записей. При необходимости долгосрочные идентификаторы записей получателей извлекаются у соответствующего поставщика адресной книги, и запрашиваются дополнительные свойства.
  
В записи отдельного получателя запрашиваемая запись сначала упорядочена, а затем все свойства, которые уже присутствуют для записи. Если одно или несколько из запрашиваемого свойства в параметре  _lpSPropTagArray_ не обрабатываются соответствующим поставщиком адресной книги, для их типов свойств будет установлено PT_ERROR. Для их свойств будет установлено значение MAPI_E_NOT_FOUND или другое значение, которое дает более конкретную причину, по которой свойства недоступны. Каждая [структура SPropValue,](spropvalue.md) включенная в параметр  _lpRecipList,_ должна быть выделена отдельно с помощью функций [MAPIAllocateBuffer](mapiallocatebuffer.md) и [MAPIAllocateMore,](mapiallocatemore.md) чтобы ее можно было освободить по отдельности. 
  
Сведения о PT_ERROR [см.](property-types.md)в
  
## <a name="see-also"></a>См. также



[ADRLIST](adrlist.md)
  
[IMAPIProp::GetProps](imapiprop-getprops.md)
  
[IMessage::ModifyRecipients](imessage-modifyrecipients.md)
  
[Каноническое свойство PidTagEntryId](pidtagentryid-canonical-property.md)
  
[SPropValue](spropvalue.md)
  
[SRowSet](srowset.md)
  
[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)

