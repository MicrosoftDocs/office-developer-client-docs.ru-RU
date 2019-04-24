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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328009"
---
# <a name="ftaddft"></a>FtAddFt

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Добавляет одно целое число без знака 64 в другое.
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Мапиутил. h  <br/> |
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
  
> возврата Структура [fileTime](filetime.md) , содержащая первое 64 – разрядное целое число, которое требуется добавить. 
    
 _Addend2_
  
> возврата Структура **fileTime** , содержащая второе 64 – разрядное целое число, которое требуется добавить. 
    
## <a name="return-value"></a>Возвращаемое значение

Функция **фтаддфт** возвращает структуру **fileTime** , которая содержит сумму двух целых чисел. Два входных параметра остаются неизменными. 
  

