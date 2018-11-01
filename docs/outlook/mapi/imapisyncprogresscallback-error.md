---
title: IMAPISyncProgressCallbackError
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISyncProgressCallback.Error
api_type:
- COM
ms.assetid: 4860992d-65d7-4cb0-a874-ceccb153dbac
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 8cff424e3b589af292e56cef1ca19198e9c80d1f
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22594987"
---
# <a name="imapisyncprogresscallbackerror"></a>IMAPISyncProgressCallback::Error

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Сведения, которые отображаются в диалоговом окне отправки и получения. Ошибки, возникающие во время синхронизации, поставщик хранения вызывает эту функцию.
  
```cpp
HRESULT Error(
  HRESULT hResult,
  const WCHAR *pwcszErrorStr
);
```

## <a name="parameters"></a>Параметры

 **hResult**
  
> Значение HRESULT сообщение об ошибке или предупреждение.
    
 **pwcszErrorStr**
  
> Указатель на строку, связанную с ошибкой для отображения.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> ����� ������� � ������ ��������� ��������� ��� ��������.
    
## <a name="see-also"></a>См. также



[IMAPISyncProgressCallback : IUnknown](imapisyncprogresscallbackiunknown.md)

