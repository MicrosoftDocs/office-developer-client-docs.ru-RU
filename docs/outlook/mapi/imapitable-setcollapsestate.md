---
title: IMAPITableSetCollapseState
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPITable.SetCollapseState
api_type:
- COM
ms.assetid: 31325e8f-1cf9-49b2-8118-953996b0037f
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 7351457dc5b72cfc4a7ef9f91e9d33a80ca98c39
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414069"
---
# <a name="imapitablesetcollapsestate"></a>IMAPITable::SetCollapseState

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Перестраивать текущее расширенное или свернутое состояние классизированной таблицы с помощью данных, сохраненных при предыдущем вызове метода [IMAPITable::GetCollapseState.](imapitable-getcollapsestate.md) 
  
```cpp
HRESULT SetCollapseState(
ULONG ulFlags,
ULONG cbCollapseState,
LPBYTE pbCollapseState,
BOOKMARK FAR * lpbkLocation
);
```

## <a name="parameters"></a>Параметры

 _ulFlags_
  
> Зарезервировано; должно быть нулем.
    
 _cbCollapseState_
  
> [in] Количествобайтов в структуре, на которые указывает параметр _pbCollapseState._ 
    
 _pbCollapseState_
  
> [in] Указатель на структуры, содержащие данные, необходимые для перестроения представления таблицы.
    
 _lpbkLocation_
  
> [out] Указатель на закладку, определяя строку в таблице, в которой необходимо перестроить свернутые или расширенные состояния. Эта закладка и ключ экземпляра, переданные в  _параметре lpbInstanceKey_ при вызове [IMAPITable::GetCollapseState,](imapitable-getcollapsestate.md) определяют ту же строку. 
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Состояние классизированной таблицы было успешно перестроено.
    
MAPI_E_BUSY 
  
> В настоящее время идет другая операция, которая препятствует запуску операции. Либо операция должна быть завершена, либо она должна быть остановлена.
    
MAPI_E_UNABLE_TO_COMPLETE 
  
> Не удалось завершить перестройку свернутой или расширенной представления.
    
## <a name="remarks"></a>Примечания

Метод **IMAPITable::SetCollapseState** повторно восстановить состояние расширенного или свернутого представления таблицы. **SetCollapseState** и **GetCollapseState** работают вместе следующим образом: 
  
1. Когда состояние классизированной таблицы вот-вот изменится, будет вызванО сообщение [IMAPITable::GetCollapseState,](imapitable-getcollapsestate.md) чтобы сохранить все данные, относящиеся к этому состоянии, до изменения. 
    
2. Чтобы восстановить представление таблицы до сохраненного состояния, **вызвано setCollapseState.** Данные, сохраненные с помощью **GetCollapseState,** передаются **в setCollapseState.** **SetCollapseState** может использовать эти данные для восстановления состояния. 
    
3. **SetCollapseState** возвращает в качестве выходного параметра закладку, которая определяет ту же строку, что и ключ экземпляра, переданный в качестве входных данных **для GetCollapseState.**
    
Дополнительные сведения о категориях таблиц см. в таблице [сортировки и категоризации.](sorting-and-categorization.md) 
  
## <a name="notes-to-implementers"></a>Примечания для исполнителей

Вы несете ответственность за проверку того, что порядок сортировки и ограничения точно такие же, как они были во время вызова **GetCollapseState.** Если было внося изменение, не следует использовать **SetCollapseState,** так как результаты могут быть непредсказуемыми. Это может произойти, если, например, клиент вызывает **GetCollapseState,** а затем **SortTable** для изменения ключа сортировки перед вызовом **SetCollapseState**. Чтобы быть безопасным, убедитесь, что сохраненные данные остаются действительными, прежде чем при восстановлении. 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Чтобы вызвать **SetCollapseState,** необходимо ранее вызвать **GetCollapseState.** Порядок сортировки, устанавливающий категории, должен быть одинаковым для обоих методов. Если заказы сортировки отличаются, результаты операции **SetCollapseState** непредсказуемы. 
  
## <a name="see-also"></a>См. также



[IMAPITable::CreateBookmark](imapitable-createbookmark.md)
  
[IMAPITable::FreeBookmark](imapitable-freebookmark.md)
  
[IMAPITable::GetCollapseState](imapitable-getcollapsestate.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)

