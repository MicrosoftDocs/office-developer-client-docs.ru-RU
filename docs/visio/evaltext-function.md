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
description: Оценивает текст в шапенаме как формулу и возвращает результат.
ms.openlocfilehash: 6600d9d6ddaf630a93fdb5c37639ce50a21a4307
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329052"
---
# <a name="evaltext-function"></a>Функция EVALTEXT

Оценивает текст в _шапенаме_ как формулу и возвращает результат. 
  
## <a name="syntax"></a>Синтаксис

EVALTEXT (* * *шапенаме! theText* * *) 
  
### <a name="parameters"></a>Параметры

|**Имя**|**Необходимость**|**Тип данных**|**Описание**|
|:-----|:-----|:-----|:-----|
| _шапенаме! theText_ <br/> |Обязательный  <br/> |**String** <br/> |Ячейка, вызываемая при изменении композиции текста связанной фигуры.  <br/> |
   
### <a name="return-value"></a>Возвращаемое значение

Строка
  
## <a name="remarks"></a>Комментарии

 _шапенаме_ можно использовать для ссылки на текст фигуры, отличной от текущей фигуры. 
  
Если текст отсутствует, результат равен нулю. Если текст не может быть оценен, функция возвращает сообщение об ошибке.
  
## <a name="example"></a>Пример

EVALTEXT (line. 2! theText) 
  
Оценивает текст, содержащийся в линии фигуры. 2. Например, если строка. 2 содержит "4 ФТ + 0,5 ФТ", возвращает значение 4,5 ФТ. 
  

