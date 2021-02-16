---
title: IMAPISessionCompareEntryIDs
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISession.CompareEntryIDs
api_type:
- COM
ms.assetid: 319f10e9-db8d-4d16-aa1f-6cf5fef493eb
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 4dfde82aa843072168288f4e0b0084dfccd5cd2b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427817"
---
# <a name="imapisessioncompareentryids"></a>IMAPISession::CompareEntryIDs

  
  
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
  
> Один или оба идентификатора записей, указанных в качестве параметров, не ссылаются на объекты, возможно, из-за того, что эти объекты в настоящее время не работают и недоступны.
    
## <a name="remarks"></a>Примечания

Метод **IMAPISession::CompareEntryIDs** сравнивает два идентификатора записей, принадлежащих одному поставщику услуг, чтобы определить, ссылаются ли они на один и тот же объект. MAPI извлекает часть [MAPIUID](mapiuid.md) из идентификаторов записей, чтобы определить поставщика услуг, ответственного за объекты, а затем вызывает метод **CompareEntryIDs** объекта входа для выполнения сравнения. 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Метод **CompareEntryIDs полезен,** так как объект может иметь несколько допустимого идентификатора записи. Это может произойти, например, после установки новой версии поставщика услуг. 
  
Если **CompareEntryIDs** возвращает ошибку, не принимайте никаких действий на основе результата сравнения. Вместо этого вы можете использовать наиболее емкий подход. **CompareEntryIDs** может привести к сбой, если, например, один или оба идентификатора записи содержат **недопустимый MAPIUID**. 
  
## <a name="mfcmapi-reference"></a>Справочные материалы по MFCMAPI

Пример кода MFCMAPI указан в приведенной ниже таблице.
  
|**Файл**|**Функция**|**Примечание**|
|:-----|:-----|:-----|
|BaseDialog.cpp  <br/> |CbaseDialog::OnCompareEntryIDs  <br/> |MFCMAPI использует метод **IMAPISession::CompareEntryIDs** для сравнения двух входных данных, которые вводит пользователь.  <br/> |
   
## <a name="see-also"></a>См. также



[MAPIUID](mapiuid.md)
  
[IMAPISession: IUnknown](imapisessioniunknown.md)


[Mfcmapi (en) � �������� ������� ����](mfcmapi-as-a-code-sample.md)

