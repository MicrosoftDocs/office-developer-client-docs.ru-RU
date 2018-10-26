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
ms.openlocfilehash: ad561bd3be7fd0c9f25c11875f62667563dfcbe7
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22578264"
---
# <a name="ftsubft"></a>FtSubFt

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Вычитает один 64-разрядных целых чисел из другого. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapiutil.h  <br/> |
|Реализовано в:  <br/> |MAPI  <br/> |
|Вызывающая сторона:  <br/> |Клиентские приложения и поставщиков услуг  <br/> |
   
```cpp
FILETIME FtSubFt(
  FILETIME Minuend,
  FILETIME Subtrahend
);
```

## <a name="parameters"></a>Параметры

 _Уменьшаемое_
  
> [in] Структура [FILETIME](filetime.md) , содержащую целых 64-разрядная версия, из которой должна быть вычитается значение с помощью параметра _вычитаемое_ . 
    
 _Вычитаемое_
  
> [in] Структура **FILETIME** , содержащую целых 64-разрядная версия, вычитается из значения, указанного параметром _Уменьшаемое_ . 
    
## <a name="return-value"></a>Возвращаемое значение

Функция **FtSubFt** возвращает структуру **FILETIME** , содержащую результат вычитания. Два входных параметра не изменяются. 
  

