---
title: IAddrBookSetPAB
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
ms.openlocfilehash: 461b59ff4f4c8a93f3a9945b05e31aef9a2997bf
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22569304"
---
# <a name="iaddrbooksetpab"></a>IAddrBook::SetPAB

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Назначает конкретным контейнером Личная адресная книга (адресной книги).
  
```cpp
HRESULT SetPAB(
  ULONG cbEntryID,
  LPENTRYID lpEntryID
);
```

## <a name="parameters"></a>Параметры

 _cbEntryID_
  
> [in] Число байтов в идентификатор записи, на который указывает параметр _lpEntryID_ . 
    
 _lpEntryID_
  
> [in] Указатель на идентификатор записи контейнера в качестве личной адресной книги. Параметр _lpEntryID_ не может быть NULL. 
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Указанный контейнер установлено как личной адресной книги.
    
## <a name="remarks"></a>Замечания

Клиенты и поставщики услуг вызовите метод **SetPAB** для назначения конкретным контейнером в качестве личной адресной книги. Личной адресной книги является контейнером, состоит из записей, скопированные из других контейнеров, а также новые записи. 
  
Вызов **SetPAB** устанавливает контейнером в качестве личной адресной книги, до этого контейнера становится недоступной или новый контейнер становится адресной книги через следующий вызов **SetPAB**. 
  
Клиенты и поставщики не нужно вызвать метод [IMAPIProp::SaveChanges](imapiprop-savechanges.md) , чтобы сохранить изменение адресной книги. 
  
## <a name="mfcmapi-reference"></a>Справочные материалы по MFCMAPI

Пример кода MFCMAPI указан в приведенной ниже таблице.
  
|**Файл**|**Функция**|**Примечание**|
|:-----|:-----|:-----|
|AbContDlg.cpp  <br/> |CAbContDlg::OnSetPAB  <br/> |Mfcmapi (en) использует метод **SetPAB** для внесите в указанный контейнер адресной книги.  <br/> |
   
## <a name="see-also"></a>См. также



[IAddrBook::GetPAB](iaddrbook-getpab.md)
  
[IAddrBook::GetSearchPath](iaddrbook-getsearchpath.md)
  
[Каноническое свойство PidTagContainerFlags](pidtagcontainerflags-canonical-property.md)
  
[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)


[Mfcmapi (en) � �������� ������� ����](mfcmapi-as-a-code-sample.md)

