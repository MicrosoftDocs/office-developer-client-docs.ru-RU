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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309466"
---
# <a name="left-function-visioshapesheet"></a>LEFT Function (VisioShapeSheet)

Возвращает самый левый символ или символы в текстовой строке в соответствии с указанным количеством символов.
  
## <a name="syntax"></a>Синтаксис

Left (* * *Text* * *, [, * * *нум_чарс_опт* * *]) 
  
### <a name="parameters"></a>Параметры

|**Имя**|**Необходимость**|**Тип данных**|**Описание**|
|:-----|:-----|:-----|:-----|
| _text_ <br/> |Обязательный  <br/> |**String** <br/> |Текстовая строка, содержащая символы, которые необходимо извлечь.  <br/> |
| _нум_чарс_опт_ <br/> |Необязательный  <br/> |**Числовой** <br/> |Число знаков, которое необходимо извлечь.  <br/> |
   
### <a name="return-value"></a>Возвращаемое значение

Строка
  
## <a name="remarks"></a>Замечания

Значение _нум_чарс_опт_ должно быть больше или равно нулю (0). 
  
Если _нум_чарс_опт_ больше, чем длина текста, то Left возвращает весь текст. Если _нум_чарс_опт_ опущено, предполагается, что он равен 1. 
  
## <a name="example"></a>Пример

LEFT ("1 января, 2004", 3) 
  
Возвращает значение "Jan". 
  

