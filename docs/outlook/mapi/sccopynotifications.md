---
title: ScCopyNotifications
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.ScCopyNotifications
api_type:
- COM
ms.assetid: ac31cf65-a2bc-4c8e-91a4-d2903aa98776
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 7d4877c81a52b529aa183ea552430b481c6617f1
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22593356"
---
# <a name="sccopynotifications"></a>ScCopyNotifications

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Группа уведомлений о событиях копируется на один блок памяти. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapiutil.h  <br/> |
|Реализованный:  <br/> |MAPI  <br/> |
|Вызывается:  <br/> |Клиентские приложения и поставщиков услуг  <br/> |
   
```cpp
SCODE ScCopyNotifications(
  int cntf,
  LPNOTIFICATION rgntf,
  LPVOID pvDst,
  ULONG FAR * pcb
);
```

## <a name="parameters"></a>Параметры

 _cntf_
  
> [in] Число структур [УВЕДОМЛЕНИЙ](notification.md) в массива, указанного в параметре _rgntf_ . 
    
 _rgntf_
  
> [in] Указатель на массив структур **УВЕДОМЛЕНИЙ** , определение уведомления о событиях для копирования. 
    
 _pvDst_
  
> [out] Указатель на возвращенные уведомления. 
    
 _печатной_
  
> [out] Необязательный указатель на переменную, где размер в байтах, массива, на который указывает с помощью параметра _rgntf_ сохраняется. Если это не имеет значение NULL, параметр _печатной_ число байтов, сохраненных в параметре _pvDst_ . 
    
## <a name="return-value"></a>������������ ��������

ЗНАЧЕНИЕ S_OK
  
> Уведомления о событиях были успешно скопированы.
    
E_INVALIDARG
  
> Обнаружен недопустимый уведомлений.
    
## <a name="remarks"></a>Замечания

Если в параметре _печатной_ передано значение NULL, не копирование не выполняется. Если ненулевое значение передается в _печатной_, функция **ScCopyNotifications** копирует размер массива и самого массива на один блок памяти. Если _печатной_ не равно NULL, перейдут в число байтов, сохраненных в параметре _pvDst_ . Параметр _pvDst_ должен быть достаточно большим для размещения всего массива. 
  

