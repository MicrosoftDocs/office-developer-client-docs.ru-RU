---
title: имапиконтролжетстате
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

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Получает значение, которое указывает, включен ли элемент управления "Кнопка" или отключен.
  
```cpp
HRESULT GetState(
  ULONG ulFlags,
  ULONG FAR * lpulState
);
```

## <a name="parameters"></a>Параметры

 _ulFlags_
  
> [in] ���������������; ������ ���� ����� ����.
    
 _лпулстате_
  
> вышли Указатель на значение, указывающее состояние элемента управления "Кнопка". Можно возвратить одно из следующих значений:
    
MAPI_DISABLED 
  
> Элемент управления "Кнопка" отключен и не может быть выбран. 
    
MAPI_ENABLED 
  
> Элемент управления Button включен и может быть выбран.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Состояние элемента управления "Кнопка" успешно извлечено.
    
## <a name="remarks"></a>Примечания

Поставщики услуг реализуют метод **имапиконтрол::** , который обеспечивает MAPI с состоянием элемента управления "Кнопка". Если кнопка включена, она может реагировать на нажатие кнопки мыши или нажатия клавиши. Если эта кнопка отключена, кнопка отображается серым цветом и не реагирует на щелчок мышью или нажатие клавиши. 
  
Дополнительные сведения о **том, как реализовать метод** GetObject и другие методы [имапиконтрол: IUnknown](imapicontroliunknown.md) , можно найти в разделе [Реализация объекта Control](control-object-implementation.md).
  
## <a name="see-also"></a>См. также



[IMAPIControl::Activate](imapicontrol-activate.md)
  
[IMAPIControl : IUnknown](imapicontroliunknown.md)

