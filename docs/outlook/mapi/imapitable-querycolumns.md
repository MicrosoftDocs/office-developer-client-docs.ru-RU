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
ms.openlocfilehash: d142e19fc4721cec4dde0df7fc030a001121da63
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410107"
---
# <a name="imapitablequerycolumns"></a>IMAPITable::QueryColumns

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Возвращает список столбцов для таблицы.
  
```cpp
HRESULT QueryColumns(
ULONG ulFlags,
LPSPropTagArray FAR * lpPropTagArray
);
```

## <a name="parameters"></a>Параметры

 _ulFlags_
  
> [in] Битоваяmas флагов, которая указывает, какой набор столбцов должен быть возвращен. Можно установить следующий флаг:
    
TBL_ALL_COLUMNS 
  
> Таблица должна возвращать все доступные столбцы.
    
 _lpPropTagArray_
  
> [out] Указатель на [структуру SPropTagArray,](sproptagarray.md) содержащую теги свойств для набора столбцов. 
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Набор столбцов был успешно возвращен.
    
MAPI_E_BUSY 
  
> В настоящее время идет другая операция, которая не позволяет начать операцию иниации набора столбцов. Либо операция должна быть разрешена для завершения, либо она должна быть остановлена.
    
## <a name="remarks"></a>Примечания

Метод **IMAPITable::QueryColumns** можно использовать для получения: 
  
- Набор столбцов по умолчанию для таблицы.
    
- Текущий столбец, задаемый для таблицы, как установлен вызовом метода [IMAPITable::SetColumns.](imapitable-setcolumns.md) 
    
- Полный набор столбцов для таблицы, столбцов, которые доступны, но не обязательно являются частью текущего набора.
    
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Если флаг TBL_ALL_COLUMNS не установлен, **IMAPITable::QueryColumns** возвращает набор столбцов по умолчанию или текущий набор столбцов таблицы в зависимости от того, был ли затронут вызов **IMAPITable::SetColumns**. **SetColumns** изменяет порядок и выбор столбцов в наборе столбцов таблицы. 
  
Если установлен флаг TBL_ALL_COLUMNS, **QueryColumns** возвращает все столбцы, которые могут быть в наборе столбцов таблицы. 
  
Освободите память для массива тегов свойств, на который указывает параметр _lpPropTagArray,_ путем вызова функции [MAPIFreeBuffer.](mapifreebuffer.md) 
  
## <a name="mfcmapi-reference"></a>Справочные материалы по MFCMAPI

Пример кода MFCMAPI указан в приведенной ниже таблице.
  
|**Файл**|**Функция**|**Примечание**|
|:-----|:-----|:-----|
|ContentsTableListCtrl.cpp  <br/> |CContentsTableListCtrl::D oSetColumns  <br/> |MFCMAPI использует метод **IMAPITable::QueryColumns** для получения текущего набора столбцов для таблицы, чтобы пользователь может изменить его.  <br/> |
   
## <a name="see-also"></a>См. также



[IMAPITable::SetColumns](imapitable-setcolumns.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[SPropTagArray](sproptagarray.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)


[Mfcmapi (en) � �������� ������� ����](mfcmapi-as-a-code-sample.md)

