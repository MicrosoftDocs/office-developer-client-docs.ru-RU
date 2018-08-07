---
title: Функция EVALTEXT
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251422
localization_priority: Normal
ms.assetid: c9b5b96c-d8c8-6119-e3f1-a2ce9d7c043e
description: Обрабатывает текст в указанной фигуре формулу, и возвращает результат.
ms.openlocfilehash: 69e79a23faa9d09aa2ad51f83363064b54742152
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813704"
---
# <a name="evaltext-function"></a>Функция EVALTEXT

Обрабатывает текст в _указанной фигуре_ формулу, и возвращает результат. 
  
## <a name="syntax"></a>Синтаксис

EVALTEXT (** *указанной фигуре! theText* **) 
  
### <a name="parameters"></a>Параметры

|**Имя**|**Обязательный или необязательный**|**Тип данных**|**Описание**|
|:-----|:-----|:-----|:-----|
| _указанной фигуре! theText_ <br/> |Обязательный  <br/> |**Строка** <br/> |Ячейка, выполняемого при изменении связанных с фигурой текстовой композиции.  <br/> |
   
### <a name="return-value"></a>������������ ��������

Строка
  
## <a name="remarks"></a>Замечания

 _указанной фигуре_ можно использовать для обращения к тексту фигуры, отличного от текущего фигуры. 
  
Если не содержит текста, результат равно нулю. Если не может обрабатываться в текст, функция возвращает ошибку.
  
## <a name="example"></a>Пример

EVALTEXT(Line.2!theText) 
  
Оценивает текст, содержащийся в Line.2 фигуры. Например, если Line.2 содержит «4 ft + 0,5 ft», возвращает значение 4,5 ft. 
  

