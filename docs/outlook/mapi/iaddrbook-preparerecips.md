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

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Подготавливает список получателей для более позднего использования системой обмена сообщениями. 
  
```cpp
HRESULT PrepareRecips(
  ULONG ulFlags,
  LPSPropTagArray lpSPropTagArray,
  LPADRLIST lpRecipList
);
```

## <a name="parameters"></a>Parameters

 _ulFlags_
  
> [in] Битмашка флагов, контролируемая тем, как открывается запись. Можно установить следующий флаг:
    
MAPI_CACHE_ONLY
  
> Для выполнения разрешения имен используйте только офлайн-адресную книгу. Например, этот флаг можно использовать для того, чтобы клиентская заявка открыла глобальный адресный список (GAL) в кэшировом режиме обмена и доступ к записи в этой адресной книге из кэша без создания трафика между клиентом и сервером. Этот флаг поддерживается только поставщиком Exchange адресной книги.
    
 _lpSPropTagArray_
  
> [in] Указатель на структуру [SPropTagArray,](sproptagarray.md) которая содержит массив тегов свойств, которые указывают свойства, если таковые имеются, которые требуют обновления. Параметр  _lpSPropTagArray может_ быть NULL. 
    
 _lpRecipList_
  
> [in] Указатель на структуру [ADRLIST,](adrlist.md) которая содержит список получателей. 
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Список получателей был успешно подготовлен.
    
## <a name="remarks"></a>Примечания

Клиенты и поставщики услуг звонят по **методу PrepareRecips,** чтобы сделать следующее: 
  
- Убедитесь, что все получатели в  _параметре lpRecipList_ имеют долгосрочные идентификаторы записи. 
    
- Убедитесь, что каждый получатель в параметре  _lpRecipList_ имеет свойства, указанные в параметре  _lpSPropTagArray,_ и чтобы эти свойства появились в начале списка получателей. 
    
MAPI преобразует краткосрочные идентификаторы записи каждого получателя в долгосрочные идентификаторы записи. При необходимости долгосрочные идентификаторы записей получателей извлекаются из соответствующего поставщика адресной книги, и запрашиваются дополнительные свойства.
  
В отдельной записи получателя запрашиваются сначала запрашиваемые свойства, а затем все свойства, которые уже присутствовали для записи. Если одно или несколько запрашиваемого свойства в параметре  _lpSPropTagArray_ не обрабатываются соответствующим поставщиком адресной книги, их типы свойств будут заданы PT_ERROR. Их значения свойств будут задатки MAPI_E_NOT_FOUND или другому значению, которое дает более конкретную причину, по которой свойства недоступны. Каждая [структура SPropValue,](spropvalue.md) включенная в параметр  _lpRecipList,_ должна быть выделена отдельно с помощью функций [MAPIAllocateBuffer](mapiallocatebuffer.md) и [MAPIAllocateMore,](mapiallocatemore.md) чтобы ее можно было освободить по отдельности. 
  
Сведения о PT_ERROR см. в этой PT_ERROR [типах свойств.](property-types.md)
  
## <a name="see-also"></a>См. также



[ADRLIST](adrlist.md)
  
[IMAPIProp::GetProps](imapiprop-getprops.md)
  
[IMessage::ModifyRecipients](imessage-modifyrecipients.md)
  
[Каноническое свойство PidTagEntryId](pidtagentryid-canonical-property.md)
  
[SPropValue](spropvalue.md)
  
[SRowSet](srowset.md)
  
[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)

