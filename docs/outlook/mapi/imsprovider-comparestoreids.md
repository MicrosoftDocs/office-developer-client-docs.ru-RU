---
title: IMSProviderCompareStoreIDs
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMSProvider.CompareStoreIDs
api_type:
- COM
ms.assetid: c3e3cfaa-9c4a-482a-9411-9c4ab01d312f
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 9905a4e972f0e599629aac74b6fbc8bae06c93b0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809426"
---
# <a name="imsprovidercomparestoreids"></a>IMSProvider::CompareStoreIDs

  
  
**Относится к**: Outlook 
  
Сравнение двух сообщений идентификаторы хранилища записей для определения, является ли они ссылаются на тот же объект хранилища.
  
```cpp
HRESULT CompareStoreIDs(
  ULONG cbEntryID1,
  LPENTRYID lpEntryID1,
  ULONG cbEntryID2,
  LPENTRYID lpEntryID2,
  ULONG ulFlags,
  ULONG FAR * lpulResult
);
```

## <a name="parameters"></a>Параметры

 _cbEntryID1_
  
> [in] Указывает размер в байтах, идентификатор записи с помощью параметра _lpEntryID1_ _._
    
 _lpEntryID1_
  
> [in] Указатель на первый идентификатор записи для сравнения.
    
 _cbEntryID2_
  
> [in] Указывает размер в байтах, идентификатор записи с помощью параметра _lpEntryID2_ _._
    
 _lpEntryID2_
  
> [in] Указатель на второй идентификатор записи для сравнения.
    
 _ulFlags_
  
> [in] ���������������; ������ ���� ����� ����.
    
 _lpulResult_
  
> [out] Указатель на возвращаемый результат сравнения. Значение TRUE, если идентификаторы двух записей ссылаются на тот же объект; в противном случае — FALSE.
    
## <a name="return-value"></a>������������ ��������

ЗНАЧЕНИЕ S_OK 
  
> ����� ������� � ������ ��������� ��������� ��� ��������.
    
## <a name="remarks"></a>���������

MAPI вызывает метод **IMSProvider::CompareStoreIDs** при обработке вызова метода [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md) . На этом этапе вызывает **CompareStoreIDs** для определения, какие раздела профиля при их наличии, связанного с хранилищем сообщений их открытием. Вызов **CompareStoreIDs** может быть выполнен, когда нет хранилищ сообщений открыты для конкретного хранилища поставщика. В дополнение к этому MAPI также вызывает **CompareStoreIDs** при обработке вызова поставщика хранилища в метод [IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md) . 
  
Идентификаторы записей, по сравнению с **CompareStoreIDs** являются оба для текущего хранения поставщика библиотеки динамической компоновки (DLL) и являются оба идентификаторы развернуть хранилища записей. Дополнительные сведения о перенос идентификаторы хранилища записей можно [IMAPISupport::WrapStoreEntryID](imapisupport-wrapstoreentryid.md).
  
Сравнение идентификаторы записей полезен, так как объект может иметь несколько идентификаторов записей. Это может произойти, например, после установки новой версии поставщика хранилища сообщений. 
  
## <a name="see-also"></a>См. также



[IMAPISession::OpenMsgStore](imapisession-openmsgstore.md)
  
[IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md)
  
[IMAPISupport::WrapStoreEntryID](imapisupport-wrapstoreentryid.md)
  
[IMSProvider : IUnknown](imsprovideriunknown.md)

