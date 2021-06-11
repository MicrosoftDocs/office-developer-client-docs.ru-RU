---
title: IMAPIViewAdviseSinkOnPrint
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIViewAdviseSink.OnPrint
api_type:
- COM
ms.assetid: d16219a0-268c-428d-9f02-4f06eb5b6d7d
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: e66315042f8b5cd5aff0e4aa076588c9f312376a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406173"
---
# <a name="imapiviewadvisesinkonprint"></a>IMAPIViewAdviseSink::OnPrint

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Заветив зрителю формы состояние печати формы.
  
```cpp
HRESULT OnPrint(
ULONG dwPageNumber,
HRESULT hrStatus
);
```

## <a name="parameters"></a>Parameters

 _dwPageNumber_
  
> [in] Номер последней напечатанной страницы.
    
 _hrStatus_
  
> [in] Значение HRESULT, указывающее состояние задания печати. Возможные значения:
    
S_FALSE 
  
> Задание печати успешно завершено.
    
S_OK 
  
> Задание печати находится в процессе выполнения.
    
FAILED 
  
> Задание печати было прекращено из-за сбоя.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Уведомление успешно.
    
MAPI_E_USER_CANCEL 
  
> Пользователь отменил операцию, как правило, нажав кнопку Отмена в диалоговом окне. 
    
## <a name="remarks"></a>Примечания

Объекты формы называют **метод IMAPIViewAdviseSink::OnPrint** во время печати, чтобы сообщить зрителю о ходе печати. 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Если задание печати включает несколько страниц, вы можете вызвать **OnPrint** после печати каждой страницы. Установите  _dwPageNumber_ на страницу, напечатаемую в настоящее время, и  _hrStatus_ S_OK. По завершению задания печати вызывайте **OnPrint** с набором  _dwPageNumber_ на последнюю напечатанную страницу,  _а hrStatus_ — S_FALSE. 
  
Дополнительные сведения об уведомлениях формы см. в рублях [Отправка и получение уведомлений о форме.](sending-and-receiving-form-notifications.md)
  
## <a name="see-also"></a>См. также



[IMAPIViewAdviseSink : IUnknown](imapiviewadvisesinkiunknown.md)

