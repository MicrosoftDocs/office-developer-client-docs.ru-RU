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
ms.openlocfilehash: 08b9b954f856d64214947d81cf700adee42bcce4
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435924"
---
# <a name="sccopynotifications"></a>ScCopyNotifications

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Копирует группу уведомлений о событиях в один блок памяти. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapiutil.h  <br/> |
|Реализовано в:  <br/> |MAPI  <br/> |
|Вызывающая сторона:  <br/> |Клиентские приложения и поставщики услуг  <br/> |
   
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
  
> [in] Количество структур [NOTIFICATION](notification.md) в массиве, указанных параметром _rgntf._ 
    
 _rgntf_
  
> [in] Указатель на массив структур **УВЕДОМЛЕНий,** определяющих уведомления о событиях, которые необходимо скопировать. 
    
 _pvDst_
  
> [out] Указатель на возвращенные уведомления. 
    
 _pcb_
  
> [out] Необязательный указатель на переменную, в которой хранится размер массива, на который указывает параметр  _rgntf_ , в вайтах. Если это не NULL, для параметра _pcb_ устанавливается количество вбайт, хранимых в _параметре pvDst._ 
    
## <a name="return-value"></a>Возвращаемое значение

S_OK
  
> Уведомления о событиях были успешно скопированы.
    
E_INVALIDARG
  
> Было выявилось недопустимое уведомление.
    
## <a name="remarks"></a>Примечания

Если в параметре  _PCB_ передается NULL, копирование не выполняется; Если в  _pcb_ передается ненулевое значение, функция **ScCopyNotifications** копирует размер массива и самого массива в один блок памяти. Если _pcb_ не имеет NULL, ему задано количество данных, хранимых в _параметре pvDst._ Параметр  _pvDst_ должен быть достаточно большим, чтобы содержать весь массив. 
  

