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
ms.openlocfilehash: 734e53c1e897c902c72319aa6f2d3d7af2d23fb6
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431710"
---
# <a name="imsprovidercomparestoreids"></a>IMSProvider::CompareStoreIDs

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Сравнивает два идентификатора записей в хранилище сообщений, чтобы определить, относятся ли они к одному объекту store.
  
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
  
> [in] Размер идентификатора записи в вайтах, на который указывает  параметр _lpEntryID1._
    
 _lpEntryID1_
  
> [in] Указатель на идентификатор первой записи, который необходимо сравнить.
    
 _cbEntryID2_
  
> [in] Размер идентификатора записи в вайтах, на который указывает  параметр _lpEntryID2._
    
 _lpEntryID2_
  
> [in] Указатель на второй идентификатор записи, который необходимо сравнить.
    
 _ulFlags_
  
> [in] ���������������; ������ ���� ����� ����.
    
 _lpulResult_
  
> [out] Указатель на возвращенный результат сравнения. TRUE, если два идентификатора записей ссылаются на один и тот же объект; в противном случае false.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> ����� ������� � ������ ��������� ��������� ��� ��������.
    
## <a name="remarks"></a>Примечания

MAPI вызывает метод **IMSProvider::CompareStoreIDs** при обработке вызова метода [IMAPISession::OpenMsgStore.](imapisession-openmsgstore.md) В этот момент с помощью **compareStoreIDs** определяется, какой раздел профиля (если он имеется) связан с открываемого хранилищем сообщений. Вызов **CompareStoreIDs** можно сделать, если для определенного поставщика хранилища не открыты хранилища сообщений. Кроме того, MAPI также вызывает **CompareStoreIDs** при обработке вызова поставщика магазина к методу [IMAPISupport::OpenProfileSection.](imapisupport-openprofilesection.md) 
  
Идентификаторы записей, сравниваемые **compareStoreIDs,** являются как для библиотеки динамической ссылки текущего поставщика (DLL) текущего поставщика, так и для неподтверченных идентификаторов записей в хранилище. Дополнительные сведения об переносе идентификаторов записей в хранилище см. в документе [IMAPISupport::WrapStoreEntryID.](imapisupport-wrapstoreentryid.md)
  
Сравнение идентификаторов записей полезно, так как объект может иметь несколько допустимых идентификаторов записей. Это может произойти, например, после установки новой версии поставщика store сообщений. 
  
## <a name="see-also"></a>См. также



[IMAPISession::OpenMsgStore](imapisession-openmsgstore.md)
  
[IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md)
  
[IMAPISupport::WrapStoreEntryID](imapisupport-wrapstoreentryid.md)
  
[IMSProvider : IUnknown](imsprovideriunknown.md)

