---
title: FtAddFt
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FtAddFt
api_type:
- COM
ms.assetid: 341ad06b-1caa-49bb-b859-cb512f6fb55d
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: cb20469adec938817fedf1b00789304625b388c8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404766"
---
# <a name="ftaddft"></a>FtAddFt

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Добавляет одно неподписаное 64-битное 64-битное в другое.
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapiutil.h  <br/> |
|Реализовано в:  <br/> |MAPI  <br/> |
|Вызывающая сторона:  <br/> |Клиентские приложения и поставщики услуг  <br/> |
   
```cpp
FILETIME FtAddFt(
  FILETIME Addend1,
  FILETIME Addend2
);
```

## <a name="parameters"></a>Параметры

 _Addend1_
  
> [in] Структура [FILETIME,](filetime.md) которая содержит первое неподписаное 64-битное количество, которое необходимо добавить. 
    
 _Addend2_
  
> [in] Структура **FILETIME,** которая содержит второе неподписаное 64-битное 64-битное количество, которое необходимо добавить. 
    
## <a name="return-value"></a>Возвращаемое значение

Функция **FtAddFt** возвращает структуру **FILETIME,** которая содержит сумму двух integers. Два входных параметра остаются без изменений. 
  

