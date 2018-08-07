---
title: IMAPISyncProgressCallbackProgress
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISyncProgressCallback.Progress
api_type:
- COM
ms.assetid: 6797cd1c-8a0b-4f42-ba56-6162d8e7b058
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 12624ef6212f9113041bf5cf3a82e2b7df6eca9e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809182"
---
# <a name="imapisyncprogresscallbackprogress"></a>IMAPISyncProgressCallback::Progress

  
  
**Относится к**: Outlook 
  
Обновление состояния в диалоговом окне отправки и получения. Поставщик хранения периодически вызывает эту функцию.
  
```cpp
HRESULT Progress(
  const WCHAR *pwcszProgress, 
  ULONG ulIndex, 
  ULONG ulIndexMax
);
```

## <a name="parameters"></a>Параметры

 **pwczsProgress**
  
> Указатель на строку, которая отображает текущий этап хода выполнения. Она может быть NULL для отслеживания хода выполнения задач.
    
 **ulIndex**
  
> Текущую позицию в стадии разработки.
    
 **ulIndexMax**
  
> Индекс, указывающее полный хода выполнения.
    
## <a name="return-value"></a>������������ ��������

ЗНАЧЕНИЕ S_OK 
  
> ����� ������� � ������ ��������� ��������� ��� ��������.
    
## <a name="see-also"></a>См. также



[IMAPISyncProgressCallback : IUnknown](imapisyncprogresscallbackiunknown.md)

