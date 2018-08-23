---
title: IMAPITableGetCollapseState
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPITable.GetCollapseState
api_type:
- COM
ms.assetid: fd4ea496-4c83-49cd-854e-f373cc1ed2af
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 46d993060d03b8c22c2d6c083c05f023648e6642
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22589667"
---
# <a name="imapitablegetcollapsestate"></a>IMAPITable::GetCollapseState

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Возвращает данные, необходимые для перестроения текущего свернут или развернут состояние форматирование таблицы.
  
```cpp
HRESULT GetCollapseState(
ULONG ulFlags,
ULONG cbInstanceKey,
LPBYTE lpbInstanceKey,
ULONG FAR * lpcbCollapseState,
LPBYTE FAR * lppbCollapseState
);
```

## <a name="parameters"></a>���������

 _ulFlags_
  
> Зарезервировано; должно быть равно нулю.
    
 _cbInstanceKey_
  
> [in] Число байт в экземпляре ключ, на который указывает параметр _lpbInstanceKey_ . 
    
 _lpbInstanceKey_
  
> [in] Указатель на **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) свойство строки, в которой текущего свернут или развернут состояние следует перестроение. Параметр _lpbInstanceKey_ не может быть NULL. 
    
 _lpcbCollapseState_
  
> [out] Указатель на число указывает параметр _lppbCollapseState_ структуры. 
    
 _lppbCollapseState_
  
> [out] Указатель на указатель на структуры, содержащие данные, которые описывают текущее представление таблицы.
    
## <a name="return-value"></a>������������ ��������

ЗНАЧЕНИЕ S_OK 
  
> Состояние для форматирование таблицы успешно сохранен.
    
MAPI_E_BUSY 
  
> В, не позволяющей операция запуск выполняется другой операции. В процессе выполнения операции должны выполнить либо должна быть остановлена.
    
MAPI_E_NO_SUPPORT 
  
> Таблица не поддерживает категоризации и дополненная и сжатого представления.
    
## <a name="remarks"></a>Замечания

Метод **IMAPITable::GetCollapseState** работает с помощью метода [IMAPITable::SetCollapseState](imapitable-setcollapsestate.md) для изменения представления пользователя по категориям таблицы. **GetCollapseState** сохраняет данные, необходимые для **SetCollapseState** для использования для перестроения соответствующих представлений категорий форматирование таблицы. Сохранение данных определите, поставщиков услуг. Тем не менее большинство поставщиков услуг, реализация **GetCollapseState** сохраните следующее: 
  
- Ключи сортировки (стандартный столбцов и столбцов категории).
    
- Сведения о строку, представляющую ключ экземпляра.
    
- Сведения для восстановления категорий свернутые и улучшенные таблицы.
    
Дополнительные сведения о таблицах по категориям можно [Сортировка и классификации](sorting-and-categorization.md).
  
## <a name="notes-to-implementers"></a>Примечания для исполнителей

Хранить текущее состояние всех узлов таблицы с помощью параметра _lppbCollapseState_ . 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Всегда вызовите **GetCollapseState** перед вызовом **SetCollapseState**. 
  
## <a name="see-also"></a>См. также



[IMAPITable::SetCollapseState](imapitable-setcollapsestate.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)

