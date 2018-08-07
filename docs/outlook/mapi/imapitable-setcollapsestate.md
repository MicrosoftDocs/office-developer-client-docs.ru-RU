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
ms.openlocfilehash: 252b6d6c7ff74acd5f0b288af48ff2901c2330ad
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809241"
---
# <a name="imapitablesetcollapsestate"></a>IMAPITable::SetCollapseState

  
  
**Относится к**: Outlook 
  
Заново создает текущее развернутое или свернутое состояние форматирование таблицы с использованием данных, сохраненный во время предыдущего вызова метода [IMAPITable::GetCollapseState](imapitable-getcollapsestate.md) . 
  
```cpp
HRESULT SetCollapseState(
ULONG ulFlags,
ULONG cbCollapseState,
LPBYTE pbCollapseState,
BOOKMARK FAR * lpbkLocation
);
```

## <a name="parameters"></a>���������

 _ulFlags_
  
> Зарезервировано; должно быть равно нулю.
    
 _cbCollapseState_
  
> [in] Число байт в структуре, на который указывает параметр _pbCollapseState_ . 
    
 _pbCollapseState_
  
> [in] Указатель на структуры, содержащие данные, необходимые для перестроения в табличном представлении.
    
 _lpbkLocation_
  
> [out] Указатель на закладку, идентифицирующий строку в таблице, необходимо перестроить свернутого или развернутого состояния. В этом закладку и ключа экземпляра, переданной в параметре _lpbInstanceKey_ в вызове [IMAPITable::GetCollapseState](imapitable-getcollapsestate.md) определите той же строке. 
    
## <a name="return-value"></a>������������ ��������

ЗНАЧЕНИЕ S_OK 
  
> Состояние по категориям таблицы успешно восстановлены.
    
MAPI_E_BUSY 
  
> В, не позволяющей операция запуск выполняется другой операции. В процессе выполнения операции должны выполнить либо должна быть остановлена.
    
MAPI_E_UNABLE_TO_COMPLETE 
  
> Таблица не может завершить перестроение свернутого или развернутого представления.
    
## <a name="remarks"></a>Замечания

Метод **IMAPITable::SetCollapseState** восстанавливает развернутое или свернутое состояние в табличном представлении. **SetCollapseState** и **GetCollapseState** работают вместе следующим образом: 
  
1. Считается изменение состояния форматирование таблицы, чтобы сохранить все данные, относящиеся к состоянию до изменения называется [IMAPITable::GetCollapseState](imapitable-getcollapsestate.md) . 
    
2. Чтобы восстановить представление таблицы в состояние сохраненного, называется **SetCollapseState** . Данные сохраняются **GetCollapseState** передается в **SetCollapseState**. **SetCollapseState** могут использовать эти данные для восстановления состояния. 
    
3. **SetCollapseState** возвращает в качестве выходного параметра закладка, идентифицирующее той же строке ключ экземпляра, переданной в качестве входных данных для **GetCollapseState**.
    
Дополнительные сведения о таблицах по категориям можно [Сортировка и классификации](sorting-and-categorization.md). 
  
## <a name="notes-to-implementers"></a>Примечания для исполнителей

Вы несете ответственность за проверка, что порядок сортировки и ограничения полностью совпадают, как во время вызова **GetCollapseState** . Если был изменен, **SetCollapseState** его не следует вызывать поскольку результатов может быть непредсказуемым. Это может произойти, если, например, клиент вызывает **GetCollapseState** , а затем **SortTable** , чтобы изменить ключ сортировки до вызова метода **SetCollapseState**. В целях безопасности проверки, что сохраненные данные по-прежнему перед тем как продолжить восстановление. 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Чтобы позвонить **SetCollapseState**, необходимо ранее вызова **GetCollapseState**. Порядок сортировки, определение категории должно совпадать для обоих методов. Если порядок сортировки не совпадают, результаты операции **SetCollapseState** непредсказуемы. 
  
## <a name="see-also"></a>См. также



[IMAPITable::CreateBookmark](imapitable-createbookmark.md)
  
[IMAPITable::FreeBookmark](imapitable-freebookmark.md)
  
[IMAPITable::GetCollapseState](imapitable-getcollapsestate.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)

