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
ms.openlocfilehash: 923864c625cb032c3b351bb999ff7cc782eae588
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22567169"
---
# <a name="sccountnotifications"></a>ScCountNotifications

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Определяет размер, в байтах, массива уведомления о событиях и проверки памяти, связанной с массивом.
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapiutil.h  <br/> |
|Реализованный:  <br/> |MAPI  <br/> |
|Вызывается:  <br/> |Клиентские приложения и поставщиков услуг  <br/> |
   
```cpp
SCODE ScCountNotifications(
  int cntf,
  LPNOTIFICATION rgntf,
  ULONG FAR * pcb
);
```

## <a name="parameters"></a>Параметры

 _cntf_
  
> [in] Число структур [УВЕДОМЛЕНИЙ](notification.md) в массива, указанного в параметре _rgntf_ . 
    
 _rgntf_
  
> [in] Указатель на массив структур **УВЕДОМЛЕНИЙ** , размер которого является будет определено. 
    
 _печатной_
  
> [out] Необязательный указатель на размер, в байтах, массива, на который указывает параметр _rgntf_ . Если значение NULL, **ScCountNotifications** проверяет массива уведомлений. 
    
## <a name="return-value"></a>������������ ��������

ЗНАЧЕНИЕ S_OK
  
> Число успешно определены.
    
MAPI_E_INVALID_PARAMETER
  
> Обнаружен недопустимый уведомлений.
    
## <a name="remarks"></a>Замечания

Если с помощью параметра _печатной_ передано значение NULL, функция **ScCountNotifications** проверяет только массива уведомления, но не подсчет выполняется; Если ненулевое значение передается в _печатной_, **ScCountNotifications** определяет размер массива и сохраняет несколько _печатной_. Параметр _печатной_ должен быть достаточно большим для размещения всего массива. 
  

