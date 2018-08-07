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
ms.openlocfilehash: df6347298aab5404ec69bd9ac876863e31b741d0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809075"
---
# <a name="imapisessioncompareentryids"></a>IMAPISession::CompareEntryIDs

  
  
**Относится к**: Outlook 
  
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
  
> Одно или оба идентификаторы записей, указанный в качестве параметров относится к объектам, возможно из-за этих объектов в настоящее время неоткрытый и недоступен.
    
## <a name="remarks"></a>Замечания

Метод **IMAPISession::CompareEntryIDs** сравнивает два идентификаторы записей, относящихся к отдельный поставщик услуг для определения, является ли они ссылаются на тот же объект. MAPI выделяет [MAPIUID](mapiuid.md) из идентификаторы записей для определения поставщика услуг, ответственных за объекты и затем вызывает метод **CompareEntryIDs** возвращается объект входа в систему для выполнения сравнения. 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Метод **CompareEntryIDs** полезен, так как объект может иметь несколько идентификаторов записей. Это может произойти, например, после установки новой версии поставщика услуг. 
  
Если **CompareEntryIDs** возвращает ошибку, не имеет каких-либо действий на основании результатов сравнения. Вместо этого можно использовать самый высокий подход невозможно. **CompareEntryIDs** может оказаться неудачным, если, например один или оба идентификаторы записей содержит недопустимый **MAPIUID**. 
  
## <a name="mfcmapi-reference"></a>Справочник по mfcmapi (en)

������ ���� mfcmapi (en) ���������� � ������� ����.
  
|**����**|**�������**|**�����������**|
|:-----|:-----|:-----|
|BaseDialog.cpp  <br/> |CbaseDialog::OnCompareEntryIDs  <br/> |Mfcmapi (en) использует метод **IMAPISession::CompareEntryIDs** для сравнения двух идентификаторы, которые пользователь вводит.  <br/> |
   
## <a name="see-also"></a>См. также



[MAPIUID](mapiuid.md)
  
[IMAPISession: IUnknown](imapisessioniunknown.md)


[Mfcmapi (en) � �������� ������� ����](mfcmapi-as-a-code-sample.md)

