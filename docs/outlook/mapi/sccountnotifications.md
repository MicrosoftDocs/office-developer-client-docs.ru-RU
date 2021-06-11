---
title: ScCountNotifications
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.ScCountNotifications
api_type:
- COM
ms.assetid: 13e80bdc-cb59-47a5-8de0-404e22f87f82
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: f5298620239d1e42e4ba613c22a98f0cf6f7d457
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437996"
---
# <a name="sccountnotifications"></a>ScCountNotifications

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Определяет размер в bytes массива уведомлений о событиях и проверяет память, связанную с массивом.
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapiutil.h  <br/> |
|Реализовано в:  <br/> |MAPI  <br/> |
|Вызывающая сторона:  <br/> |Клиентские приложения и поставщики услуг  <br/> |
   
```cpp
SCODE ScCountNotifications(
  int cntf,
  LPNOTIFICATION rgntf,
  ULONG FAR * pcb
);
```

## <a name="parameters"></a>Parameters

 _cntf_
  
> [in] Количество [структур УВЕДОМЛЕНий](notification.md) в массиве, указанных параметром _rgntf._ 
    
 _rgntf_
  
> [in] Указатель на массив структур **NOTIFICATION,** размер которых должен быть определен. 
    
 _pcb_
  
> [вышел] Необязательный указатель на размер в bytes массива, указываемого параметром _rgntf._ Если NULL, **ScCountNotifications** проверяет массив уведомлений. 
    
## <a name="return-value"></a>Возвращаемое значение

S_OK
  
> Граф был определен успешно.
    
MAPI_E_INVALID_PARAMETER
  
> Недействительное уведомление было встречено.
    
## <a name="remarks"></a>Примечания

Если NULL передается в _параметре pcb,_ функция **ScCountNotifications** проверяет только массив уведомлений, но подсчет не делается; если значение non-null передается в _pcb,_ **ScCountNotifications** определяет размер массива и сохраняет причину _pcb._ Параметр  _PCB_ должен быть достаточно большим, чтобы содержать весь массив. 
  

