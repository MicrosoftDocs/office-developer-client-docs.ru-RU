---
title: Функция TEXTHEIGHT
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251504
localization_priority: Normal
ms.assetid: 5a10892f-c8fa-c127-2f5a-564009ce5411
description: Возвращает высоту составного текста в фигуре, где ни одна текстовая строка не превышает максимальное значение.
ms.openlocfilehash: 7455f58f14f9a4a0ae1fcd5375dba5d5860d3852
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427411"
---
# <a name="textheight-function"></a>Функция TEXTHEIGHT

Возвращает высоту составного текста в фигуре, где ни одна текстовая строка не превышает _максимальное значение._ 
  
## <a name="syntax"></a>Синтаксис

TEXTHEIGHT(** *shapename! TheText* ** ** *[,maximumwidth]* ** ) 
  
### <a name="parameters"></a>Параметры

|**Имя**|**Необходимость**|**Тип данных**|**Описание**|
|:-----|:-----|:-----|:-----|
| _shapename!theText_ <br/> |Обязательно  <br/> |**Строка** <br/> |Ссылка на ячейку с именем TheText в целевой фигуре.  _shapename!_ — имя фигуры, из которой вы хотите получить текст.  <br/> |
| _maximumwidth_ <br/> |Необязательный  <br/> |**Числовой** <br/> |Максимальная ширина текстового блока.  <br/> |
   
### <a name="return-value"></a>Возвращаемое значение

String
  
## <a name="remarks"></a>Примечания

Возвращаемая величина включает высоту текста, включая пробел до и после текста, интервал строки в тексте, а также верхний и нижний блоки текста. Эта функция обычно используется для настройки высоты фигуры в виде текста, который она содержит.
  
## <a name="example"></a>Пример

TEXTHEIGHT(TheText,(Width - 0.5 in)) 
  
Возвращает высоту текста при оболочке по ширине фигуры минус 0,5 дюйма. 
  

