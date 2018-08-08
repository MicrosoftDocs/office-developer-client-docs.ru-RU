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
ms.openlocfilehash: 01bdf6cdde864d1ea4ed19dfeb01a96236dc9c63
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808891"
---
# <a name="imapiformadvisesinkonchange"></a>IMAPIFormAdviseSink::OnChange

  
  
**Относится к**: Outlook 
  
Указывает, было изменено в состояние просмотра формы. 
  
```cpp
HRESULT OnChange(
  ULONG ulDir
);
```

## <a name="parameters"></a>Параметры

 _ulDir_
  
> [in] Битовая маска флаги, который предоставляет сведения об изменениях, выполненной в средстве просмотра и ожидаемых ответа в форме. Можно задать следующие флажки:
    
VCSTATUS_CATEGORY 
  
> Имеется следующий или предыдущий сообщение в другой категории. 
    
VCSTATUS_INTERACTIVE 
  
> Форма должна пользовательского интерфейса. Если этот флаг не установлен, форма следует отключать отображение пользовательского интерфейса, даже в ответ на команду, которая обычно приводит пользовательского интерфейса для отображения. 
    
VCSTATUS_MODAL 
  
> Форма является модальным для просмотра формы. 
    
VCSTATUS_NEXT 
  
> В средстве просмотра формы существует следующее сообщение. 
    
VCSTATUS_PREV 
  
> В средстве просмотра формы существует предыдущее сообщение. 
    
VCSTATUS_READONLY 
  
> Удаление, отправка и переместите операции должны быть отключены. 
    
VCSTATUS_UNREAD 
  
> В средстве просмотра формы имеется следующий или предыдущий непрочитанные сообщения.
    
## <a name="return-value"></a>������������ ��������

ЗНАЧЕНИЕ S_OK 
  
> Уведомление успешно.
    
## <a name="remarks"></a>Замечания

Средства просмотра форм вызовите метод **IMAPIFormAdviseSink::OnChange** для уведомления формы об изменении состояния средство просмотра. Как правило только изменения задание или снять VCSTATUS_NEXT или VCSTATUS_PREVIOUS флаг, в зависимости от наличия или отсутствия следующий или предыдущий сообщения в средстве просмотра. Соответственно объект формы затем включает или отключает следующий или предыдущий действия, которые он поддерживает. 
  
Параметры VCSTATUS_MODAL и VCSTATUS_INTERACTIVE не может изменить в контекст представления после его создания.
  
## <a name="notes-to-implementers"></a>Примечания для исполнителей

Реализации этого метода полностью зависит от особенностей формы. Большинство объектов формы используйте этот метод для изменения их пользовательского интерфейса (например, чтобы включить или отключить команды меню или кнопки в соответствии с параметр flags состояние просмотра).
  
## <a name="see-also"></a>См. также



[IMAPIViewContext::ActivateNext](imapiviewcontext-activatenext.md)
  
[IMAPIFormAdviseSink : IUnknown](imapiformadvisesinkiunknown.md)

