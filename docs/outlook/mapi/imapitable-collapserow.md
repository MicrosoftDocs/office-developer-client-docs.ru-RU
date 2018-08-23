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
ms.openlocfilehash: b4dd7e9715c2d3c99eda44f7eed0b3360a2e33be
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22595302"
---
# <a name="imapitablecollapserow"></a>IMAPITable::CollapseRow

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Сворачивание категорию расширенной таблицы, удаление все заголовки нижнего уровня и конечные строки, относящегося к категории из в табличном представлении.
  
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
  
> [in] Число байт в свойстве PR_INSTANCE_KEY, на который указывает параметр _pbInstanceKey_ . 
    
 _pbInstanceKey_
  
> [in] Указатель на свойство **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)), идентифицирующий строку заголовков для категории. 
    
 _ulFlags_
  
> Зарезервировано; должно быть равно нулю.
    
 _lpulRowCount_
  
> [out] Указатель на общее количество строк, которые были исключены из в табличном представлении.
    
## <a name="return-value"></a>������������ ��������

ЗНАЧЕНИЕ S_OK 
  
> Свернуть операция успешно выполнено.
    
MAPI_E_NOT_FOUND 
  
> Строка, определенного параметром _pbInstanceKey_ не существует. 
    
MAPI_E_INVALID_ENTRYID 
  
> Строка, определенного параметром _pbInstanceKey_ не существует. Эта ошибка является альтернативой MAPI_E_NOT_FOUND; поставщиков услуг можно вернуть одну. 
    
## <a name="remarks"></a>Замечания

Метод **IMAPITable::CollapseRow** сворачивает категории таблицы и удаляет его из в табличном представлении. Строки свернуты начиная со строки, заданной свойством **PR_INSTANCE_KEY** указывает параметр _pbInstanceKey_ . Число строк, которые удалены в представлении возвращается в содержимое параметра _lpulRowCount_ . 
  
Уведомления для строки таблицы, которые удаляются из представления, в результате выполнения операции свернуть никогда не создаются. 
  
Если строка, в которой определяется закладку сворачивается из представления, закладки перемещается для указания на ней отображается строка. 
  
Дополнительные сведения о таблицах по категориям можно [Сортировка и классификации](sorting-and-categorization.md).
  
## <a name="mfcmapi-reference"></a>Справочник по mfcmapi (en)

������ ���� mfcmapi (en) ���������� � ������� ����.
  
|**����**|**�������**|**�����������**|
|:-----|:-----|:-----|
|ContentsTableListCtrl.cpp  <br/> |CContentsTableListCtrl::DoExpandCollapse  <br/> |Mfcmapi (en) использует метод **IMAPITable::CollapseRow** для Свернуть категорию в таблице.  <br/> |
   
## <a name="see-also"></a>См. также



[IMAPITable::ExpandRow](imapitable-expandrow.md)
  
[IMAPITable::GetCollapseState](imapitable-getcollapsestate.md)
  
[IMAPITable::QuerySortOrder](imapitable-querysortorder.md)
  
[IMAPITable::SetCollapseState](imapitable-setcollapsestate.md)
  
[IMAPITable::SortTable](imapitable-sorttable.md)
  
[SSortOrderSet](ssortorderset.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)


[Mfcmapi (en) � �������� ������� ����](mfcmapi-as-a-code-sample.md)

