---
title: IMAPITableQueryColumns
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPITable.QueryColumns
api_type:
- COM
ms.assetid: d6341acc-c6ca-4605-93af-77230040339d
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 86dfaa8fbc9ff24d38472f1339a22534086d890b
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22593748"
---
# <a name="imapitablequerycolumns"></a>IMAPITable::QueryColumns

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Возвращает список столбцов для таблицы.
  
```cpp
HRESULT QueryColumns(
ULONG ulFlags,
LPSPropTagArray FAR * lpPropTagArray
);
```

## <a name="parameters"></a>���������

 _ulFlags_
  
> [in] Битовая маска флаги, которое указывает, какой столбец значение должны быть возвращены. Можно задать следующий флаг:
    
TBL_ALL_COLUMNS 
  
> В таблице должен возвращать все доступные столбцы.
    
 _lpPropTagArray_
  
> [out] Установите указатель на структуру [SPropTagArray](sproptagarray.md) , содержащий свойства тегов для столбца. 
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Набор столбцов успешно возвращен.
    
MAPI_E_BUSY 
  
> Другой операции в процессе выполнения, не позволяющей столбце устанавливается операции извлечения запуск. В процессе выполнения операции должны выполнить либо должна быть остановлена.
    
## <a name="remarks"></a>Замечания

Метод **IMAPITable::QueryColumns** может вызываться для извлечения: 
  
- По умолчанию набор столбцов для таблицы.
    
- Текущий набор столбцов для таблицы, в соответствии с параметром вызов метода [IMAPITable::SetColumns](imapitable-setcolumns.md) . 
    
- Полный набор столбцов для таблицы, столбцы, которые доступны, но не обязательно частью текущего набора.
    
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Если флаг TBL_ALL_COLUMNS не задано, **IMAPITable::QueryColumns** возвращает таблицы по умолчанию либо текущий набор столбцов, в зависимости от того, является ли изменяет таблицы с помощью вызова **IMAPITable::SetColumns**. **Метода SetColumns** изменяет порядок и выбор столбцов в набор столбцов таблицы. 
  
Если установлен флаг TBL_ALL_COLUMNS, **QueryColumns** возвращает все столбцы, которые могут находиться в набор столбцов в таблице. 
  
Освободите память для массива свойства tag указывает параметр _lpPropTagArray_ путем вызова функции [MAPIFreeBuffer](mapifreebuffer.md) . 
  
## <a name="mfcmapi-reference"></a>Справочные материалы по MFCMAPI

Пример кода MFCMAPI указан в приведенной ниже таблице.
  
|**Файл**|**Функция**|**Примечание**|
|:-----|:-----|:-----|
|ContentsTableListCtrl.cpp  <br/> |CContentsTableListCtrl::DoSetColumns  <br/> |Mfcmapi (en) используется метод **IMAPITable::QueryColumns** для получения текущего набор столбцов для таблицы, пользователь может изменять его.  <br/> |
   
## <a name="see-also"></a>См. также



[IMAPITable::SetColumns](imapitable-setcolumns.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[SPropTagArray](sproptagarray.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)


[Mfcmapi (en) � �������� ������� ����](mfcmapi-as-a-code-sample.md)

