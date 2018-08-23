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
ms.openlocfilehash: 1f93ee653c9365488432c4e797b171a199c30107
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22583717"
---
# <a name="iaddrbookgetpab"></a>IAddrBook::GetPAB

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Возвращает идентификатор записи контейнера, который используется в качестве Личная адресная книга (адресной книги).
  
```cpp
HRESULT GetPAB(
  ULONG FAR * lpcbEntryID,
  LPENTRYID FAR * lppEntryID
);
```

## <a name="parameters"></a>Параметры

 _lpcbEntryID_
  
> [out] Указатель на число байтов в идентификатор записи, на который указывает параметр _lppEntryID_ . 
    
 _lppEntryID_
  
> [out] Указатель на указатель на идентификатор записи личной адресной книги. Параметр _lppEntryID_ содержит нулевое значение, если контейнер не был определен как личной адресной книги. 
    
## <a name="return-value"></a>������������ ��������

ЗНАЧЕНИЕ S_OK 
  
> Идентификатор записи адресной книги успешно возвращен.
    
## <a name="remarks"></a>Замечания

Клиенты вызовите метод **GetPAB** для извлечения идентификатор записи контейнера обозначены как личной адресной книги. Если не было установлено в профиле адресной книги, MAPI выбирает в качестве личной адресной книги первого контейнера в иерархии адресной книги, обеспечивающий изменения. 
  
## <a name="mfcmapi-reference"></a>Справочник по mfcmapi (en)

������ ���� mfcmapi (en) ���������� � ������� ����.
  
|**����**|**�������**|**�����������**|
|:-----|:-----|:-----|
|MainDlg.cpp  <br/> |CMainDlg::OnOpenPAB  <br/> |Mfcmapi (en) использует метод **GetPAB** для получения идентификатора для пользователя Личная адресная книга.  <br/> |
   
## <a name="see-also"></a>См. также



[MAPIAllocateBuffer](mapiallocatebuffer.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[Каноническое свойство PidTagContainerFlags](pidtagcontainerflags-canonical-property.md)
  
[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)


[Mfcmapi (en) � �������� ������� ����](mfcmapi-as-a-code-sample.md)

