---
title: LEFT Function (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1021757
localization_priority: Normal
ms.assetid: 0c2f6e06-b772-2006-ec7b-8695d097f146
description: Возвращает самый левый символ или символы в текстовой строке в соответствии с указанным количеством символов.
ms.openlocfilehash: aa4141cfc53bd41a6d58e8bc666b18a06fc80245
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427523"
---
# <a name="left-function-visioshapesheet"></a>LEFT Function (VisioShapeSheet)

Возвращает самый левый символ или символы в текстовой строке в соответствии с указанным количеством символов.
  
## <a name="syntax"></a>Синтаксис

Left (* * *Text* * *, [, * * *num_chars_opt* * *]) 
  
### <a name="parameters"></a>Параметры

|**Имя**|**Необходимость**|**Тип данных**|**Описание**|
|:-----|:-----|:-----|:-----|
| _text_ <br/> |Обязательный  <br/> |**String** <br/> |Текстовая строка, содержащая символы, которые необходимо извлечь.  <br/> |
| _num_chars_opt_ <br/> |Необязательный  <br/> |**Числовой** <br/> |Число знаков, которое необходимо извлечь.  <br/> |
   
### <a name="return-value"></a>Возвращаемое значение

String
  
## <a name="remarks"></a>Примечания

Значение _num_chars_opt_ должно быть больше или равно нулю (0). 
  
Если _num_chars_opt_ больше, чем длина текста, то Left возвращает весь текст. Если параметр _num_chars_opt_ опущен, предполагается, что он равен 1. 
  
## <a name="example"></a>Пример

LEFT ("1 января, 2004", 3) 
  
Возвращает значение "Jan". 
  

