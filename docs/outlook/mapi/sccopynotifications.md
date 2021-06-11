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

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
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

## <a name="parameters"></a>Parameters

 _cntf_
  
> [in] Количество [структур УВЕДОМЛЕНий](notification.md) в массиве, указанных параметром _rgntf._ 
    
 _rgntf_
  
> [in] Указатель на массив структур **УВЕДОМЛЕНий,** определяющих скопированные уведомления о событиях. 
    
 _pvDst_
  
> [вышел] Указатель на возвращенные уведомления. 
    
 _pcb_
  
> [вышел] Необязательный указатель на переменную, в которой хранится размер в bytes массива, указываемого параметром _rgntf._ Если не NULL, то параметр _PCB_ задан для количества bytes, хранимого в _параметре pvDst._ 
    
## <a name="return-value"></a>Возвращаемое значение

S_OK
  
> Уведомления о событиях были успешно скопированы.
    
E_INVALIDARG
  
> Недействительное уведомление было встречено.
    
## <a name="remarks"></a>Примечания

Если NULL передается в  _параметре PCB,_ копирование не выполняется; Если значение non-null передается в  _pcb,_ функция **ScCopyNotifications** копирует размер массива и сам массив в один блок памяти. Если _pcb не_ является NULL, он задан для количества bytes, хранимого в _параметре pvDst._ Параметр  _pvDst должен_ быть достаточно большим, чтобы содержать весь массив. 
  

