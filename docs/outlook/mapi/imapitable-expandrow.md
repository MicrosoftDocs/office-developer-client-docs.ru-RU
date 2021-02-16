---
title: IMAPITableExpandRow
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPITable.ExpandRow
api_type:
- COM
ms.assetid: b96dd8f6-e648-4014-8a1d-ae1da771c439
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 5e2ce756baaefef7bd0028e746b1dbe10756365e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415168"
---
# <a name="imapitableexpandrow"></a>IMAPITable::ExpandRow

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Расширяет категорию свернутой таблицы, добавляя строки заголовков листового или нижнего уровня, принадлежащие этой категории, в представление таблицы.
  
```cpp
HRESULT ExpandRow(
ULONG cbInstanceKey,
LPBYTE pbInstanceKey,
ULONG ulRowCount,
ULONG ulFlags,
LPSRowSet FAR * lppRows,
ULONG FAR * lpulMoreRows
);
```

## <a name="parameters"></a>Параметры

 _cbInstanceKey_
  
> [in] Количество в свойствах PR_INSTANCE_KEY, на которые указывает параметр _pbInstanceKey._ 
    
 _pbInstanceKey_
  
> [in] Указатель на свойство **PR_INSTANCE_KEY** ([PidTagInstanceKey),](pidtaginstancekey-canonical-property.md)которое определяет строку заголовка для категории. 
    
 _ulRowCount_
  
> [in] Максимальное число строк, возвращаемого в _параметре lppRows._ 
    
 _ulFlags_
  
> Зарезервировано; должно быть нулем.
    
 _lppRows_
  
> [out] Указатель на структуру [SRowSet,](srowset.md) получающего первые строки (до  _ulRowCount),_ которые были вставлены в представление таблицы в результате расширения. Эти строки вставляются после строки заголовка, заданной параметром _pbInstanceKey._ Параметр  _lppRows может_ иметь значение NULL, если параметр  _ulRowCount_ имеет нулевое значение. 
    
 _lpulMoreRows_
  
> [out] Указатель на общее количество строк, добавленных в представление таблицы.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Категория была успешно расширена.
    
MAPI_E_NOT_FOUND 
  
> Строка, заданная  _параметром pbInstanceKey,_ не существует. 
    
## <a name="remarks"></a>Примечания

Метод **IMAPITable::ExpandRow** расширяет категорию свернутой таблицы, добавляя строки заголовков листового или нижнего уровня, принадлежащие этой категории, в представление таблицы. В параметре _ulRowCount_ может быть указано ограничение на количество строк, возвращаемого в _параметре lppRows._ Если  _ulRowCount_ имеет значение больше нуля и одна или несколько строк возвращаются в наборе строк, на который указывает  _lppRows,_ положение закладки BOOKMARK_CURRENT перемещается в строку сразу после последней строки в наборе строк.
  
Если _для ulRowCount_ установлено значение 0, запрашивается добавить строки заголовков нулевого или нижнего уровня в категорию или нулевые строки, так как в категории нет строк заголовков конечного или нижнего уровня, положение BOOKMARK_CURRENT устанавливается на строку после строки, заданной _pbInstanceKey._ 
  
## <a name="notes-to-implementers"></a>Примечания для исполнителей

Не создавать уведомления для строк, добавляемой в представление таблицы из-за расширения категории.
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Число строк в наборе строк, на которое указывает параметр  _lppRows,_ не может быть равно числу строк, которые были фактически добавлены в таблицу, а также всему набору строк заголовков конечного или нижнего уровня для категории. Могут возникать ошибки, например недостаточно памяти или число строк в категории, превышающих число, указанное в параметре _ulRowCount._ В любом случае BOOKMARK_CURRENT будет иметь положение в последней возвращаемой строке. Чтобы немедленно получить остальные строки в категории, вызовите [IMAPITable::QueryRows.](imapitable-queryrows.md)
  
Не ожидайте получения уведомления таблицы при смене состояния категории. Можно поддерживать локальный кэш строк, которые можно обновлять с помощью каждого вызова **ExpandRow** **или CollapseRow.** 
  
Дополнительные сведения о классификации таблиц см. в таблице [сортировки и категоризации.](sorting-and-categorization.md)
  
## <a name="mfcmapi-reference"></a>Справочные материалы по MFCMAPI

Пример кода MFCMAPI указан в приведенной ниже таблице.
  
|**Файл**|**Функция**|**Примечание**|
|:-----|:-----|:-----|
|ContentsTableListCtrl.cpp  <br/> |CContentsTableListCtrl::D oExpandCollapse  <br/> |MFCMAPI использует метод **IMAPITable::ExpandRow** для расширения категории свернутой таблицы.  <br/> |
   
## <a name="see-also"></a>См. также



[IMAPITable::CollapseRow](imapitable-collapserow.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)


[Mfcmapi (en) � �������� ������� ����](mfcmapi-as-a-code-sample.md)

