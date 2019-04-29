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

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
НаСтраивает указатель в пределах указанного массива уведомлений о событии. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Мапиутил. h  <br/> |
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

## <a name="parameters"></a>Параметры

 _кнтф_
  
> возврата Количество структур [уведомлений](notification.md) в массиве, указанном с помощью параметра _ргнтф_ . 
    
 _ргнтф_
  
> возврата Указатель на массив структур **уведомлений** , определяющий уведомления о событиях, в которых будет корректироваться указатель. 
    
 _Пвбасеолд_
  
> возврата Указатель на исходный базовый адрес массива, указанного параметром _ргнтф_ . 
    
 _Пвбасенев_
  
> возврата Расположение, в которое **скрелокнотификатионс** записывает новый базовый адрес массива, указанного с помощью параметра _ргнтф_ . 
    
 _ПКБ_
  
> вышли Указатель на размер массива (в байтах), указанный параметром _пвбасенев_ . 
    
## <a name="return-value"></a>Возвращаемое значение

S_OK
  
> Указатель был успешно изменен.
    
МАПИ_Е_ИНВАЛИД_ПАРАМЕТЕР
  
> Обнаружено недопустимое уведомление.
    
## <a name="remarks"></a>Примечания

Параметр _ПКБ_ для функции **скрелокнотификатионс** является необязательным. 
  
## <a name="see-also"></a>См. также



[ScRelocProps](screlocprops.md)

