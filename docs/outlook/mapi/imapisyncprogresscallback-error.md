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
ms.openlocfilehash: 80010ca19999ba519f051e914f02f240abb524e2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424933"
---
# <a name="imapisyncprogresscallbackerror"></a>IMAPISyncProgressCallback::Error

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Предоставляет сведения, отображаемые в диалоговом окте Отправка/Получение. Если во время синхронизации встречаются ошибки, поставщик магазина вызывает эту функцию.
  
```cpp
HRESULT Error(
  HRESULT hResult,
  const WCHAR *pwcszErrorStr
);
```

## <a name="parameters"></a>Parameters

 **hResult**
  
> HRESULT ошибки или предупреждения.
    
 **pwcszErrorStr**
  
> Указатель на строку, связанную с отображаемой ошибкой.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> ����� ������� � ������ ��������� ��������� ��� ��������.
    
## <a name="see-also"></a>См. также



[IMAPISyncProgressCallback : IUnknown](imapisyncprogresscallbackiunknown.md)

