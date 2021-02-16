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

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Сравнивает два идентификатора записей, чтобы определить, относятся ли они к одному объекту. 
  
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

## <a name="parameters"></a>Параметры

 _cbEntryID1_
  
> [in] Количество byte в идентификаторе записи, на который указывает параметр _lpEntryID1._ 
    
 _lpEntryID1_
  
> [in] Указатель на идентификатор первой записи, который необходимо сравнить.
    
 _cbEntryID2_
  
> [in] Количество byte в идентификаторе записи, на который указывает параметр _lpEntryID2._ 
    
 _lpEntryID2_
  
> [in] Указатель на второй идентификатор записи, который необходимо сравнить.
    
 _ulFlags_
  
> [in] ���������������; ������ ���� ����� ����.
    
 _lpulResult_
  
> [out] Указатель на результат сравнения. TRUE, если два идентификатора записей ссылаются на один и тот же объект; в противном случае false.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Сравнение было успешным.
    
MAPI_E_UNKNOWN_ENTRYID 
  
> Один или оба идентификатора записей, указанных в качестве параметров, не ссылаются на допустимые объекты, возможно, из-за того, что они в настоящее время не работают и недоступны.
    
## <a name="remarks"></a>Примечания

Метод **IMAPISupport::CompareEntryIDs** реализован для объектов поддержки адресной книги и поставщика store сообщений. **CompareEntryIDs** сравнивает два идентификатора записей, принадлежащих одному поставщику услуг, чтобы определить, относятся ли они к одному объекту. MAPI извлекает часть [MAPIUID](mapiuid.md) из идентификаторов записей, чтобы определить поставщика услуг, ответственного за объекты. Затем MAPI вызывает метод **CompareEntryIDs** объекта для его логотипа для выполнения сравнения. 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

 **CompareEntryIDs полезен,** так как объект может иметь несколько допустимых идентификаторов записей. Это может произойти, например, после установки новой версии поставщика услуг. 
  
Если **CompareEntryIDs** возвращает ошибку, не принимайте никаких действий на основе результата сравнения. Вместо этого вы можете использовать наиболее емкий подход. **CompareEntryIDs** может привести к сбой, если, например, один или оба идентификатора записи содержат недействительные **структуры MAPIUID.** 
  
## <a name="see-also"></a>См. также



[MAPIUID](mapiuid.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

