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
description: Оценивает текст в имени фигуры как формулу и возвращает результат.
ms.openlocfilehash: 6600d9d6ddaf630a93fdb5c37639ce50a21a4307
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438360"
---
# <a name="evaltext-function"></a>Функция EVALTEXT

Оценивает текст в  _имени фигуры_ как формулу и возвращает результат. 
  
## <a name="syntax"></a>Синтаксис

EVALTEXT(** *shapename!theText* ** ) 
  
### <a name="parameters"></a>Параметры

|**Имя**|**Необходимость**|**Тип данных**|**Описание**|
|:-----|:-----|:-----|:-----|
| _shapename!theText_ <br/> |Обязательно  <br/> |**Строка** <br/> |Ячейка, активная при смене текстовой композиции связанной фигуры.  <br/> |
   
### <a name="return-value"></a>Возвращаемое значение

String
  
## <a name="remarks"></a>Примечания

 _имя фигуры_ можно использовать для ссылки на текст фигуры, которая не является текущей. 
  
Если текста нет, результат будет нулем. Если не удается оценить текст, функция возвращает ошибку.
  
## <a name="example"></a>Пример

EVALTEXT(Line.2!theText) 
  
Оценивает текст, содержащийся в фигуре Line.2. Например, если Line.2 содержит "4 ft + 0.5 ft", возвращает значение 4,5 ft. 
  

