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

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Возвращает список столбцов для таблицы.
  
```cpp
HRESULT QueryColumns(
ULONG ulFlags,
LPSPropTagArray FAR * lpPropTagArray
);
```

## <a name="parameters"></a>Parameters

 _ulFlags_
  
> [in] Bitmask флагов, которые указывают, какой столбец должен быть возвращен. Можно установить следующий флаг:
    
TBL_ALL_COLUMNS 
  
> В таблице должны быть возвращены все доступные столбцы.
    
 _lpPropTagArray_
  
> [вышел] Указатель на [структуру SPropTagArray,](sproptagarray.md) содержащую теги свойств для набора столбцов. 
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Набор столбцов был успешно возвращен.
    
MAPI_E_BUSY 
  
> В настоящее время продолжается еще одна операция, которая не позволяет начать операцию набора столбцов для ирисовки. Либо операция должна быть разрешена к завершению, либо она должна быть остановлена.
    
## <a name="remarks"></a>Примечания

Метод **IMAPITable::QueryColumns** может быть вызван для получения: 
  
- Столбец по умолчанию, установленный для таблицы.
    
- Текущий столбец для таблицы, установленный вызовом метода [IMAPITable::SetColumns.](imapitable-setcolumns.md) 
    
- Полный столбец, заданный для таблицы, столбцы, которые доступны, но необязательно являются частью текущего набора.
    
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Если флаг TBL_ALL_COLUMNS, **IMAPITable::QueryColumns** возвращает по умолчанию или текущему набору столбцов таблицы в зависимости от того, повлияла ли на таблицу вызов **IMAPITable::SetColumns**. **SetColumns** изменяет порядок и выбор столбцов в наборе столбцов таблицы. 
  
Если задайте флаг TBL_ALL_COLUMNS, **QueryColumns** возвращает все столбцы, которые могут быть в столбце таблицы. 
  
Освободите память для массива тегов свойств, на который указывает параметр _lpPropTagArray,_ назвав [функцию MAPIFreeBuffer.](mapifreebuffer.md) 
  
## <a name="mfcmapi-reference"></a>Справочные материалы по MFCMAPI

Пример кода MFCMAPI указан в приведенной ниже таблице.
  
|**Файл**|**Функция**|**Примечание**|
|:-----|:-----|:-----|
|ContentsTableListCtrl.cpp  <br/> |CContentsTableListCtrl::D SetColumns  <br/> |MFCMAPI использует метод **IMAPITable::QueryColumns** для получения текущего набора столбцов для таблицы, чтобы пользователь может изменить его.  <br/> |
   
## <a name="see-also"></a>См. также



[IMAPITable::SetColumns](imapitable-setcolumns.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[SPropTagArray](sproptagarray.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)


[Mfcmapi (en) � �������� ������� ����](mfcmapi-as-a-code-sample.md)

