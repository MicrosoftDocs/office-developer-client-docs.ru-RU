---
title: IMAPITableCollapseRow
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPITable.CollapseRow
api_type:
- COM
ms.assetid: 1a23e555-be26-43fb-a715-cfc4ffa623cd
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: e6a180ceb325a705ebf226bb728c52cce7396490
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416176"
---
# <a name="imapitablecollapserow"></a>IMAPITable::CollapseRow

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Свернет категорию расширенной таблицы, удалив все заголовки нижнего уровня и строки листов, принадлежащие этой категории, из представления таблицы.
  
```cpp
HRESULT CollapseRow(
ULONG cbInstanceKey,
LPBYTE pbInstanceKey,
ULONG ulFlags,
ULONG FAR * lpulRowCount
);
```

## <a name="parameters"></a>Параметры

 _cbInstanceKey_
  
> [in] Количество в свойствах PR_INSTANCE_KEY, на которые указывает параметр _pbInstanceKey._ 
    
 _pbInstanceKey_
  
> [in] Указатель на свойство **PR_INSTANCE_KEY** ([PidTagInstanceKey),](pidtaginstancekey-canonical-property.md)которое определяет строку заголовка для категории. 
    
 _ulFlags_
  
> Зарезервировано; должно быть нулем.
    
 _lpulRowCount_
  
> [out] Указатель на общее количество строк, которые удаляются из представления таблицы.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Операция свернуть успешно.
    
MAPI_E_NOT_FOUND 
  
> Строка, заданная  _параметром pbInstanceKey,_ не существует. 
    
MAPI_E_INVALID_ENTRYID 
  
> Строка, заданная  _параметром pbInstanceKey,_ не существует. Эта ошибка является альтернативой MAPI_E_NOT_FOUND; поставщики услуг могут вернуть один из них. 
    
## <a name="remarks"></a>Примечания

Метод **IMAPITable::CollapseRow** свергает категорию таблицы и удаляет ее из представления таблицы. Строки свернуты, начиная со строки, заданной свойством **PR_INSTANCE_KEY,** на который указывает параметр _pbInstanceKey._ Количество строк, которые удаляются из представления, возвращается в содержимом параметра _lpulRowCount._ 
  
Уведомления никогда не создаются для строк таблиц, которые удаляются из представления в результате операции свернуть. 
  
Когда строка, определяемая закладкой, свернута из представления, закладка перемещается, чтобы указать на следующую видимую строку. 
  
Дополнительные сведения о классификации таблиц см. в таблице [сортировки и категоризации.](sorting-and-categorization.md)
  
## <a name="mfcmapi-reference"></a>Справочные материалы по MFCMAPI

Пример кода MFCMAPI указан в приведенной ниже таблице.
  
|**Файл**|**Функция**|**Примечание**|
|:-----|:-----|:-----|
|ContentsTableListCtrl.cpp  <br/> |CContentsTableListCtrl::D oExpandCollapse  <br/> |MFCMAPI использует метод **IMAPITable::CollapseRow** для свернуть категорию таблицы.  <br/> |
   
## <a name="see-also"></a>См. также



[IMAPITable::ExpandRow](imapitable-expandrow.md)
  
[IMAPITable::GetCollapseState](imapitable-getcollapsestate.md)
  
[IMAPITable::QuerySortOrder](imapitable-querysortorder.md)
  
[IMAPITable::SetCollapseState](imapitable-setcollapsestate.md)
  
[IMAPITable::SortTable](imapitable-sorttable.md)
  
[SSortOrderSet](ssortorderset.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)


[Mfcmapi (en) � �������� ������� ����](mfcmapi-as-a-code-sample.md)

