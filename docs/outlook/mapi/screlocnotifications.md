---
title: ScRelocNotifications
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.ScRelocNotifications
api_type:
- COM
ms.assetid: 22de5d38-7be6-48b3-90a7-bc553dcdb042
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 81da4b77f0d2162a1119b7945b1e0ceb87ba9fb8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415203"
---
# <a name="screlocnotifications"></a>ScRelocNotifications

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Настраивает указатель в указанном массиве уведомлений о событиях. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapiutil.h  <br/> |
|Реализовано в:  <br/> |MAPI  <br/> |
|Вызывающая сторона:  <br/> |Клиентские приложения и поставщики услуг  <br/> |
   
```cpp
SCODE ScRelocNotifications(
  int cntf,
  LPNOTIFICATION rgntf,
  LPVOID pvBaseOld,
  LPVOID pvBaseNew,
  ULONG FAR * pcb
);
```

## <a name="parameters"></a>Parameters

 _cntf_
  
> [in] Количество [структур УВЕДОМЛЕНий](notification.md) в массиве, указанных параметром _rgntf._ 
    
 _rgntf_
  
> [in] Указатель на массив структур **УВЕДОМЛЕНий,** определяющих уведомления о событиях, в рамках которых должен быть скорректирован указатель. 
    
 _pvBaseOld_
  
> [in] Указатель на исходный базовый адрес массива, указанный _параметром rgntf._ 
    
 _pvBaseNew_
  
> [in] Расположение, в которое **ScRelocNotifications** записывает новый базовый адрес массива, указанный _параметром rgntf._ 
    
 _pcb_
  
> [вышел] Указатель на размер в bytes массива, указанный _параметром pvBaseNew._ 
    
## <a name="return-value"></a>Возвращаемое значение

S_OK
  
> Указатель был успешно скорректирован.
    
MAPI_E_INVALID_PARAMETER
  
> Недействительное уведомление было встречено.
    
## <a name="remarks"></a>Примечания

Параметр  _pcb_ для **функции ScRelocNotifications** необязателен. 
  
## <a name="see-also"></a>См. также



[ScRelocProps](screlocprops.md)

