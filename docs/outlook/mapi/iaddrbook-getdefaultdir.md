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
ms.openlocfilehash: d9ad74d8ae02a49ee3c222394caedfd571f84b1c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436876"
---
# <a name="iaddrbookgetdefaultdir"></a>IAddrBook::GetDefaultDir

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Возвращает идентификатор записи для начального контейнера адресной книги.
  
```cpp
HRESULT GetDefaultDir(
  ULONG FAR * lpcbEntryID,
  LPENTRYID FAR * lppEntryID
);
```

## <a name="parameters"></a>Parameters

 _lpcbEntryID_
  
> [вышел] Указатель на количество byte в идентификаторе входа, на который указывает параметр _lppEntryID._ 
    
 _lppEntryID_
  
> [вышел] Указатель на указатель на идентификатор входа контейнера по умолчанию.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Идентификатор входа контейнера по умолчанию был успешно возвращен.
    
## <a name="remarks"></a>Примечания

Клиентские приложения и поставщики услуг звонят **методу GetDefaultDir,** чтобы получить идентификатор записи контейнера адресной книги по умолчанию. Контейнер по умолчанию — это то, что пользователь видит в адресной книге при первом открывании адресной книги. Если контейнер по умолчанию не установлен вызовом метода [IAddrBook::SetDefaultDir,](iaddrbook-setdefaultdir.md) MAPI назначает в качестве контейнера по умолчанию первый контейнер с именами, которые не являются личной адресной книгой (PAB). Если такой контейнер не удается найти, PAB становится контейнером по умолчанию. 
  
Чтобы установить каталог по умолчанию, клиент или поставщик вызывает **метод SetDefaultDir.** Клиентам и поставщикам не нужно вызывать [метод IMAPIProp::SaveChanges;](imapiprop-savechanges.md) поскольку изменения в адресной книге не происходят, изменения немедленно вносят в нее. 
  
## <a name="mfcmapi-reference"></a>Справочные материалы по MFCMAPI

Пример кода MFCMAPI указан в приведенной ниже таблице.
  
|**Файл**|**Функция**|**Примечание**|
|:-----|:-----|:-----|
|MainDlg.cpp  <br/> |CMainDlg::OnOpenDefaultDir  <br/> |MFCMAPI использует **метод GetDefaultDir** для получения ID для контейнера адресной книги по умолчанию.  <br/> |
   
## <a name="see-also"></a>См. также



[IAddrBook::SetDefaultDir](iaddrbook-setdefaultdir.md)
  
[MAPIAllocateBuffer](mapiallocatebuffer.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[Каноническое свойство PidTagContainerFlags](pidtagcontainerflags-canonical-property.md)
  
[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)


[Mfcmapi (en) � �������� ������� ����](mfcmapi-as-a-code-sample.md)

