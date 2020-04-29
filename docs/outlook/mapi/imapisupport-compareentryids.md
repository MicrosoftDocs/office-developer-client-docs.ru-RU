---
title: имаписуппорткомпаринтридс
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
    
 _лпулресулт_
  
> вышли Указатель на результат сравнения. Значение TRUE, если два идентификатора записи ссылаются на один объект; в противном случае — FALSE.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Сравнение выполнено успешно.
    
MAPI_E_UNKNOWN_ENTRYID 
  
> Один или оба идентификатора записи, указанные в качестве параметров, не ссылаются на допустимые объекты, возможно потому, что они неоткрыты и недоступны.
    
## <a name="remarks"></a>Примечания

Метод **имаписуппорт:: метод compareentryids** реализован для адресных книг и объектов поддержки поставщиков хранилища сообщений. **Метод compareentryids** сравнивает два идентификатора записи, которые принадлежат одному поставщику услуг, чтобы определить, ссылаются ли они на один и тот же объект. MAPI извлекает часть [мапиуид](mapiuid.md) из идентификаторов записей, чтобы определить поставщика услуг, ответственного за объекты. Затем MAPI вызывает метод **метод compareentryids** своего объекта logon для выполнения сравнения. 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

 **Метод compareentryids** полезен, так как объект может иметь несколько допустимых идентификаторов записи. Такая ситуация может возникать, например, после установки новой версии поставщика услуг. 
  
Если **метод compareentryids** возвращает ошибку, не следует предпринимать никаких действий в зависимости от результата сравнения. Вместо этого рекомендуется использовать максимально консервативный подход. **Метод compareentryids** может не работать, если, например, один или оба идентификатора записи содержат недопустимую структуру **мапиуид** . 
  
## <a name="see-also"></a>См. также



[MAPIUID](mapiuid.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

