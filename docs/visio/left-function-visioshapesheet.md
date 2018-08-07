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
description: Возвращает левые знаки в текстовой строке, на основе числа символов.
ms.openlocfilehash: 4e8deb3098ce6d217dcce0cae23d07ed723d9fb8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814063"
---
# <a name="left-function-visioshapesheet"></a>LEFT Function (VisioShapeSheet)

Возвращает левые знаки в текстовой строке, на основе числа символов.
  
## <a name="syntax"></a>Синтаксис

СЛЕВА (** *текст* **, [, ** *num_chars_opt* **]) 
  
### <a name="parameters"></a>Параметры

|**Имя**|**Обязательный или необязательный**|**Тип данных**|**Описание**|
|:-----|:-----|:-----|:-----|
| _text_ <br/> |Обязательный  <br/> |**Строка** <br/> |Текстовая строка, содержащая знаки, которые вы хотите извлечь.  <br/> |
| _num_chars_opt_ <br/> |Optional  <br/> |**Числовой** <br/> |Число знаков, которое вы хотите извлечь.  <br/> |
   
### <a name="return-value"></a>������������ ��������

Строка
  
## <a name="remarks"></a>Замечания

Значение _num_chars_opt_ должно быть больше или равно нулю (0). 
  
Если _num_chars_opt_ больше, чем длина текста, ЛЕВСИМВ возвращает весь текст. Если _num_chars_opt_ указан, предполагается 1. 
  
## <a name="example"></a>Пример

СЛЕВА («1 января 2004», 3) 
  
Возвращает значение «Янв». 
  

