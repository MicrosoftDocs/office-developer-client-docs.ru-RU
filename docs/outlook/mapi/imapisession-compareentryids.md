---
title: Имаписессионкомпаринтридс
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
  
Сравнивает два идентификатора записи, чтобы определить, ссылаются ли они на один и тот же объект. 
  
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
  
> возврата Число байтов в идентификаторе записи, на которое указывает параметр _lpEntryID1_ . 
    
 _lpEntryID1_
  
> возврата Указатель на первый идентификатор записи, который необходимо сравнить.
    
 _cbEntryID2_
  
> возврата Число байтов в идентификаторе записи, на которое указывает параметр _lpEntryID2_ . 
    
 _lpEntryID2_
  
> возврата Указатель на второй идентификатор записи, который необходимо сравнить.
    
 _ulFlags_
  
> [in] ���������������; ������ ���� ����� ����.
    
 _Лпулресулт_
  
> вышли Указатель на результат сравнения. ЗНАЧЕНИЕ TRUE, если два идентификатора записи ссылаются на один объект; в противном случае — FALSE.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Сравнение выполнено успешно.
    
МАПИ_Е_УНКНОВН_ЕНТРИД 
  
> Один или оба идентификатора записи, указанные как параметры, не ссылаются на объекты, возможно, из-за того, что эти объекты в данный момент неоткрыты и недоступны.
    
## <a name="remarks"></a>Примечания

Метод **IMAPISession:: метод compareentryids** сравнивает два идентификатора записи, которые принадлежат одному поставщику услуг, чтобы определить, ссылаются ли они на один и тот же объект. MAPI извлекает часть [мапиуид](mapiuid.md) из идентификаторов записей, чтобы определить поставщика услуг, ответственного за объекты, а затем вызывает метод **метод compareentryids** объекта logon для выполнения сравнения. 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Метод **метод compareentryids** полезен, так как объект может иметь несколько допустимых идентификаторов записи. Такая ситуация может возникать, например, после установки новой версии поставщика услуг. 
  
Если **метод compareentryids** возвращает ошибку, не следует предпринимать никаких действий в зависимости от результата сравнения. Вместо этого рекомендуется использовать максимально консервативный подход. **Метод compareentryids** может не работать, если, например, один или оба идентификатора записи содержат недопустимый **мапиуид**. 
  
## <a name="mfcmapi-reference"></a>Справочные материалы по MFCMAPI

Пример кода MFCMAPI указан в приведенной ниже таблице.
  
|**Файл**|**Функция**|**Примечание**|
|:-----|:-----|:-----|
|Баседиалог. cpp  <br/> |Кбаседиалог:: Онкомпаринтридс  <br/> |MFCMAPI использует метод **IMAPISession:: метод compareentryids** для сравнения двух идентификаторов записей, вводимых пользователем.  <br/> |
   
## <a name="see-also"></a>См. также



[MAPIUID](mapiuid.md)
  
[IMAPISession: IUnknown](imapisessioniunknown.md)


[Mfcmapi (en) � �������� ������� ����](mfcmapi-as-a-code-sample.md)

