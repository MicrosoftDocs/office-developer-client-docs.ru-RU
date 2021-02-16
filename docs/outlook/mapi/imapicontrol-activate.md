---
title: IMAPIControlActivate
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIControl.Activate
api_type:
- COM
ms.assetid: 2b641030-2429-4217-a648-0a9f3d1a1b29
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: d3b47e423daf428c67761d13deef1ae0858c91c0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418017"
---
# <a name="imapicontrolactivate"></a>IMAPIControl::Activate

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Выполняет такую задачу, как отображение диалогового окна или запуск программной операции, когда пользователь клиентского приложения нажимает кнопку управления.
  
```cpp
HRESULT Activate(
  ULONG ulFlags,
  ULONG_PTR ulUIParam
);
```

## <a name="parameters"></a>Параметры

 _ulFlags_
  
> [in] ���������������; ������ ���� ����� ����.
    
 _ulUIParam_
  
> [in] Handle to the parent window of the dialog box on which the button control appears.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Кнопка управления успешно активирована.
    
## <a name="remarks"></a>Примечания

Метод **IMAPIControl::Activate** выполняет задачи после нажатия пользователем кнопки. После нажатия в рамках обработки таблицы отображения MAPI вызывает  активацию после первого вызова [IMAPIControl::GetState,](imapicontrol-getstate.md) чтобы определить, включена ли кнопка. 
  
Дополнительные сведения о реализации **метода Activate** и других методов [IMAPIControl : IUnknown](imapicontroliunknown.md) см. в реализации [объекта control.](control-object-implementation.md)
  
## <a name="see-also"></a>См. также



[IMAPIControl::GetState](imapicontrol-getstate.md)
  
[IMAPIControl : IUnknown](imapicontroliunknown.md)

