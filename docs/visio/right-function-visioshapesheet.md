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
description: Возвращает последний символ или символы в текстовой строке в соответствии с указанным количеством символов.
ms.openlocfilehash: faf14ef55b34e51bac11129d6857e381d07357c7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326728"
---
# <a name="right-function-visioshapesheet"></a>RIGHT Function (VisioShapeSheet)

Возвращает последний символ или символы в текстовой строке в соответствии с указанным количеством символов.
  
## <a name="syntax"></a>Синтаксис

Right (* * *Text* * * [, * * *нум_чарс_опт* * *]) 
  
### <a name="parameters"></a>Параметры

|**Имя**|**Необходимость**|**Тип данных**|**Описание**|
|:-----|:-----|:-----|:-----|
| _text_ <br/> |Обязательный  <br/> |**String** <br/> | Текстовая строка, содержащая символы, которые необходимо извлечь.  <br/> |
| _нум_чарс_опт_ <br/> |Необязательный  <br/> |**Number** <br/> |Число знаков, которое необходимо извлечь. По умолчанию используется значение 1.  <br/> |
   
### <a name="return-value"></a>Возвращаемое значение

Строка
  
## <a name="remarks"></a>Замечания

Значение _нум_чарс_опт_ должно быть больше или равно нулю (0). 
  
Если _нум_чарс_опт_ больше, чем длина текста, то право возвращает весь текст. Если _нум_чарс_опт_ опущено, предполагается, что он равен 1. 
  
## <a name="example"></a>Пример

RIGHT ("1 января, 2004", 4) 
  
Возвращает значение 2004. 
  

