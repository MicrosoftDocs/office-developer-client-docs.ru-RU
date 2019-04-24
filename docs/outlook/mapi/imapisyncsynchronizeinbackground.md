---
title: Имаписинк Синчронизеинбаккграунд
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISync.SynchronizeInBackground
api_type:
- COM
ms.assetid: c4aaca65-d553-476c-8c6d-5f880b6efdc1
description: 'Дата последнего изменения: 26 июня 2012 года'
ms.openlocfilehash: 108073f5e4833d9641e67065eb642320352fffe4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341372"
---
# <a name="imapisync--synchronizeinbackground"></a>IMAPISync : SynchronizeInBackground

 
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
 Инициирует синхронизацию. Этот метод вызывается с помощью Microsoft Outlook 2010 и Microsoft Outlook 2013 и реализуется поставщиками хранилища сообщений. 
  
```cpp
HRESULT SynchronizeInBackground (
  PMAPISIB psibpb
);
```

## <a name="parameters"></a>Параметры

 _псибпб_
  
> Информирует поставщика о том, что будет синхронизировано и предоставляет доступ к интерфейсам, которые можно использовать во время синхронизации. Это структура [маписиб](mapisib.md) . 
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> ����� ������� � ������ ��������� ��������� ��� ��������.
    
## <a name="see-also"></a>См. также



[IMAPISync : IUnknown](imapisynciunknown.md)
  
[MAPISIB](mapisib.md)

