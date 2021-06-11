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

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Сравнивает два идентификатора входа в хранилище сообщений, чтобы определить, относятся ли они к одному объекту магазина.
  
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

## <a name="parameters"></a>Parameters

 _cbEntryID1_
  
> [in] Размер в bytes идентификатора записи, на который указывает параметр _lpEntryID1._ 
    
 _lpEntryID1_
  
> [in] Указатель на первый идентификатор записи, который необходимо сравнить.
    
 _cbEntryID2_
  
> [in] Размер в bytes идентификатора записи, на который указывает параметр _lpEntryID2._ 
    
 _lpEntryID2_
  
> [in] Указатель на второй идентификатор записи, который необходимо сравнить.
    
 _ulFlags_
  
> [in] ���������������; ������ ���� ����� ����.
    
 _lpulResult_
  
> [вышел] Указатель на возвращенный результат сравнения. TRUE, если два идентификатора записи относятся к одному объекту; в противном случае FALSE.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> ����� ������� � ������ ��������� ��������� ��� ��������.
    
## <a name="remarks"></a>Примечания

MAPI вызывает **метод IMSProvider::CompareStoreIDs** при обработке вызова метода [IMAPISession::OpenMsgStore.](imapisession-openmsgstore.md) В данный момент для определения того, какой раздел профиля связан с открываемой хранилищем сообщений, **вызвано compareStoreIDs.** Вызов **CompareStoreIDs можно** сделать, если для конкретного поставщика магазинов не открыты магазины сообщений. Кроме того, MAPI также вызывает **CompareStoreIDs** при обработке вызова поставщика магазина в [метод IMAPISupport::OpenProfileSection.](imapisupport-openprofilesection.md) 
  
Идентификаторы записей, сравниваемые **с CompareStoreID,** являются как для библиотеки динамических ссылок текущего поставщика хранения (DLL), так и для идентификаторов входа в хранилище. Дополнительные сведения о идентификаторах входа в магазин для упаковки см. в [книге IMAPISupport::WrapStoreEntryID.](imapisupport-wrapstoreentryid.md)
  
Сравнение идентификаторов записей полезно, так как объект может иметь несколько допустимых идентификаторов записи. Это может произойти, например, после установки новой версии поставщика магазина сообщений. 
  
## <a name="see-also"></a>См. также



[IMAPISession::OpenMsgStore](imapisession-openmsgstore.md)
  
[IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md)
  
[IMAPISupport::WrapStoreEntryID](imapisupport-wrapstoreentryid.md)
  
[IMSProvider : IUnknown](imsprovideriunknown.md)

