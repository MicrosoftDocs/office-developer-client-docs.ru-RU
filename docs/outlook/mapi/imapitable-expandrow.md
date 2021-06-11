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

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Расширяет категорию обрушения таблицы, добавляя в представление таблицы лист или строки заголовка нижнего уровня, принадлежащие этой категории.
  
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

## <a name="parameters"></a>Parameters

 _cbInstanceKey_
  
> [in] Количество битов в свойстве PR_INSTANCE_KEY, на который указывает параметр _pbInstanceKey._ 
    
 _pbInstanceKey_
  
> [in] Указатель на **свойство PR_INSTANCE_KEY** [(PidTagInstanceKey),](pidtaginstancekey-canonical-property.md)которое определяет строку заголовка для категории. 
    
 _ulRowCount_
  
> [in] Максимальное количество строк, возвращаемых в _параметре lppRows._ 
    
 _ulFlags_
  
> Зарезервировано; должно быть нулевой.
    
 _lppRows_
  
> [вышел] Указатель на структуру [SRowSet,](srowset.md) получающего первые (до  _ulRowCount)_ строки, вставленные в представление таблицы в результате расширения. Эти строки вставляются после строки заголовка, которая определена _параметром pbInstanceKey._ Параметр  _lppRows может_ быть NULL, если  _параметр ulRowCount_ — ноль. 
    
 _lpulMoreRows_
  
> [вышел] Указатель на общее количество строк, добавленных в представление таблицы.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Категория была успешно расширена.
    
MAPI_E_NOT_FOUND 
  
> Строка, определенная  _параметром pbInstanceKey,_ не существует. 
    
## <a name="remarks"></a>Примечания

Метод **IMAPITable::ExpandRow** расширяет категорию обрушения таблицы, добавляя в представление таблицы лист или строки заголовка более низкого уровня, которые относятся к категории. Ограничение количества строк, возвращаемого в _параметре lppRows,_ может быть указано в _параметре ulRowCount._ Если  _значение ulRowCount_ превышает 0, а в наборе строк, на которые указывают  _lppRows,_ возвращается одно или несколько строк, положение закладки BOOKMARK_CURRENT перемещается в строку сразу после последней строки в наборе строк.
  
Если _значение ulRowCount_ установлено на нулевом уровне, запрашивая, чтобы в категорию добавлялись строки с нулевой или нижней строками заголовков, либо возвращались нулевые строки, так как в этой категории нет строки заголовка на уровне листа или нижнего уровня, положение BOOKMARK_CURRENT заданной строкой после строки, идентифицированной _pbInstanceKey._ 
  
## <a name="notes-to-implementers"></a>Примечания для исполнителей

Не создавать уведомления на строках, которые добавляются в представление таблицы из-за расширения категорий.
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Количество строк в наборе строк, на которое указывает параметр  _lppRows,_ может не равняться количеству строк, которые были добавлены в таблицу, всему набору строк заголовка листа или строки заголовка более низкого уровня для категории. Могут возникать ошибки, такие как нехватка памяти или количество строк в категории, превышающих число, указанное в параметре _ulRowCount._ В любом случае BOOKMARK_CURRENT будет позицион BOOKMARK_CURRENT в последней строке. Чтобы немедленно получить остальные строки в этой категории, позвоните [в IMAPITable::QueryRows](imapitable-queryrows.md).
  
Не ожидайте получения уведомления таблицы при смене состояния категории. Можно сохранить локальный кэш строк, которые можно обновить с помощью каждого вызова **ExpandRow** или **CollapseRow.** 
  
Дополнительные сведения о классификации таблиц см. в [рубрике Сортировка и классификация.](sorting-and-categorization.md)
  
## <a name="mfcmapi-reference"></a>Справочные материалы по MFCMAPI

Пример кода MFCMAPI указан в приведенной ниже таблице.
  
|**Файл**|**Функция**|**Примечание**|
|:-----|:-----|:-----|
|ContentsTableListCtrl.cpp  <br/> |CContentsTableListCtrl::D oExpandCollapse  <br/> |MFCMAPI использует **метод IMAPITable::ExpandRow** для расширения категории обрушения таблицы.  <br/> |
   
## <a name="see-also"></a>См. также



[IMAPITable::CollapseRow](imapitable-collapserow.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)


[Mfcmapi (en) � �������� ������� ����](mfcmapi-as-a-code-sample.md)

