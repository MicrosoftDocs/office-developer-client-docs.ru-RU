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
ms.openlocfilehash: 3f13a4d278b85ffae33e8f44f3a15eb499fb11b3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808777"
---
# <a name="iaddrbooksetpab"></a>IAddrBook::SetPAB

  
  
**Относится к**: Outlook 
  
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
    
## <a name="return-value"></a>������������ ��������

ЗНАЧЕНИЕ S_OK 
  
> Указанный контейнер установлено как личной адресной книги.
    
## <a name="remarks"></a>Замечания

Клиенты и поставщики услуг вызовите метод **SetPAB** для назначения конкретным контейнером в качестве личной адресной книги. Личной адресной книги является контейнером, состоит из записей, скопированные из других контейнеров, а также новые записи. 
  
Вызов **SetPAB** устанавливает контейнером в качестве личной адресной книги, до этого контейнера становится недоступной или новый контейнер становится адресной книги через следующий вызов **SetPAB**. 
  
Клиенты и поставщики не нужно вызвать метод [IMAPIProp::SaveChanges](imapiprop-savechanges.md) , чтобы сохранить изменение адресной книги. 
  
## <a name="mfcmapi-reference"></a>Справочник по mfcmapi (en)

������ ���� mfcmapi (en) ���������� � ������� ����.
  
|**����**|**�������**|**�����������**|
|:-----|:-----|:-----|
|AbContDlg.cpp  <br/> |CAbContDlg::OnSetPAB  <br/> |Mfcmapi (en) использует метод **SetPAB** для внесите в указанный контейнер адресной книги.  <br/> |
   
## <a name="see-also"></a>См. также



[IAddrBook::GetPAB](iaddrbook-getpab.md)
  
[IAddrBook::GetSearchPath](iaddrbook-getsearchpath.md)
  
[Каноническое свойство PidTagContainerFlags](pidtagcontainerflags-canonical-property.md)
  
[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)


[Mfcmapi (en) � �������� ������� ����](mfcmapi-as-a-code-sample.md)

