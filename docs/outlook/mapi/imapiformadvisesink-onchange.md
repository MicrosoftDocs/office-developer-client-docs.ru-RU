---
title: IMAPIFormAdviseSinkOnChange
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormAdviseSink.OnChange
api_type:
- COM
ms.assetid: d700b40f-e5b2-4d37-bf1f-8fd3dfa0dda5
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 02663570e3173bbd696af732e71f060d9dee49bc
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431899"
---
# <a name="imapiformadvisesinkonchange"></a>IMAPIFormAdviseSink::OnChange

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Указывает, что в состоянии просмотра формы произошли изменения. 
  
```cpp
HRESULT OnChange(
  ULONG ulDir
);
```

## <a name="parameters"></a>Parameters

 _ulDir_
  
> [in] Битмашка флагов, которая содержит сведения об изменениях, произошедших в зрительском окне, и ожидаемом отклике в форме. Можно установить следующие флаги:
    
VCSTATUS_CATEGORY 
  
> Существует следующее или предыдущее сообщение в другой категории. 
    
VCSTATUS_INTERACTIVE 
  
> В форме должен отображаться пользовательский интерфейс. Если этот флаг не установлен, форма должна подавлять отображение пользовательского интерфейса даже в ответ на глагол, который обычно вызывает отображение пользовательского интерфейса. 
    
VCSTATUS_MODAL 
  
> Форма должна быть модальной для просмотра формы. 
    
VCSTATUS_NEXT 
  
> В представлении формы есть следующее сообщение. 
    
VCSTATUS_PREV 
  
> В представлении формы имеется предыдущее сообщение. 
    
VCSTATUS_READONLY 
  
> Операции удаления, отправки и перемещения должны быть отключены. 
    
VCSTATUS_UNREAD 
  
> В представлении формы имеется следующее или предыдущее непрочитанные сообщения.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Уведомление было успешным.
    
## <a name="remarks"></a>Примечания

Зрители формы звонят по методу **IMAPIFormAdviseSink::OnChange,** чтобы уведомить форму об изменении состояния пользователя. Обычно единственным изменением является установка или очистка флага VCSTATUS_NEXT или VCSTATUS_PREVIOUS в зависимости от наличия или отсутствия следующего или предыдущего сообщения в зрителье. Соответственно, объект формы включает или отключает любые последующие или предыдущие действия, которые он поддерживает. 
  
Параметры VCSTATUS_MODAL и VCSTATUS_INTERACTIVE не могут измениться в контексте представления после создания.
  
## <a name="notes-to-implementers"></a>Примечания для исполнителей

Конкретная реализация этого метода полностью зависит от специфики формы. Большинство объектов формы используют этот метод для изменения пользовательского интерфейса (например, для включения или отключения команд или кнопок меню, чтобы соответствовать параметру флагов состояния просмотра).
  
## <a name="see-also"></a>См. также



[IMAPIViewContext::ActivateNext](imapiviewcontext-activatenext.md)
  
[IMAPIFormAdviseSink : IUnknown](imapiformadvisesinkiunknown.md)

