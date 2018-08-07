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
description: Возвращает последние знаки текстовой строки, на основе числа символов.
ms.openlocfilehash: e35cc4918809d5f134f9519c01cb3c93407258e1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814609"
---
# <a name="right-function-visioshapesheet"></a>RIGHT Function (VisioShapeSheet)

Возвращает последние знаки текстовой строки, на основе числа символов.
  
## <a name="syntax"></a>Синтаксис

СПРАВА (** *текст* ** [, ** *num_chars_opt* **]) 
  
### <a name="parameters"></a>Параметры

|**Имя**|**Обязательный или необязательный**|**Тип данных**|**Описание**|
|:-----|:-----|:-----|:-----|
| _text_ <br/> |Обязательный  <br/> |**Строка** <br/> | Текстовая строка, содержащая знаки, которые нужно извлечь.  <br/> |
| _num_chars_opt_ <br/> |Optional  <br/> |**Число** <br/> |Число знаков, которое вы хотите извлечь. Значение по умолчанию — 1.  <br/> |
   
### <a name="return-value"></a>������������ ��������

Строка
  
## <a name="remarks"></a>Замечания

Значение _num_chars_opt_ должно быть больше или равно нулю (0). 
  
Если _num_chars_opt_ больше, чем длина текста, ПРАВСИМВ возвращает весь текст. Если _num_chars_opt_ указан, предполагается 1. 
  
## <a name="example"></a>Пример

СПРАВА («1 января 2004», 4) 
  
Возвращает значение 2004 г. 
  

