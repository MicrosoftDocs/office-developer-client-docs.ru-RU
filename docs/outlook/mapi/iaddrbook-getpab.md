---
title: IAddrBookGetPAB
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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419900"
---
# <a name="iaddrbookgetpab"></a>IAddrBook::GetPAB

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Возвращает идентификатор входа контейнера, назначенного в качестве личной адресной книги (PAB).
  
```cpp
HRESULT GetPAB(
  ULONG FAR * lpcbEntryID,
  LPENTRYID FAR * lppEntryID
);
```

## <a name="parameters"></a>Parameters

 _lpcbEntryID_
  
> [вышел] Указатель на количество byte в идентификаторе входа, на который указывает параметр _lppEntryID._ 
    
 _lppEntryID_
  
> [вышел] Указатель на указатель на идентификатор записи PAB. Параметр  _lppEntryID содержит_ ноль, если контейнер не назначен как PAB. 
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Идентификатор записи PAB был успешно возвращен.
    
## <a name="remarks"></a>Примечания

Клиенты звонят **методу GetPAB,** чтобы получить идентификатор входа контейнера, назначенного как PAB. Если PAB не установлен в профиле, MAPI выбирает в качестве PAB первый контейнер в иерархии адресной книги, который позволяет вносить изменения. 
  
## <a name="mfcmapi-reference"></a>Справочные материалы по MFCMAPI

Пример кода MFCMAPI указан в приведенной ниже таблице.
  
|**Файл**|**Функция**|**Примечание**|
|:-----|:-----|:-----|
|MainDlg.cpp  <br/> |CMainDlg::OnOpenPAB  <br/> |MFCMAPI использует **метод GetPAB** для получения ID для личной адресной книги пользователя.  <br/> |
   
## <a name="see-also"></a>См. также



[MAPIAllocateBuffer](mapiallocatebuffer.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[Каноническое свойство PidTagContainerFlags](pidtagcontainerflags-canonical-property.md)
  
[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)


[Mfcmapi (en) � �������� ������� ����](mfcmapi-as-a-code-sample.md)

