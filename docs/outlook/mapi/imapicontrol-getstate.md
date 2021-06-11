---
title: IMAPIControlGetState
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIControl.GetState
api_type:
- COM
ms.assetid: fb321b48-3e5f-4b99-9af0-a57b66f26a2e
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: f477c617533d66fc129c7192c9f86bb8a46afbb1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419011"
---
# <a name="imapicontrolgetstate"></a>IMAPIControl::GetState

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Извлекает значение, которое указывает, включено или отключено управление кнопкой.
  
```cpp
HRESULT GetState(
  ULONG ulFlags,
  ULONG FAR * lpulState
);
```

## <a name="parameters"></a>Parameters

 _ulFlags_
  
> [in] ���������������; ������ ���� ����� ����.
    
 _lpulState_
  
> [вышел] Указатель на значение, указыва которое указывает состояние управления кнопкой. Одно из следующих значений можно вернуть:
    
MAPI_DISABLED 
  
> Кнопка управления отключена и не может быть нажата. 
    
MAPI_ENABLED 
  
> Кнопка управления включена и может быть нажата.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Состояние управления кнопкой было успешно восстановлено.
    
## <a name="remarks"></a>Примечания

Поставщики услуг реализуют **метод IMAPIControl::GetState,** чтобы обеспечить MAPI состоянием управления кнопками. Если кнопка включена, она может отвечать на щелчком мыши или нажатием клавиши. Если она отключена, кнопка отображается приглухоженной и не реагирует на щелчком мыши или нажатием клавиши. 
  
Дополнительные сведения о том, как реализовать **GetState** и другие [методы IMAPIControl: IUnknown,](imapicontroliunknown.md) см. в этой [строке Control Object Implementation](control-object-implementation.md).
  
## <a name="see-also"></a>См. также



[IMAPIControl::Activate](imapicontrol-activate.md)
  
[IMAPIControl : IUnknown](imapicontroliunknown.md)

