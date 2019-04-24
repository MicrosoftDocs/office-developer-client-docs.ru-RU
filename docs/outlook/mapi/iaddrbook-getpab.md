---
title: Иаддрбукжетпаб
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IAddrBook.GetPAB
api_type:
- COM
ms.assetid: 9830e09c-700f-469b-a54d-4e4e0583aa84
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 6c565c088fd4ef7d5df141bf770c560f79535998
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32349303"
---
# <a name="iaddrbookgetpab"></a>IAddrBook::GetPAB

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Возвращает идентификатор элемента контейнера, назначенный в качестве личной адресной книги (PAB).
  
```cpp
HRESULT GetPAB(
  ULONG FAR * lpcbEntryID,
  LPENTRYID FAR * lppEntryID
);
```

## <a name="parameters"></a>Параметры

 _Лпкбентрид_
  
> вышли Указатель на число байтов в идентификаторе записи, на который указывает параметр _лппентрид_ . 
    
 _Лппентрид_
  
> вышли Указатель на указатель на идентификатор записи личной АДРЕСНОЙ книги. Параметр _лппентрид_ содержит ноль, если контейнер не назначен в качестве личной адресной книги. 
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Идентификатор записи личной АДРЕСНОЙ книги успешно возвращен.
    
## <a name="remarks"></a>Примечания

Клиенты вызывают метод **жетпаб** для получения идентификатора записи контейнера, назначенного в качестве личной адресной книги. Если в профиле не установлена PAB, MAPI выбирает в качестве личной АДРЕСНОЙ книги первый контейнер в иерархии адресной книги, который разрешает изменения. 
  
## <a name="mfcmapi-reference"></a>Справочные материалы по MFCMAPI

Пример кода MFCMAPI указан в приведенной ниже таблице.
  
|**Файл**|**Функция**|**Примечание**|
|:-----|:-----|:-----|
|Маиндлг. cpp  <br/> |Кмаиндлг:: Онопенпаб  <br/> |MFCMAPI использует метод **жетпаб** , чтобы получить идентификатор для личной адресной книги пользователя.  <br/> |
   
## <a name="see-also"></a>См. также



[MAPIAllocateBuffer](mapiallocatebuffer.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[Каноническое свойство PidTagContainerFlags](pidtagcontainerflags-canonical-property.md)
  
[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)


[Mfcmapi (en) � �������� ������� ����](mfcmapi-as-a-code-sample.md)

