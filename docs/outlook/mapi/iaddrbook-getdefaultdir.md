---
title: IAddrBookGetDefaultDir
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
ms.openlocfilehash: a9f0fac76f06bd638aeff89ff096507209cc0287
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22568457"
---
# <a name="iaddrbookgetdefaultdir"></a>IAddrBook::GetDefaultDir

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Возвращает идентификатор записи для контейнер начальной адресной книги.
  
```cpp
HRESULT GetDefaultDir(
  ULONG FAR * lpcbEntryID,
  LPENTRYID FAR * lppEntryID
);
```

## <a name="parameters"></a>Параметры

 _lpcbEntryID_
  
> [out] Указатель на число байтов в идентификатор записи, на который указывает параметр _lppEntryID_ . 
    
 _lppEntryID_
  
> [out] Указатель на указатель на запись идентификатор контейнера по умолчанию.
    
## <a name="return-value"></a>������������ ��������

ЗНАЧЕНИЕ S_OK 
  
> Идентификатор записи по умолчанию контейнера успешно возвращен.
    
## <a name="remarks"></a>Замечания

Клиентские приложения и поставщиков услуг вызовите метод **GetDefaultDir** для получения идентификатора запись контейнер адресной книги по умолчанию. Контейнер по умолчанию является то, что на экране пользователя отображается отображаются в адресной книге, при первом открытии адресной книги. Если контейнер по умолчанию с помощью вызова метода [IAddrBook::SetDefaultDir](iaddrbook-setdefaultdir.md) не задано, MAPI, назначает как контейнер по умолчанию первого контейнера с именами, который не является личная адресная книга (адресной книги). Если не удается найти такие контейнер, личной адресной книги становится контейнера по умолчанию. 
  
По умолчанию каталог, клиента или поставщика вызывается метод **SetDefaultDir** . Клиенты и поставщики не нужно вызвать метод [IMAPIProp::SaveChanges](imapiprop-savechanges.md) ; так как изменения в адресной книге не выполняются, изменения сразу же становятся постоянными. 
  
## <a name="mfcmapi-reference"></a>Справочник по mfcmapi (en)

������ ���� mfcmapi (en) ���������� � ������� ����.
  
|**����**|**�������**|**�����������**|
|:-----|:-----|:-----|
|MainDlg.cpp  <br/> |CMainDlg::OnOpenDefaultDir  <br/> |Mfcmapi (en) использует метод **GetDefaultDir** , чтобы получить идентификатор контейнер адресной книги по умолчанию.  <br/> |
   
## <a name="see-also"></a>См. также



[IAddrBook::SetDefaultDir](iaddrbook-setdefaultdir.md)
  
[MAPIAllocateBuffer](mapiallocatebuffer.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[Каноническое свойство PidTagContainerFlags](pidtagcontainerflags-canonical-property.md)
  
[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)


[Mfcmapi (en) � �������� ������� ����](mfcmapi-as-a-code-sample.md)

