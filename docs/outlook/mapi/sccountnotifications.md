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

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Определяет размер (в байтах) массива уведомлений о событиях и проверяет память, связанную с массивом.
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Мапиутил. h  <br/> |
|Реализовано в:  <br/> |MAPI  <br/> |
|Вызывающая сторона:  <br/> |Клиентские приложения и поставщики услуг  <br/> |
   
```cpp
SCODE ScCountNotifications(
  int cntf,
  LPNOTIFICATION rgntf,
  ULONG FAR * pcb
);
```

## <a name="parameters"></a>Параметры

 _кнтф_
  
> возврата Количество структур [уведомлений](notification.md) в массиве, указанном с помощью параметра _ргнтф_ . 
    
 _ргнтф_
  
> возврата Указатель на массив структур **уведомлений** , размер которых необходимо определить. 
    
 _пкб_
  
> вышли Необязательный указатель размера массива (в байтах), на который указывает параметр _ргнтф_ . Если значение равно NULL, **сккаунтнотификатионс** проверяет массив уведомлений. 
    
## <a name="return-value"></a>Возвращаемое значение

S_OK
  
> Число успешно определено.
    
MAPI_E_INVALID_PARAMETER
  
> Обнаружено недопустимое уведомление.
    
## <a name="remarks"></a>Примечания

Если в параметре _ПКБ_ передается значение null, функция **сккаунтнотификатионс** только проверяет массив уведомлений, но подсчет не выполняется; Если в _ПКБ_передается значение, отличное от NULL, **сккаунтнотификатионс** определяет размер массива и сохраняет ошибку _ПКБ_. Параметр _ПКБ_ должен быть достаточно большим, чтобы вместить весь массив. 
  

