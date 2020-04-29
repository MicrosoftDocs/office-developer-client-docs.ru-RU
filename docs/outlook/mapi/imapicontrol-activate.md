---
title: имапиконтролактивате
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
  
Выполняет задачу, например отображение диалогового окна или запуск программной операции, когда пользователь клиентского приложения щелкает элемент управления "Кнопка".
  
```cpp
HRESULT Activate(
  ULONG ulFlags,
  ULONG_PTR ulUIParam
);
```

## <a name="parameters"></a>Параметры

 _ulFlags_
  
> [in] ���������������; ������ ���� ����� ����.
    
 _улуипарам_
  
> возврата Дескриптор родительского окна диалогового окна, в котором отображается элемент управления "Кнопка".
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Элемент управления "Кнопка" успешно активирован.
    
## <a name="remarks"></a>Примечания

Метод **имапиконтрол:: Activate** выполняет задачи после нажатия пользователем кнопки элемента управления "Кнопка". После выполнения щелчка в рамках обработки отображаемой таблицы MAPI вызывает **активацию** после первого вызова [имапиконтрол::-State](imapicontrol-getstate.md) , чтобы определить, включена ли кнопка. 
  
Дополнительные сведения о том, как реализовать **активацию** и другие методы [имапиконтрол: IUnknown](imapicontroliunknown.md) , можно найти в разделе [Реализация объекта Control](control-object-implementation.md).
  
## <a name="see-also"></a>См. также



[IMAPIControl::GetState](imapicontrol-getstate.md)
  
[IMAPIControl : IUnknown](imapicontroliunknown.md)

