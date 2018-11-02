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
ms.openlocfilehash: 7f330ef3099175dde88bec2de3512a3c4af1db49
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22580686"
---
# <a name="imapicontrolactivate"></a>IMAPIControl::Activate

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Выполняет задачи, как отображение диалогового окна или запуск программный операции при нажатии элемента управления кнопка пользователе клиентского приложения.
  
```cpp
HRESULT Activate(
  ULONG ulFlags,
  ULONG_PTR ulUIParam
);
```

## <a name="parameters"></a>���������

 _ulFlags_
  
> [in] ���������������; ������ ���� ����� ����.
    
 _ulUIParam_
  
> [in] Дескриптор родительского окна диалоговое окно, на котором отображается элемент управления button.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Элемент управления button успешно активирована.
    
## <a name="remarks"></a>Примечания

Метод **IMAPIControl::Activate** выполняет задачи, после щелчка элемента управления button. После завершения нажмите кнопку как часть обработки в таблице отображения MAPI выполняется вызов **активировать** после первого вызова [IMAPIControl::GetState](imapicontrol-getstate.md) для определения, включено ли кнопки. 
  
Дополнительные сведения о реализации **активировать** , а другой [IMAPIControl: IUnknown](imapicontroliunknown.md) методы, видеть [Реализации объекта элемента управления](control-object-implementation.md).
  
## <a name="see-also"></a>См. также



[IMAPIControl::GetState](imapicontrol-getstate.md)
  
[IMAPIControl : IUnknown](imapicontroliunknown.md)

