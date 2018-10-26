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
ms.openlocfilehash: 3d45c4722b6a0200ea3937ba606da0af5c793df2
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22581855"
---
# <a name="imapicontrolgetstate"></a>IMAPIControl::GetState

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Получает значение, указывающее, включено ли элемент управления button.
  
```cpp
HRESULT GetState(
  ULONG ulFlags,
  ULONG FAR * lpulState
);
```

## <a name="parameters"></a>���������

 _ulFlags_
  
> [in] ���������������; ������ ���� ����� ����.
    
 _lpulState_
  
> [out] Указатель на значение, указывающее состояние элемента управления кнопка. Можно получить одно из следующих значений:
    
MAPI_DISABLED 
  
> Элемент управления button отключена и не может быть выбрана. 
    
MAPI_ENABLED 
  
> Элемент управления button включено, можно щелкнуть.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Состояние элемента управления кнопка был успешно извлечен.
    
## <a name="remarks"></a>Замечания

Поставщики услуг реализуйте метод **IMAPIControl::GetState** для предоставления MAPI с состоянием элемента управления button. Кнопка может отвечать на щелчок мыши или нажатия клавиш. Если они отключены, кнопка недоступна и не отвечает на щелчок мыши или нажатия клавиш. 
  
Дополнительные сведения о реализации **GetState** , а другой [IMAPIControl: IUnknown](imapicontroliunknown.md) методы, видеть [Реализации объекта элемента управления](control-object-implementation.md).
  
## <a name="see-also"></a>См. также



[IMAPIControl::Activate](imapicontrol-activate.md)
  
[IMAPIControl : IUnknown](imapicontroliunknown.md)

