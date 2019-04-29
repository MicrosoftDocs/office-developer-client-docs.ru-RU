---
title: FtSubFt
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FtSubFt
api_type:
- COM
ms.assetid: 6619fc41-5518-44ce-85c1-6b0077ed5cb9
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: edd789a586adc71289ff821aa7cf7a33f79fb738
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408420"
---
# <a name="ftsubft"></a>FtSubFt

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
ВыЧитает одно целое число без знака (64) из другого. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Мапиутил. h  <br/> |
|Реализовано в:  <br/> |MAPI  <br/> |
|Вызывающая сторона:  <br/> |Клиентские приложения и поставщики услуг  <br/> |
   
```cpp
FILETIME FtSubFt(
  FILETIME Minuend,
  FILETIME Subtrahend
);
```

## <a name="parameters"></a>Параметры

 _Минуенд_
  
> возврата Структура [fileTime](filetime.md) , которая содержит неподписанное 64-разрядное целое число, из которого значение параметра _субтрахенд_ должно вычитаться. 
    
 _Субтрахенд_
  
> возврата Структура **fileTime** , которая содержит неподписанное 64-разрядное целое число, которое вычитается из значения, указанного с помощью параметра _минуенд_ . 
    
## <a name="return-value"></a>Возвращаемое значение

Функция **фтсубфт** возвращает структуру **fileTime** , которая содержит результат вычитания. Два входных параметра остаются неизменными. 
  

