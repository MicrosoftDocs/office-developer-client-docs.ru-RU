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
ms.openlocfilehash: 9dbf02fc94519d40431fb6bd493ef8e68df59d11
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22566546"
---
# <a name="imapisupportcompareentryids"></a>IMAPISupport::CompareEntryIDs

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Сравнение двух идентификаторы записей для определения, является ли они ссылаются на тот же объект. 
  
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
  
> [in] Число байтов в идентификатор записи, на который указывает параметр _lpEntryID1_ . 
    
 _lpEntryID1_
  
> [in] Указатель на первый идентификатор записи для сравнения.
    
 _cbEntryID2_
  
> [in] Число байтов в идентификатор записи, на который указывает параметр _lpEntryID2_ . 
    
 _lpEntryID2_
  
> [in] Указатель на второй идентификатор записи для сравнения.
    
 _ulFlags_
  
> [in] ���������������; ������ ���� ����� ����.
    
 _lpulResult_
  
> [out] Указатель на результат сравнения. Значение TRUE, если идентификаторы двух записей ссылаются на тот же объект; в противном случае — FALSE.
    
## <a name="return-value"></a>������������ ��������

ЗНАЧЕНИЕ S_OK 
  
> Сравнение успешно завершена.
    
MAPI_E_UNKNOWN_ENTRYID 
  
> Одно или оба идентификаторы записей, указанный в качестве параметров ссылается на допустимый объекты возможно так как они в настоящее время неоткрытый и недоступен.
    
## <a name="remarks"></a>Замечания

Метод **IMAPISupport::CompareEntryIDs** реализуется для адресной книги и сообщения хранилища поставщика объекты поддержки. **CompareEntryIDs** сравниваются два идентификаторы записей, относящихся к отдельный поставщик услуг для определения, является ли они ссылаются на тот же объект. MAPI выделяет [MAPIUID](mapiuid.md) из идентификаторы записей для определения поставщика услуг, ответственных за объекты. MAPI вызывает метод **CompareEntryIDs** возвращается объект входа в систему для выполнения сравнения. 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

 **CompareEntryIDs** полезен, так как объект может иметь несколько идентификаторов записей. Это может произойти, например, после установки новой версии поставщика услуг. 
  
Если **CompareEntryIDs** возвращает ошибку, не имеет каких-либо действий на основании результатов сравнения. Вместо этого можно использовать самый высокий подход невозможно. **CompareEntryIDs** может оказаться неудачным, если, например один или оба идентификаторы записей содержит недопустимый структуры **MAPIUID** . 
  
## <a name="see-also"></a>См. также



[MAPIUID](mapiuid.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

