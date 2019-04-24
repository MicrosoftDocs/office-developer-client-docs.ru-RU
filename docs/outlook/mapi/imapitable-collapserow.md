---
title: Имапитаблеколлапсеров
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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328969"
---
# <a name="imapitablecollapserow"></a>IMAPITable::CollapseRow

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Сворачивает развернутую категорию таблицы, удаляя все заголовки нижнего уровня и конечные строки, принадлежащие к категории, из представления таблицы.
  
```cpp
HRESULT CollapseRow(
ULONG cbInstanceKey,
LPBYTE pbInstanceKey,
ULONG ulFlags,
ULONG FAR * lpulRowCount
);
```

## <a name="parameters"></a>Параметры

 _Кбинстанцекэй_
  
> возврата Количество байтов в свойстве ПР_ИНСТАНЦЕ_КЭЙ, на которое указывает параметр _пбинстанцекэй_ . 
    
 _Пбинстанцекэй_
  
> возврата Указатель на свойство **пр_инстанце_кэй** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)), которое определяет строку заголовка для категории. 
    
 _ulFlags_
  
> Резервирования должно быть равно нулю.
    
 _Лпулровкаунт_
  
> вышли Указатель на общее число строк, которые удаляются из представления таблицы.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Операция сворачивания выполнена успешно.
    
МАПИ_Е_НОТ_ФАУНД 
  
> Строка, указанная с помощью параметра _пбинстанцекэй_ , не существует. 
    
МАПИ_Е_ИНВАЛИД_ЕНТРИД 
  
> Строка, указанная с помощью параметра _пбинстанцекэй_ , не существует. Эта ошибка является альтернативой МАПИ_Е_НОТ_ФАУНД; поставщики услуг могут возвращать один из них. 
    
## <a name="remarks"></a>Комментарии

Метод **IMAPITable:: коллапсеров** сворачивает категорию таблицы и удаляет ее из представления таблицы. Строки свернуты, начиная со строки, указанной свойством **пр_инстанце_кэй** , на которую указывает параметр _пбинстанцекэй_ . Количество строк, удаленных из представления, возвращается в содержимом параметра _лпулровкаунт_ . 
  
Уведомления никогда не создаются для строк таблицы, которые удаляются из представления в результате выполнения операции свертывания. 
  
Когда строка, определенная закладками, свернута в представлении, закладка перемещается в указатель на следующую видимую строку. 
  
Для получения дополнительных сведений об классифицированных таблицах, ознакомьтесь со статьей [Сортировка и категоризация](sorting-and-categorization.md).
  
## <a name="mfcmapi-reference"></a>Справочные материалы по MFCMAPI

Пример кода MFCMAPI указан в приведенной ниже таблице.
  
|**Файл**|**Функция**|**Примечание**|
|:-----|:-----|:-----|
|Контентстаблелистктрл. cpp  <br/> |Кконтентстаблелистктрл::D Оекспандколлапсе  <br/> |MFCMAPI использует метод **IMAPITable:: коллапсеров** для сворачивания категории таблицы.  <br/> |
   
## <a name="see-also"></a>См. также



[IMAPITable::ExpandRow](imapitable-expandrow.md)
  
[IMAPITable::GetCollapseState](imapitable-getcollapsestate.md)
  
[IMAPITable::QuerySortOrder](imapitable-querysortorder.md)
  
[IMAPITable::SetCollapseState](imapitable-setcollapsestate.md)
  
[IMAPITable::SortTable](imapitable-sorttable.md)
  
[SSortOrderSet](ssortorderset.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)


[Mfcmapi (en) � �������� ������� ����](mfcmapi-as-a-code-sample.md)

