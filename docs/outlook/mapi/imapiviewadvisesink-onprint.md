---
title: Имапивиевадвисесинконпринт
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
ms.openlocfilehash: e66315042f8b5cd5aff0e4aa076588c9f312376a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406173"
---
# <a name="imapiviewadvisesinkonprint"></a>IMAPIViewAdviseSink::OnPrint

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Уведомляет средство просмотра форм о состоянии печати формы.
  
```cpp
HRESULT OnPrint(
ULONG dwPageNumber,
HRESULT hrStatus
);
```

## <a name="parameters"></a>Параметры

 _Двпаженумбер_
  
> возврата Номер последней напечатанной страницы.
    
 _Хрстатус_
  
> возврата Значение HRESULT, указывающее состояние задания печати. Возможные значения:
    
S_FALSE 
  
> Задание печати успешно завершено.
    
S_OK 
  
> Выполняется задание печати.
    
СБОЕВ 
  
> Задание печати прервано из-за ошибки.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Уведомление успешно установлено.
    
МАПИ_Е_УСЕР_КАНЦЕЛ 
  
> Пользователь отменил операцию, как правило, нажав кнопку Отмена в диалоговом окне. 
    
## <a name="remarks"></a>Примечания

Объекты форм вызывают метод **имапивиевадвисесинк:: OnPrint** при печати для информирования средства просмотра о ходе печати. 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Если задание печати включает несколько страниц, вы можете вызвать функцию **OnPrint** после печати каждой страницы. Задайте для _двпаженумбер_ страницу, которая печатается в данный момент, и _ХРСТАТУС_ в значение S_OK. После завершения задания печати вызовите функцию **OnPrint** с _двпаженумбер_ , установленной на последнюю страницу, и _хрстатус_ значение S_FALSE. 
  
Дополнительные сведения об уведомлениях формы можно найти в статье [Отправка и получение уведомлений формы](sending-and-receiving-form-notifications.md).
  
## <a name="see-also"></a>См. также



[IMAPIViewAdviseSink : IUnknown](imapiviewadvisesinkiunknown.md)

