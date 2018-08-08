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
ms.openlocfilehash: 954630b0b92772d961dc61084c28a9ab419e4c2f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808523"
---
# <a name="ftsubft"></a>FtSubFt

  
  
**Относится к**: Outlook 
  
Вычитает один 64-разрядных целых чисел из другого. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapiutil.h  <br/> |
|Реализованный:  <br/> |MAPI  <br/> |
|Вызывается:  <br/> |Клиентские приложения и поставщиков услуг  <br/> |
   
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
    
## <a name="return-value"></a>������������ ��������

Функция **FtSubFt** возвращает структуру **FILETIME** , содержащую результат вычитания. Два входных параметра не изменяются. 
  

