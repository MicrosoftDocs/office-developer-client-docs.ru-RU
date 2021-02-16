---
title: IMsgStoreCompareEntryIDs
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgStore.CompareEntryIDs
api_type:
- COM
ms.assetid: 33d70748-0d3f-4be4-bcb5-7ec048887944
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 2a2439bae79b497f018391983e2c4b03a35eee70
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424254"
---
# <a name="imsgstorecompareentryids"></a>IMsgStore::CompareEntryIDs

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Сравнивает два идентификатора записей, чтобы определить, ссылаются ли они на ту же запись в хранилище сообщений. MAPI передает этот вызов поставщику услуг, только если уникальные идентификаторы (UID) в обоих идентификаторах записей, которые необходимо сравнить, обрабатываются этим поставщиком.
  
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
  
> [in] Количество byte в идентификаторе записи, на который указывает  параметр _lpEntryID1._
    
 _lpEntryID1_
  
> [in] Указатель на идентификатор первой записи, который необходимо сравнить.
    
 _cbEntryID2_
  
> [in] Количество byte в идентификаторе записи, на который указывает  параметр _lpEntryID2._
    
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
  
> Один или оба идентификатора записей, указанных в качестве параметров, не ссылаются на объекты, возможно, потому, что соответствующие объекты в настоящее время не воплены и недоступны.
    
## <a name="remarks"></a>Примечания

Метод **IMsgStore::CompareEntryIDs** сравнивает два идентификатора записей, принадлежащих хранилищу сообщений, чтобы определить, относятся ли они к одному объекту. 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

 **CompareEntryIDs полезен,** так как у объекта может быть несколько допустимого идентификатора записи (например, после установки новой версии поставщика магазина сообщений). 
  
Если **CompareEntryIDs** возвращает ошибку, не принимайте никаких действий на основе результата сравнения. Вместо этого вы можете использовать наиболее емкий подход. **CompareEntryIDs** может привести к сбой, если, например, один или оба идентификатора записи содержат **недопустимый MAPIUID**. 
  
## <a name="mfcmapi-reference"></a>Справочные материалы по MFCMAPI

Пример кода MFCMAPI указан в приведенной ниже таблице.
  
|**Файл**|**Функция**|**Примечание**|
|:-----|:-----|:-----|
|BaseDialog.cpp  <br/> |CBaseDialog::OnCompareEntryIDs  <br/> |MFCMAPI использует метод **IMsgStore::CompareEntryIDs** для сравнения ИД записей.  <br/> |
   
## <a name="see-also"></a>См. также



[MAPIUID](mapiuid.md)
  
[IMsgStore: IMAPIProp](imsgstoreimapiprop.md)


[Mfcmapi (en) � �������� ������� ����](mfcmapi-as-a-code-sample.md)

