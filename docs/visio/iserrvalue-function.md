---
title: Функция ISERRVALUE
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251453
localization_priority: Normal
ms.assetid: c7feec6f-f47a-60ee-b056-7b2dc51ed9a9
description: 'Возвращает значение TRUE, если значение ссылка_на_ячейку Ошибка типа #VALUE, где аргумент в формуле имеет неверный тип. Функция ISERRVALUE используется в логических выражениях, которые ссылаются на другую ячейку.'
ms.openlocfilehash: 50c501cc404d9c5f80e0bd1261b3d3bcd7087de2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814000"
---
# <a name="iserrvalue-function"></a>Функция ISERRVALUE

Возвращает значение TRUE, если значение _ссылка_на_ячейку_ Ошибка типа #VALUE, где аргумент в формуле имеет неверный тип. Функция ISERRVALUE используется в логических выражениях, которые ссылаются на другую ячейку. 
  
## <a name="syntax"></a>Синтаксис

ISERRVALUE (** *ссылка_на_ячейку* **) 
  
### <a name="parameters"></a>Параметры

|**Имя**|**Обязательный или необязательный**|**Тип данных**|**Описание**|
|:-----|:-----|:-----|:-----|
| _ссылка_на_ячейку_ <br/> |Обязательный  <br/> |**Строка** <br/> |Ссылка на ячейку.  <br/> |
   
## <a name="remarks"></a>Замечания

Вспомогательный ячейки, которые буквы от A до D не возвращают #VALUE! Ошибка может содержать формулы и цифр в ту же строку. Ячейки X и Y должно содержать только цифры. 
  
## <a name="example-1"></a>Пример 1

|**Cell**|**Формулы**|**Возвращаемое значение**|
|:-----|:-----|:-----|
|Scratch.X1  <br/> |= «Дом»  <br/> |#VALUE!  <br/> |
|Scratch.A1  <br/> |= Если (ISERRVALUE(Scratch.X1),2,Scratch.X1)  <br/> |2  <br/> |
   
Возвращает 2, так как возвращаемое значение является #VALUE! Ошибка и выражение указывает, что Microsoft Visio для возврата 2 вместо ошибки.
  
## <a name="example-2"></a>Пример 2

|**Cell**|**Формулы**|**Возвращаемое значение**|
|:-----|:-----|:-----|
|Scratch.A1  <br/> |= «5 + 7»  <br/> |5 + 7  <br/> |
|Scratch.B1  <br/> |= Если (ISERRVALUE(Scratch.A1),2,Scratch.A1)  <br/> |5 + 7  <br/> |
   
Возвращает 12 так как возвращаемое значение не является #VALUE! Ошибка и выражение указывает, что Visio для возврата значения первой ячейки.
  

