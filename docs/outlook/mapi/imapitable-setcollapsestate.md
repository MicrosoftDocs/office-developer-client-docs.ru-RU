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

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Восстановление текущего расширенного или свернутого состояния таблицы категорий с помощью данных, которые были сохранены при предварительном вызове метода [IMAPITable::GetCollapseState.](imapitable-getcollapsestate.md) 
  
```cpp
HRESULT SetCollapseState(
ULONG ulFlags,
ULONG cbCollapseState,
LPBYTE pbCollapseState,
BOOKMARK FAR * lpbkLocation
);
```

## <a name="parameters"></a>Parameters

 _ulFlags_
  
> Зарезервировано; должно быть нулевой.
    
 _cbCollapseState_
  
> [in] Количество bytes в структуре, на который указывает параметр _pbCollapseState._ 
    
 _pbCollapseState_
  
> [in] Указатель на структуры, содержащие данные, необходимые для восстановления представления таблицы.
    
 _lpbkLocation_
  
> [вышел] Указатель на закладки, определяющие строку в таблице, на которой должно быть восстановлено рухнувшего или расширенного состояния. Эта закладка и ключ экземпляра, переданные в  _параметре lpbInstanceKey_ в [вызове IMAPITable::GetCollapseState,](imapitable-getcollapsestate.md) определяют ту же строку. 
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Состояние классифицизированной таблицы было успешно восстановлено.
    
MAPI_E_BUSY 
  
> В настоящее время продолжается еще одна операция, которая не позволяет начать операцию. Либо операция должна быть разрешена к завершению, либо она должна быть остановлена.
    
MAPI_E_UNABLE_TO_COMPLETE 
  
> В таблице не удалось завершить восстановление рухнувшего или расширенного представления.
    
## <a name="remarks"></a>Примечания

Метод **IMAPITable::SetCollapseState** reestablishes expanded or collapsed state of the table view. **SetCollapseState и** **GetCollapseState** работают вместе следующим образом: 
  
1. Когда состояние классифицируемых таблиц изменится, для сохранения всех данных, относящихся к государству до изменения, вызван [IMAPITable::GetCollapseState.](imapitable-getcollapsestate.md) 
    
2. Чтобы восстановить представление таблицы до сохраненного состояния, **называется SetCollapseState.** Данные, сохраненные **GetCollapseState,** передаются **в SetCollapseState.** **SetCollapseState** может использовать эти данные для восстановления состояния. 
    
3. **SetCollapseState** возвращает в качестве параметра вывода закладки, которая определяет ту же строку, что и ключ экземпляра, переданный в качестве ввода **в GetCollapseState.**
    
Дополнительные сведения о классификации таблиц см. в [рубрике Сортировка и классификация.](sorting-and-categorization.md) 
  
## <a name="notes-to-implementers"></a>Примечания для исполнителей

Вы несете ответственность за проверку того, что порядок сортировки и ограничения точно такие же, как и во время вызова **GetCollapseState.** Если изменения были сделаны, **SetCollapseState** не следует называть, так как результаты могут быть непредсказуемыми. Это может произойти, если, например, клиент вызывает **GetCollapseState,** а затем **SortTable,** чтобы изменить ключ сортировки перед вызовом **SetCollapseState**. Чтобы быть безопасным, убедитесь, что сохраненные данные по-прежнему действительны перед началом восстановления. 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Чтобы вызвать **SetCollapseState,** необходимо предварительно вызвать **GetCollapseState.** Порядок сортировки, устанавливающий категории, должен быть одинаковым для обоих методов. Если заказы сортировки отличаются, результаты операции **SetCollapseState** непредсказуемы. 
  
## <a name="see-also"></a>См. также



[IMAPITable::CreateBookmark](imapitable-createbookmark.md)
  
[IMAPITable::FreeBookmark](imapitable-freebookmark.md)
  
[IMAPITable::GetCollapseState](imapitable-getcollapsestate.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)

