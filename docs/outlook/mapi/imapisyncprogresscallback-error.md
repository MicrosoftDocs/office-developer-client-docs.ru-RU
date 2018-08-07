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
ms.openlocfilehash: 9dc368e6502bbb14cf42f6bc5a08fd2893f98bf6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809180"
---
# <a name="imapisyncprogresscallbackerror"></a>IMAPISyncProgressCallback::Error

  
  
**Относится к**: Outlook 
  
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
    
## <a name="return-value"></a>������������ ��������

ЗНАЧЕНИЕ S_OK 
  
> ����� ������� � ������ ��������� ��������� ��� ��������.
    
## <a name="see-also"></a>См. также



[IMAPISyncProgressCallback : IUnknown](imapisyncprogresscallbackiunknown.md)

