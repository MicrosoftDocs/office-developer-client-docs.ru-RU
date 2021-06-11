---
title: MID Function (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1027310
localization_priority: Normal
ms.assetid: 5041d957-1bd9-4d76-cf43-7b4fcd1e7dec
description: Возвращает определенное количество символов из строки текста, начиная с определенной позиции, в зависимости от количества символов, которые вы указываете.
ms.openlocfilehash: 58d5e784e49c8e9fba0bf668626049298783c158
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410268"
---
# <a name="mid-function-visioshapesheet"></a>MID Function (VisioShapeSheet)

Возвращает определенное количество символов из строки текста, начиная с определенной позиции, в зависимости от количества символов, которые вы указываете.
  
## <a name="syntax"></a>Синтаксис

MID (** *text* **, ** *start_num* **, ** *num_chars* ** ) 
  
### <a name="parameters"></a>Параметры

|**Имя**|**Необходимость**|**Тип данных**|**Описание**|
|:-----|:-----|:-----|:-----|
| _text_ <br/> |Обязательный  <br/> |**String** <br/> |Текстовая строка, содержаная символы, которые необходимо извлечь.  <br/> |
| _start_num_ <br/> |Обязательный  <br/> |**Number** <br/> |Положение первого символа, который необходимо извлечь. Первый символ в строке текста — позиция 1.  <br/> |
| _num_chars_ <br/> |Обязательный  <br/> |**Number** <br/> |Количество возвращаемого символа.  <br/> |
   
### <a name="return-value"></a>Возвращаемое значение

String
  
## <a name="remarks"></a>Примечания

Если *start_num:* 
  
- Больше, чем длина  *текста,*  MID возвращает "" (пустой текст). 
    
- Меньше, чем длина *текста,* но start_num плюс *num_chars* превышает длину *текста,* MID возвращает символы до конца  *текста* . 
    
- Менее 1, MID возвращает #VALUE! значение ошибки. 
    
Если  *num_chars*  отрицательный, MID возвращает #VALUE! значение ошибки. 
  
## <a name="example"></a>Пример

MID ("SSN 999-99-9999",5,11) 
  
Возвращает 999-99-9999. 
  

