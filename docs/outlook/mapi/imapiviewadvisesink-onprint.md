---
title: IMAPIViewAdviseSinkOnPrint
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIViewAdviseSink.OnPrint
api_type:
- COM
ms.assetid: d16219a0-268c-428d-9f02-4f06eb5b6d7d
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: bf3eee43a70fbc4abf32b60379fc7b191bd9d513
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809235"
---
# <a name="imapiviewadvisesinkonprint"></a>IMAPIViewAdviseSink::OnPrint

  
  
**Относится к**: Outlook 
  
Уведомляет средство просмотра формы из состояния печати формы.
  
```cpp
HRESULT OnPrint(
ULONG dwPageNumber,
HRESULT hrStatus
);
```

## <a name="parameters"></a>Параметры

 _dwPageNumber_
  
> [in] Номер последней страницы при выводе на печать.
    
 _hrStatus_
  
> [in] Значение HRESULT, указывающее состояние задания печати. Возможные значения:
    
S_FALSE 
  
> Задание печати успешно завершено.
    
ЗНАЧЕНИЕ S_OK 
  
> Задание печати находится в стадии разработки.
    
НЕ УДАЛОСЬ 
  
> Задание печати был завершен из-за сбоя.
    
## <a name="return-value"></a>������������ ��������

ЗНАЧЕНИЕ S_OK 
  
> Уведомление успешно завершен.
    
MAPI_E_USER_CANCEL 
  
> Пользователь отменил операцию, как правило, нажав кнопку "Отмена" в диалоговом окне. 
    
## <a name="remarks"></a>Замечания

Объекты формы вызовите метод **IMAPIViewAdviseSink::OnPrint** при печати для оповещения просмотра ход печати. 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Если задание печати состоит из нескольких страниц, можно позвонить **OnPrint** после печати каждой страницы. Значение S_OK _dwPageNumber_ на страницу в настоящее время печатается и _hrStatus_ . По завершении задания печати звонок, **OnPrint** с _dwPageNumber_ к последнему задать страницы при выводе на печать и _hrStatus_ значение S_FALSE. 
  
Дополнительные сведения о уведомлений формы можно [Отправка и получение уведомлений формы](sending-and-receiving-form-notifications.md).
  
## <a name="see-also"></a>См. также



[IMAPIViewAdviseSink : IUnknown](imapiviewadvisesinkiunknown.md)

