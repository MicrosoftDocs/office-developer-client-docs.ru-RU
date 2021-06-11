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
ms.openlocfilehash: 97575a65cd6825e07d6f11c813beec539f99f53a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436078"
---
# <a name="imapitablegetcollapsestate"></a>IMAPITable::GetCollapseState

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Возвращает данные, необходимые для восстановления текущего рухнувшего или расширенного состояния классифицизированной таблицы.
  
```cpp
HRESULT GetCollapseState(
ULONG ulFlags,
ULONG cbInstanceKey,
LPBYTE lpbInstanceKey,
ULONG FAR * lpcbCollapseState,
LPBYTE FAR * lppbCollapseState
);
```

## <a name="parameters"></a>Parameters

 _ulFlags_
  
> Зарезервировано; должно быть нулевой.
    
 _cbInstanceKey_
  
> [in] Количество bytes в ключе экземпляра, на который указывает параметр _lpbInstanceKey._ 
    
 _lpbInstanceKey_
  
> [in] Указатель на **свойство PR_INSTANCE_KEY** [(PidTagInstanceKey)](pidtaginstancekey-canonical-property.md)строки, при которой текущее состояние рухнуло или расширено, должно быть восстановлено. Параметр  _lpbInstanceKey не_ может быть NULL. 
    
 _lpcbCollapseState_
  
> [вышел] Указатель на количество структур, на которые указывает параметр _lppbCollapseState._ 
    
 _lppbCollapseState_
  
> [вышел] Указатель на указатель на структуры, содержащие данные, описывая текущее представление таблицы.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Состояние для классифицизированной таблицы было успешно сохранено.
    
MAPI_E_BUSY 
  
> В настоящее время продолжается еще одна операция, которая не позволяет начать операцию. Либо операция должна быть разрешена к завершению, либо она должна быть остановлена.
    
MAPI_E_NO_SUPPORT 
  
> Таблица не поддерживает категоризации, а также расширенные и свернутые представления.
    
## <a name="remarks"></a>Примечания

Метод **IMAPITable::GetCollapseState** работает с методом [IMAPITable::SetCollapseState,](imapitable-setcollapsestate.md) чтобы изменить представление пользователя о классифицируемых таблицах. **GetCollapseState** сохраняет данные, необходимые **для SetCollapseState** для восстановления соответствующих представлений категорий таблицы. Поставщики услуг определяют данные, которые необходимо сохранить. Однако большинство поставщиков услуг, реализующих **GetCollapseState,** сохраняет следующее: 
  
- Клавиши сортировки (стандартные столбцы и столбцы категорий).
    
- Сведения о строке, которую представляет ключ экземпляра.
    
- Сведения для восстановления разрушенных и расширенных категорий таблицы.
    
Дополнительные сведения о классификации таблиц см. в [рубрике Сортировка и классификация.](sorting-and-categorization.md)
  
## <a name="notes-to-implementers"></a>Примечания для исполнителей

Сохранить текущее состояние всех узлов таблицы в параметре _lppbCollapseState._ 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Всегда **вызывай GetCollapseState** перед вызовом **SetCollapseState.** 
  
## <a name="see-also"></a>См. также



[IMAPITable::SetCollapseState](imapitable-setcollapsestate.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)

