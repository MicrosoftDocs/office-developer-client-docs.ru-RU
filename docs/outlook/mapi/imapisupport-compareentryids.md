---
title: IMAPISupportCompareEntryIDs
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.CompareEntryIDs
api_type:
- COM
ms.assetid: be6991d9-6353-4838-bc6b-39de51a94d8d
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 6c79943792c8c17ee007c39b5c5c215a6fbc0699
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431045"
---
# <a name="imapisupportcompareentryids"></a>IMAPISupport::CompareEntryIDs

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Сравнивает два идентификатора записи, чтобы определить, относятся ли они к одному объекту. 
  
```cpp
HRESULT CompareEntryIDs(
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
  
> [in] Количество byte в идентификаторе входа, на который указывает параметр _lpEntryID1._ 
    
 _lpEntryID1_
  
> [in] Указатель на первый идентификатор записи, который необходимо сравнить.
    
 _cbEntryID2_
  
> [in] Количество byte в идентификаторе входа, на который указывает параметр _lpEntryID2._ 
    
 _lpEntryID2_
  
> [in] Указатель на второй идентификатор записи, который необходимо сравнить.
    
 _ulFlags_
  
> [in] ���������������; ������ ���� ����� ����.
    
 _lpulResult_
  
> [вышел] Указатель на результат сравнения. TRUE, если два идентификатора записи относятся к одному объекту; в противном случае FALSE.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Сравнение было успешным.
    
MAPI_E_UNKNOWN_ENTRYID 
  
> Один или оба идентификатора записи, указанных в качестве параметров, не относятся к допустимым объектам, возможно, потому, что они в настоящее время не были отперты и недоступны.
    
## <a name="remarks"></a>Примечания

Метод **IMAPISupport::CompareEntryIDs** реализован для объектов поддержки поставщиков адресной книги и магазина сообщений. **CompareEntryIDs** сравнивает два идентификатора записи, принадлежащих одному поставщику услуг, чтобы определить, относятся ли они к одному объекту. MAPI извлекает часть [MAPIUID](mapiuid.md) из идентификаторов записи, чтобы определить поставщика услуг, ответственного за объекты. Затем MAPI вызывает метод **CompareEntryIDs** объекта с логотипом для выполнения сравнения. 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

 **CompareEntryIDs полезен,** так как объект может иметь несколько допустимых идентификаторов записи. Такая ситуация может возникнуть, например, после установки новой версии поставщика услуг. 
  
Если **compareEntryIDs** возвращает ошибку, не принимайте никаких действий в зависимости от результата сравнения. Вместо этого примите наиболее консервативный подход. **CompareEntryIDs может** привести к сбой, если, например, один или оба идентификатора записи содержат недействительные **структуры MAPIUID.** 
  
## <a name="see-also"></a>См. также



[MAPIUID](mapiuid.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

