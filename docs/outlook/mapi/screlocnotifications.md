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
ms.openlocfilehash: bb4ff6a128b9fed29ff0be5325c21e5600389740
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812240"
---
# <a name="screlocnotifications"></a>ScRelocNotifications

  
  
**Относится к**: Outlook 
  
Изменяет указатель в массиве указанного события уведомления. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapiutil.h  <br/> |
|Реализованный:  <br/> |MAPI  <br/> |
|Вызывается:  <br/> |Клиентские приложения и поставщиков услуг  <br/> |
   
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

 _cntf_
  
> [in] Число структур [УВЕДОМЛЕНИЙ](notification.md) в массива, указанного в параметре _rgntf_ . 
    
 _rgntf_
  
> [in] Указатель на массив структур **УВЕДОМЛЕНИЙ** , определение уведомления о событиях, в течение которых является указатель для настройки. 
    
 _pvBaseOld_
  
> [in] Указатель на исходный базовый адрес массива, указанного в параметре _rgntf_ . 
    
 _pvBaseNew_
  
> [in] Расположение, к которому **ScRelocNotifications** записывает новый базовый адрес массива, указанного в параметре _rgntf_ . 
    
 _печатной_
  
> [out] Указатель на размер, в байтах, массива, указанного в параметре _pvBaseNew_ . 
    
## <a name="return-value"></a>������������ ��������

ЗНАЧЕНИЕ S_OK
  
> Указатель был успешно изменены.
    
MAPI_E_INVALID_PARAMETER
  
> Обнаружен недопустимый уведомлений.
    
## <a name="remarks"></a>Замечания

Это необязательный параметр _печатной_ в функцию **ScRelocNotifications** . 
  
## <a name="see-also"></a>См. также



[ScRelocProps](screlocprops.md)

