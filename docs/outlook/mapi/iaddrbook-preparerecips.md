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
description: '���� ���������� ���������: 23 ���� 2011 �.'
ms.openlocfilehash: fe3e098b2b70e77bd0c536002a4724810261bff3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/15/2018
ms.locfileid: "19808782"
---
# <a name="iaddrbookpreparerecips"></a>IAddrBook::PrepareRecips

  
  
**Применимо к**: Outlook 
  
Подготовка списка получателей для дальнейшего использования системой обмена сообщениями. 
  
```cpp
HRESULT PrepareRecips(
  ULONG ulFlags,
  LPSPropTagArray lpSPropTagArray,
  LPADRLIST lpRecipList
);
```

## <a name="parameters"></a>���������

 _ulFlags_
  
> [in] Битовая маска флаги, который определяет, как открыть запись. Можно задать следующий флаг:
    
MAPI_CACHE_ONLY
  
> Для выполнения разрешения имен используйте автономной адресной книги. Например чтобы разрешить клиентским приложением для открытия глобальном списке адресов (GAL) в режиме кэширования данных exchange и для доступа к записи в этот список адресов из кэша без создания трафика между клиентом и сервером можно использовать этот флаг. Этот флаг поддерживается только поставщик Exchange адресной книги.
    
 _lpSPropTagArray_
  
> [in] Указатель на структуру [SPropTagArray](sproptagarray.md) , который содержит массив тегов свойств, которые указывают свойства, при их наличии, который требуется обновление. Параметр _lpSPropTagArray_ может быть NULL. 
    
 _lpRecipList_
  
> [in] Указатель на структуру [ADRLIST](adrlist.md) , содержащий список получателей. 
    
## <a name="return-value"></a>������������ ��������

ЗНАЧЕНИЕ S_OK 
  
> Список получателей успешно подготовлен.
    
## <a name="remarks"></a>Замечания

Клиенты и поставщики услуг вызовите метод **PrepareRecips** для выполните следующее: 
  
- Убедитесь, что всех получателей с помощью параметра _lpRecipList_ имеют долгосрочного идентификаторы записей. 
    
- Убедитесь, что каждого получателя, с помощью параметра _lpRecipList_ имеет свойства, указанные в параметре _lpSPropTagArray_ и, что эти свойства отображаются в начале списка получателей. 
    
MAPI преобразует каждого получателя краткосрочных идентификаторы записей для долгосрочного идентификаторы записей. При необходимости получателей долгосрочного идентификаторы записей извлекаются из соответствующих адресной книге и запрашиваются дополнительные свойства.
  
В отдельную запись получателя запрошенные свойства упорядочены во-первых, следуют все свойства, которые они уже присутствуют запись. Если один или несколько обязательных свойств с помощью параметра _lpSPropTagArray_ не обрабатывается поставщик соответствующие адресной книги, их типы свойств будет иметь значение PT_ERROR. Значения свойств будет иметь значение MAPI_E_NOT_FOUND или другой значение, задающее более конкретные причину, почему свойства недоступны. Каждая структура [SPropValue](spropvalue.md) , включенных в параметре _lpRecipList_ необходимо отдельно выделить с помощью функции [MAPIAllocateBuffer](mapiallocatebuffer.md) и [MAPIAllocateMore](mapiallocatemore.md) , чтобы его можно освободить по отдельности. 
  
Сведения о PT_ERROR содержатся [Типы свойств](property-types.md).
  
## <a name="see-also"></a>См. также



[ADRLIST](adrlist.md)
  
[IMAPIProp::GetProps](imapiprop-getprops.md)
  
[IMessage::ModifyRecipients](imessage-modifyrecipients.md)
  
[Каноническое свойство PidTagEntryId](pidtagentryid-canonical-property.md)
  
[SPropValue](spropvalue.md)
  
[SRowSet](srowset.md)
  
[IAddrBook: IMAPIProp](iaddrbookimapiprop.md)

