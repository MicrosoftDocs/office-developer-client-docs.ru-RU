---
title: Иаддрбукжетдефаултдир
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IAddrBook.GetDefaultDir
api_type:
- COM
ms.assetid: 7a9fdf3f-fd76-40fb-8217-967c6efba5f6
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: d9ad74d8ae02a49ee3c222394caedfd571f84b1c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32336696"
---
# <a name="iaddrbookgetdefaultdir"></a>IAddrBook::GetDefaultDir

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Возвращает идентификатор для исходного контейнера адресных книг.
  
```cpp
HRESULT GetDefaultDir(
  ULONG FAR * lpcbEntryID,
  LPENTRYID FAR * lppEntryID
);
```

## <a name="parameters"></a>Параметры

 _Лпкбентрид_
  
> вышли Указатель на число байтов в идентификаторе записи, на который указывает параметр _лппентрид_ . 
    
 _Лппентрид_
  
> вышли Указатель на указатель на идентификатор элемента контейнера по умолчанию.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Идентификатор элемента контейнера по умолчанию успешно возвращен.
    
## <a name="remarks"></a>Комментарии

Клиентские приложения и поставщики услуг вызывают метод **жетдефаултдир** для получения идентификатора записи контейнера адресной книги по умолчанию. По умолчанию при первом открытии адресной книги пользователь видит отображаемый в адресной книге. Если контейнер по умолчанию не был задан при вызове метода [IAddrBook:: сетдефаултдир](iaddrbook-setdefaultdir.md) , то в качестве контейнера по умолчанию используется MAPI, который является первым контейнером с именами, не являющийся личной адресной книгой (PAB). Если такой контейнер не удается найти, PAB становится контейнером по умолчанию. 
  
Чтобы задать каталог по умолчанию, клиент или поставщик вызывает метод **сетдефаултдир** . Клиентам и поставщикам не нужно вызывать метод [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) ; так как изменения в адресной книге не являются транзакционными, изменения немедленно вносятся в окончательные. 
  
## <a name="mfcmapi-reference"></a>Справочные материалы по MFCMAPI

Пример кода MFCMAPI указан в приведенной ниже таблице.
  
|**Файл**|**Функция**|**Примечание**|
|:-----|:-----|:-----|
|Маиндлг. cpp  <br/> |Кмаиндлг:: Онопендефаултдир  <br/> |MFCMAPI использует метод **жетдефаултдир** , чтобы получить идентификатор для контейнера адресной книги по умолчанию.  <br/> |
   
## <a name="see-also"></a>См. также



[IAddrBook::SetDefaultDir](iaddrbook-setdefaultdir.md)
  
[MAPIAllocateBuffer](mapiallocatebuffer.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[Каноническое свойство PidTagContainerFlags](pidtagcontainerflags-canonical-property.md)
  
[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)


[Mfcmapi (en) � �������� ������� ����](mfcmapi-as-a-code-sample.md)

