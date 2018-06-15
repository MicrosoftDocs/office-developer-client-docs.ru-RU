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
description: '���� ���������� ���������: 23 ���� 2011 �.'
ms.openlocfilehash: a6ae89bf9b2b16439cc06f0e106859dda10ea22c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/15/2018
ms.locfileid: "19808828"
---
# <a name="imapicontrolgetstate"></a>IMAPIControl::GetState

  
  
**Применимо к**: Outlook 
  
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
    
## <a name="return-value"></a>������������ ��������

ЗНАЧЕНИЕ S_OK 
  
> Состояние элемента управления кнопка был успешно извлечен.
    
## <a name="remarks"></a>Замечания

Поставщики услуг реализуйте метод **IMAPIControl::GetState** для предоставления MAPI с состоянием элемента управления button. Кнопка может отвечать на щелчок мыши или нажатия клавиш. Если они отключены, кнопка недоступна и не отвечает на щелчок мыши или нажатия клавиш. 
  
Дополнительные сведения о реализации **GetState** , а другой [IMAPIControl: IUnknown](imapicontroliunknown.md) методы, видеть [Реализации объекта элемента управления](control-object-implementation.md).
  
## <a name="see-also"></a>См. также



[IMAPIControl::Activate](imapicontrol-activate.md)
  
[IMAPIControl: IUnknown](imapicontroliunknown.md)

