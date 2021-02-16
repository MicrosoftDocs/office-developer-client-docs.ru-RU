---
title: RIGHT Function (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1027314
localization_priority: Normal
ms.assetid: 910f0297-d588-2048-f308-03f3c2389bba
description: Возвращает последний символ или символы в текстовой строке в зависимости от количества символов, которые вы указываете.
ms.openlocfilehash: faf14ef55b34e51bac11129d6857e381d07357c7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411458"
---
# <a name="right-function-visioshapesheet"></a>RIGHT Function (VisioShapeSheet)

Возвращает последний символ или символы в текстовой строке в зависимости от количества символов, которые вы указываете.
  
## <a name="syntax"></a>Синтаксис

RIGHT(** *text* ** [, ** *num_chars_opt* ** ]) 
  
### <a name="parameters"></a>Параметры

|**Имя**|**Необходимость**|**Тип данных**|**Описание**|
|:-----|:-----|:-----|:-----|
| _text_ <br/> |Обязательно  <br/> |**Строка** <br/> | Текстовая строка, содержащая символы, которые нужно извлечь.  <br/> |
| _num_chars_opt_ <br/> |Необязательна  <br/> |**Number** <br/> |Количество символов, которые нужно извлечь. По умолчанию используется значение 1.  <br/> |
   
### <a name="return-value"></a>Возвращаемое значение

String
  
## <a name="remarks"></a>Примечания

Значение num_chars_opt  должно быть больше или равно нулю (0). 
  
Если  _num_chars_opt_ больше длины текста, right возвращает весь текст. Если  _num_chars_opt_ опущен, предполагается, что это 1. 
  
## <a name="example"></a>Пример

RIGHT (1 января 2004 г., 4) 
  
Возвращает значение 2004. 
  

