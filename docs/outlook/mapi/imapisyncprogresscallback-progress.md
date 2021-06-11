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
ms.openlocfilehash: 9b44337a4bc9615558ac6337e99ea206ba063b1a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429112"
---
# <a name="imapisyncprogresscallbackprogress"></a>IMAPISyncProgressCallback::Progress

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Обновляет состояние в диалоговом окантове Отправка/Получение. Поставщик магазина периодически вызывает эту функцию.
  
```cpp
HRESULT Progress(
  const WCHAR *pwcszProgress, 
  ULONG ulIndex, 
  ULONG ulIndexMax
);
```

## <a name="parameters"></a>Parameters

 **pwczsProgress**
  
> Указатель на строку, отображаемую на текущем этапе выполнения. Это может быть NULL для обновления прогресса.
    
 **ulIndex**
  
> Текущая позиция.
    
 **ulIndexMax**
  
> Индекс, указывающий полный прогресс.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> ����� ������� � ������ ��������� ��������� ��� ��������.
    
## <a name="see-also"></a>См. также



[IMAPISyncProgressCallback : IUnknown](imapisyncprogresscallbackiunknown.md)

