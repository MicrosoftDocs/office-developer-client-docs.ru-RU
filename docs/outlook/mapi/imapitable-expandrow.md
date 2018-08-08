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
ms.openlocfilehash: 1b3d8c74d85696e733b378a4cac2b8e2a3b6a072
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809200"
---
# <a name="imapitableexpandrow"></a>IMAPITable::ExpandRow

  
  
**Относится к**: Outlook 
  
При развертывании категории свернутые таблицы, добавление конечных или нижнем уровне заголовка строки, относящегося к категории, которую требуется в табличном представлении.
  
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
  
> [in] Число байт в свойстве PR_INSTANCE_KEY, на который указывает параметр _pbInstanceKey_ . 
    
 _pbInstanceKey_
  
> [in] Указатель на свойство **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)), идентифицирующий строку заголовков для категории. 
    
 _ulRowCount_
  
> [in] Максимальное число строк для возвращения в параметре _lppRows_ . 
    
 _ulFlags_
  
> Зарезервировано; должно быть равно нулю.
    
 _lppRows_
  
> [out] Указатель на структуру [SRowSet](srowset.md) , получение первого (до _ulRowCount_) строк, добавленных в табличном представлении из-за развертывание. Эти строки вставляется после строки заголовка, определенного параметром _pbInstanceKey_ . Параметр _lppRows_ может быть NULL, если параметр _ulRowCount_ равно нулю. 
    
 _lpulMoreRows_
  
> [out] Указатель на общее количество строк, которые были добавлены в табличном представлении.
    
## <a name="return-value"></a>������������ ��������

ЗНАЧЕНИЕ S_OK 
  
> Категории была расширена успешно.
    
MAPI_E_NOT_FOUND 
  
> Строка, определенного параметром _pbInstanceKey_ не существует. 
    
## <a name="remarks"></a>Замечания

Метод **IMAPITable::ExpandRow** разворачивает свернутые категорию, добавление конечных или нижнем уровне заголовка строки, относящихся к категории, которую требуется в табличном представлении. Максимальное число строк, возвращаемых с помощью параметра _lppRows_ можно указать с помощью параметра _ulRowCount_ . Если одна или несколько строк, возвращенных в наборе строк, на который указывает _lppRows_ _ulRowCount_ задано значение больше нуля, задайте положение закладки, BOOKMARK_CURRENT перемещается в строку сразу после последней строки в строке.
  
Когда _ulRowCount_ имеет значение нуль, разрешения на запрос, который нуль конечного или нижнем уровне строки заголовка добавляется по категории или не возвращается ноль строки, так как нет конечного или нижнем уровне заголовков строк в категории, положение BOOKMARK_CURRENT задано значение строки следующие строки, _pbInstanceKey_. 
  
## <a name="notes-to-implementers"></a>Примечания для исполнителей

Не создавать уведомления на строки, которые добавлены в представлении таблицы из-за расширения категории.
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Количество строк в наборе строк, на который указывает параметр _lppRows_ не может быть равен максимальному числу строк, которые фактически были добавлены к таблице, весь набор конечных или нижнем уровне заголовка строки для категории. Например, недостаточно памяти или количество строк в категории, превышающие номер, указанный в параметре _ulRowCount_ могут возникать ошибки. В любом случае BOOKMARK_CURRENT будет размещен в последней строки. Чтобы немедленно получить остальных строк в категории, вызовите [IMAPITable::QueryRows](imapitable-queryrows.md).
  
Не ожидается в таблице уведомлений при изменении состояния категории. Удовлетворяет локальный кэш строк, которые могут быть обновлены с каждым вызовом **ExpandRow** или **CollapseRow** . 
  
Дополнительные сведения о таблицах по категориям можно [Сортировка и классификации](sorting-and-categorization.md).
  
## <a name="mfcmapi-reference"></a>Справочник по mfcmapi (en)

������ ���� mfcmapi (en) ���������� � ������� ����.
  
|**����**|**�������**|**�����������**|
|:-----|:-----|:-----|
|ContentsTableListCtrl.cpp  <br/> |CContentsTableListCtrl::DoExpandCollapse  <br/> |Mfcmapi (en) использует метод **IMAPITable::ExpandRow** разверните категорию свернутые.  <br/> |
   
## <a name="see-also"></a>См. также



[IMAPITable::CollapseRow](imapitable-collapserow.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)


[Mfcmapi (en) � �������� ������� ����](mfcmapi-as-a-code-sample.md)

