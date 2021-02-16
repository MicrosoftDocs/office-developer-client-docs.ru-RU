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
  
Определяет размер массива уведомлений о событиях (в bytes) и проверяет память, связанную с массивом.
  
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

## <a name="parameters"></a>Параметры

 _cntf_
  
> [in] Количество структур [NOTIFICATION](notification.md) в массиве, указанных параметром _rgntf._ 
    
 _rgntf_
  
> [in] Указатель на массив структур **УВЕДОМЛЕНий,** размер которых необходимо определить. 
    
 _pcb_
  
> [out] Необязательный указатель на размер массива,на который указывает параметр  _rgntf_ (в bytes). Если nULL, **ScCountNotifications** проверяет массив уведомлений. 
    
## <a name="return-value"></a>Возвращаемое значение

S_OK
  
> Количество было определено успешно.
    
MAPI_E_INVALID_PARAMETER
  
> Было выявилось недопустимое уведомление.
    
## <a name="remarks"></a>Примечания

Если в параметре _PCB_ передается NULL, функция **ScCountNotifications** проверяет только массив уведомлений, но подсчет не делается; Если в _pcb_ передается ненулевое значение, **ScCountNotifications** определяет размер массива и сохраняет пксб _причины._ Параметр  _pcb_ должен быть достаточно большим, чтобы содержать весь массив. 
  

