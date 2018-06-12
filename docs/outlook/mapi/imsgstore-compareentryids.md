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
description: '���� ���������� ���������: 9 ����� 2015 �.'
ms.openlocfilehash: a1c5cdc67bc64f20dd8ba0a5e8682c5e2f97294f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809374"
---
# <a name="imsgstorecompareentryids"></a>IMsgStore::CompareEntryIDs

  
  
**Применимо к**: Outlook 
  
Сравнение двух идентификаторы записей для определения, является ли они ссылаются на той же операции в банке сообщений. MAPI передает этот вызов к поставщику услуг только в том случае, если уникальных идентификаторов (UID) в обоих идентификаторы записей для сравнения обрабатываются этого поставщика.
  
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
  
> [in] Число байтов в идентификатор записи, на который указывает параметр _lpEntryID1_ _._
    
 _lpEntryID1_
  
> [in] Указатель на первый идентификатор записи для сравнения.
    
 _cbEntryID2_
  
> [in] Число байтов в идентификатор записи, на который указывает параметр _lpEntryID2_ _._
    
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
  
> Одна или обе идентификаторы записей, указанный в качестве параметров относится к объектам, возможно из-за соответствующими объектами неоткрытый и недоступен в представление.
    
## <a name="remarks"></a>Замечания

Метод **IMsgStore::CompareEntryIDs** сравнивает два идентификаторы записей, относящихся к хранилище сообщений, чтобы определить, является ли они ссылаются на тот же объект. 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

 **CompareEntryIDs** полезен, так как объект может иметь несколько идентификаторов записей (например, после установки новой версии поставщика хранилища сообщений). 
  
Если **CompareEntryIDs** возвращает ошибку, не имеет каких-либо действий на основании результатов сравнения. Вместо этого можно использовать самый высокий подход невозможно. **CompareEntryIDs** может оказаться неудачным, если, например один или оба идентификаторы записей содержит недопустимый **MAPIUID**. 
  
## <a name="mfcmapi-reference"></a>Справочник по mfcmapi (en)

������ ���� mfcmapi (en) ���������� � ������� ����.
  
|**����**|**�������**|**�����������**|
|:-----|:-----|:-----|
|BaseDialog.cpp  <br/> |CBaseDialog::OnCompareEntryIDs  <br/> |Mfcmapi (en) использует метод **IMsgStore::CompareEntryIDs** для сравнения запись идентификаторы.  <br/> |
   
## <a name="see-also"></a>См. также



[MAPIUID](mapiuid.md)
  
[IMsgStore: IMAPIProp](imsgstoreimapiprop.md)


[Mfcmapi (en) � �������� ������� ����](mfcmapi-as-a-code-sample.md)

