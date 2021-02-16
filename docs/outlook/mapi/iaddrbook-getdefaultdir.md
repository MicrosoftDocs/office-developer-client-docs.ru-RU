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

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Возвращает идентификатор записи для исходного контейнера адресной книги.
  
```cpp
HRESULT GetDefaultDir(
  ULONG FAR * lpcbEntryID,
  LPENTRYID FAR * lppEntryID
);
```

## <a name="parameters"></a>Параметры

 _lpcbEntryID_
  
> [out] Указатель на количество byte в идентификаторе записи, на который указывает параметр _lppEntryID._ 
    
 _lppEntryID_
  
> [out] Указатель на указатель на идентификатор записи контейнера по умолчанию.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Идентификатор записи контейнера по умолчанию был успешно возвращен.
    
## <a name="remarks"></a>Примечания

Клиентские приложения и поставщики услуг звонят **методу GetDefaultDir,** чтобы получить идентификатор записи контейнера адресной книги по умолчанию. Контейнер по умолчанию — это то, что пользователь видит в адресной книге при первом открытие адресной книги. Если контейнер по умолчанию не был установлен вызовом метода [IAddrBook::SetDefaultDir,](iaddrbook-setdefaultdir.md) MAPI назначает в качестве контейнера по умолчанию первый контейнер с именами, которые не являются личной адресной книгой (PAB). Если такой контейнер не найден, то PAB становится контейнером по умолчанию. 
  
Чтобы установить каталог по умолчанию, клиент или поставщик вызывает метод **SetDefaultDir.** Клиентам и поставщикам не нужно вызывать метод [IMAPIProp::SaveChanges;](imapiprop-savechanges.md) так как изменения в адресной книге не будут внесены, изменения сразу же будут внесены без изменений. 
  
## <a name="mfcmapi-reference"></a>Справочные материалы по MFCMAPI

Пример кода MFCMAPI указан в приведенной ниже таблице.
  
|**Файл**|**Функция**|**Примечание**|
|:-----|:-----|:-----|
|MainDlg.cpp  <br/> |CMainDlg::OnOpenDefaultDir  <br/> |MFCMAPI использует метод **GetDefaultDir** для получения ИД контейнера адресной книги по умолчанию.  <br/> |
   
## <a name="see-also"></a>См. также



[IAddrBook::SetDefaultDir](iaddrbook-setdefaultdir.md)
  
[MAPIAllocateBuffer](mapiallocatebuffer.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[Каноническое свойство PidTagContainerFlags](pidtagcontainerflags-canonical-property.md)
  
[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)


[Mfcmapi (en) � �������� ������� ����](mfcmapi-as-a-code-sample.md)

