---
title: Функция TEXTWIDTH
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251505
localization_priority: Normal
ms.assetid: a9b8efcf-edc0-ad99-deae-21df16c58807
description: Возвращает ширину составного текста в фигуре.
ms.openlocfilehash: 43848bba4d24a0c31a3a084d123cd56140bf0709
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422035"
---
# <a name="textwidth-function"></a>Функция TEXTWIDTH

Возвращает ширину составного текста в фигуре. 
  
## <a name="syntax"></a>Синтаксис

TEXTWIDTH (* * *шапенаме! TheText* * * * * *[, максимумвидс]* * *) 
  
### <a name="parameters"></a>Параметры

|**Имя**|**Необходимость**|**Тип данных**|**Описание**|
|:-----|:-----|:-----|:-----|
| _шапенаме! theText_ <br/> |Обязательный  <br/> |**String** <br/> |Ссылка на ячейку с именем TheText в целевой фигуре.  _шапенаме!_ — имя фигуры, из которой требуется получить текст.  <br/> |
| _максимумвидс_ <br/> |Необязательный  <br/> |**Числовой** <br/> |Максимальная ширина блока текста.  <br/> |
   
### <a name="return-value"></a>Возвращаемое значение

String
  
## <a name="remarks"></a>Примечания

Функция TEXTWIDTH обычно используется для настройки ширины фигуры в соответствии с текстом, который она содержит.
  
Если _шитн!_ не указан, фигура по умолчанию — текущая фигура. 
  
Если указан _максимумвидс_ , то результатом является длинная строка текста, соответствующая в _максимумвидс_. Если _максимумвидс_ опущено, то результатом будет общая ширина текста. 
  
## <a name="example"></a>Пример

TEXTWIDTH (TheText) 
  
Возвращает общую длину текста в текущей фигуре. 
  

