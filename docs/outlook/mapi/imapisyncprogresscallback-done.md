---
title: IMAPISyncProgressCallbackDone
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISyncProgressCallback.Done
api_type:
- COM
ms.assetid: aaa8eb56-f22f-4c5a-a224-807ff001e0ca
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 8d397e12b8b24c5031e6e6d89d98134d487a815b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422350"
---
# <a name="imapisyncprogresscallbackdone"></a>IMAPISyncProgressCallback::Done

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
 Сообщает Microsoft Outlook о том, что синхронизация завершена. 
  
```cpp
HRESULT Done(
  HANDLE hThreadDoneEvent, 
  HRESULT hResult
);
```

## <a name="parameters"></a>Параметры

 **hThreadDoneEvent**
  
> Событие, которое передается обратно, чтобы позволить Microsoft Outlook закрыть handle. Это может быть NULL.
    
 **hResult**
  
> HRESULT, указывающий конечное состояние хода выполнения.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> ����� ������� � ������ ��������� ��������� ��� ��������.
    
## <a name="see-also"></a>См. также



[IMAPISyncProgressCallback : IUnknown](imapisyncprogresscallbackiunknown.md)

