---
title: Иаддрбуксетпаб
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IAddrBook.SetPAB
api_type:
- COM
ms.assetid: 75daf9d4-6975-435f-91e5-1b41e0047ab7
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 29677ce74f405e8ca03f1639f3d98288532e9653
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424618"
---
# <a name="iaddrbooksetpab"></a>IAddrBook::SetPAB

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Назначает определенный контейнер в качестве личной адресной книги (PAB).
  
```cpp
HRESULT SetPAB(
  ULONG cbEntryID,
  LPENTRYID lpEntryID
);
```

## <a name="parameters"></a>Параметры

 _Кбентрид_
  
> возврата Число байтов в идентификаторе записи, на которое указывает параметр _лпентрид_ . 
    
 _Лпентрид_
  
> возврата Указатель на идентификатор записи контейнера, который необходимо назначить в качестве личной АДРЕСНОЙ книги. Параметр _лпентрид_ не может иметь значение null. 
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Указанный контейнер был установлен в качестве личной АДРЕСНОЙ книги.
    
## <a name="remarks"></a>Примечания

Клиенты и поставщики услуг вызывают метод **сетпаб** , чтобы назначить конкретный контейнер в качестве личной адресной книги. PAB — это контейнер, который содержит записи, скопированные из других контейнеров, а также новые записи. 
  
При вызове **сетпаб** создается контейнер в качестве личной адресной книги, пока он не станет недоступен или новый контейнер становится личной адресной книгой при последующих вызовах **сетпаб**. 
  
Клиентам и поставщикам не нужно вызывать метод [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) , чтобы сделать изменение личной адресной книги постоянным. 
  
## <a name="mfcmapi-reference"></a>Справочные материалы по MFCMAPI

Пример кода MFCMAPI указан в приведенной ниже таблице.
  
|**Файл**|**Функция**|**Примечание**|
|:-----|:-----|:-----|
|Абконтдлг. cpp  <br/> |Кабконтдлг:: Онсетпаб  <br/> |MFCMAPI использует метод **сетпаб** , чтобы сделать указанный контейнер личной адресной книгой.  <br/> |
   
## <a name="see-also"></a>См. также



[IAddrBook::GetPAB](iaddrbook-getpab.md)
  
[IAddrBook::GetSearchPath](iaddrbook-getsearchpath.md)
  
[Каноническое свойство PidTagContainerFlags](pidtagcontainerflags-canonical-property.md)
  
[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)


[Mfcmapi (en) � �������� ������� ����](mfcmapi-as-a-code-sample.md)

