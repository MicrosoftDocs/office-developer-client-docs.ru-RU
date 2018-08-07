---
title: Функция THEMEVAL
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 9eac3b8c-532c-4312-935d-fe8b63bcaf75
description: Получает значения из активной темы.
ms.openlocfilehash: 7bbd017c859a0a167bbd279d60af029e98421375
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815031"
---
# <a name="themeval-function"></a>Функция THEMEVAL

Получает значения из активной темы. 
  
## <a name="version-information"></a>Сведения о версии

Добавлена версия: Visio 2013
 
  
## <a name="syntax"></a>Синтаксис

 **THEMEVAL** ([ _«theme_value»_] [, _по умолчанию_]) 
  
### <a name="parameters"></a>Параметры

|**Имя**|**Обязательный или необязательный**|**Тип данных**|**Описание**|
|:-----|:-----|:-----|:-----|
| _«theme_value»_ <br/> |Optional  <br/> |**Строка** <br/> |Имя определения темы для получения значения из ячейки.  <br/> |
| _default_ <br/> |Optional  <br/> |Разное  <br/> |Значение по умолчанию, если документ не является темой (нет нет определения темы).  <br/> |
   
## <a name="remarks"></a>Замечания

Если функция **THEMEVAL** не получает все аргументы, возвращает темой значение ячейки узла. Это значение, хранящееся в определении текущей темы. Ячейка узла должен быть способен к которым применяются темы для возврата значения; Если ячейки не может переходить темой, **THEMEVAL** возвращает ошибку. 
  
Если функция **THEMEVAL** получает один аргумент, он получает значение из определения темы, переданной в качестве аргумента. Аргумент передано в качестве первого параметра должен быть целым числом или одно точное строк, перечисленные в следующей таблице. 
  
Функция **THEMEVAL** также может принимать целое число для первого параметра, как в диапазоне от 1 до 8. С помощью целые значения получает цвет, индекса из цветовая схема темы. Таким образом возвращает значение "1", «Темный» цвет из темы, "2" возвращает цвет «Недоступно», "3" возвращает цвет «Акцент 1", и т.д. 
  
Если функция **THEMEVAL** получает два аргумента, он получает значение из определения темы, переданной в качестве первого аргумента. Тем не менее если в документе есть нет темы, примененных к нему, функция **THEMEVAL** использует значение, указанное в качестве аргумента второй. 
  
**Возможные аргументы для параметра «theme_value»**

|**Значение**|**Описание**|
|:-----|:-----|
|«Темный»  <br/> |Получает RGB темный цвет из определения темы.  <br/> |
|«Недоступно»  <br/> |Получает цвета Light RGB из определения темы.  <br/> |
|«BackgroundColor»  <br/> |Получает цвет фона RGB из определения темы.  <br/> |
|«AccentColor»  <br/> |Получает цвета RGB акцент 1 из определения темы.  <br/> |
|«AccentColor2»  <br/> |Получает цвета Accent2 RGB из определения темы.  <br/> |
|«AccentColor3»  <br/> |Получает цвета Accent3 RGB из определения темы.  <br/> |
|«AccentColor4»  <br/> |Получает цвета Accent4 RGB из определения темы.  <br/> |
|«AccentColor5»  <br/> |Получает цвета Accent5 RGB из определения темы.  <br/> |
|«AccentColor6»  <br/> |Получает цвета Accent6 RGB из определения темы.  <br/> |
|«LinePattern»  <br/> |Получает значение ячейки LinePattern из определения темы.  <br/> |
|«Толщина линии»  <br/> |Получает значение ячейки Толщина линии из определения темы.  <br/> |
|«Цвет линии»  <br/> |Получает значение ячейки цвет линии из определения темы.  <br/> |
|«LineCap»  <br/> |Получает значение ячейки LineCap из определения темы.  <br/> |
|«LineBegin»  <br/> |Получает значение ячейки BeginArrow из определения темы.  <br/> |
|«LineEnd»  <br/> |Получает значение ячейки EndArrow из определения темы.  <br/> |
|«LineColorTrans»  <br/> |Получает значение ячейки LineColorTrans из определения темы.  <br/> |
|«LineCompoundtype»  <br/> |Получает значение ячейки CompoundType из определения темы.  <br/> |
|«LineBegin»  <br/> |Получает значение ячейки BeginArrow из определения темы.  <br/> |
|«LineEnd»  <br/> |Получает значение ячейки EndArrow из определения темы.  <br/> |
|«LineBeginSize»  <br/> |Получает значение ячейки BeginArrowSize из определения темы.  <br/> |
|«LineEndSize»  <br/> |Получает значение ячейки EndArrowSize из определения темы.  <br/> |
|«LineRounding»  <br/> |Получает значение ячейки округление из определения темы.  <br/> |
|«ConnectorColor»  <br/> |Получает значение ячейки цвет линии из определения темы.  <br/> |
|«ConnectorPattern»  <br/> |Получает значение ячейки LinePattern из определения темы.  <br/> |
|«ConnectorWeight»  <br/> |Получает значение ячейки Толщина линии из определения темы.  <br/> |
|«ConnectorTransparency»  <br/> |Получает значение ячейки LineColorTrans из определения темы.  <br/> |
|«ConnectorRounding»  <br/> |Получает значение ячейки округление из определения темы.  <br/> |
|«ConnectorBegin»  <br/> |Получает значение ячейки BeginArrow из определения темы.  <br/> |
|«ConnectorEnd»  <br/> |Получает значение ячейки EndArrow из определения темы.  <br/> |
|«ConnectorBeginSize»  <br/> |Получает значение ячейки BeginArrowSize из определения темы.  <br/> |
|«ConnectorEndSize»  <br/> |Получает значение ячейки EndArrowSize из определения темы.  <br/> |
|«FillColor»  <br/> |Получает значение ячейки FillForegnd из определения темы.  <br/> |
|«FillColor2»  <br/> |Получает значение ячейки FillBkgnd из определения темы.  <br/> |
|«FillTransparency»  <br/> |Получает значение ячейки FillForegndTrans из определения темы.  <br/> |
|«Узор заливки»  <br/> |Получает значение ячейки узор заливки из определения темы.  <br/> |
|«LineGradientEnabled»  <br/> |Получает значение ячейки LineGradientEnabled из определения темы.  <br/> |
|«LineGradientDir»  <br/> |Получает значение ячейки LineGradientDir из определения темы.  <br/> |
|«LineGradientAngle»  <br/> |Получает значение ячейки LineGradientAngle из определения темы.  <br/> |
|«FillGradientEnabled»  <br/> |Получает значение ячейки FillGradientEnabled из определения темы.  <br/> |
|«FillGradientDir»  <br/> |Получает значение ячейки FillGradientDir из определения темы.  <br/> |
|«FillGradientAngle»  <br/> |Получает значение ячейки FillGradientAngle из определения темы.  <br/> |
|«RotateGradientWithShape»  <br/> |Получает значение ячейки RotateGradientWithShape из определения темы.  <br/> |
|«UseGroupGradient»  <br/> |Получает значение ячейки UseGroupGradient из определения темы.  <br/> |
|«ShadowType»  <br/> |Получает значение ячейки ShapeShdwType из определения темы.  <br/> |
|«ShadowColor»  <br/> |Получает значение ячейки ShdwColor из определения темы.  <br/> |
|«ShadowTransparency»  <br/> |Получает значение ячейки ShdwColorTrans из определения темы.  <br/> |
|«ShadowMagnification»  <br/> |Получает значение ячейки ShapeShdwScaleFactor из определения темы.  <br/> |
|«ShadowBlur»  <br/> |Получает значение ячейки ShapeShdwBlur из определения темы.  <br/> |
|«ShadowXOffset»  <br/> |Получает значение ячейки ShapeShdwOffsetX из определения темы.  <br/> |
|«ShadowYOffset»  <br/> |Получает значение ячейки ShapeShdwOffsetY из определения темы.  <br/> |
|«ShadowDirection»  <br/> |Получает значение ячейки ShapeShdwObliqueAngle из определения темы.  <br/> |
|«ShadowPattern»  <br/> |Получает значение ячейки ShdwPattern из определения темы.  <br/> |
|«BevelTopType»  <br/> |Получает значение ячейки BevelTopType из определения темы.  <br/> |
|«BevelTopWidth»  <br/> |Получает значение ячейки BevelTopWidth из определения темы.  <br/> |
|«BevelTopHeight»  <br/> |Получает значение ячейки BevelTopHeight из определения темы.  <br/> |
|«BevelMaterial»  <br/> |Получает значение ячейки BevelMaterialType из определения темы.  <br/> |
|«BevelLighting»  <br/> |Получает значение ячейки BevelLightingType из определения темы.  <br/> |
|«BevelLightingAngle»  <br/> |Получает значение ячейки BevelLightingAngle из определения темы.  <br/> |
|«BevelContourColor»  <br/> |Получает значение ячейки BevelContourColor из определения темы.  <br/> |
|«BevelContourSize»  <br/> |Получает значение ячейки BevelContourSize из определения темы.  <br/> |
|«ReflectionBlur»  <br/> |Получает значение ячейки ReflectionBlur из определения темы.  <br/> |
|«ReflectionDist»  <br/> |Получает значение ячейки ReflectionDist из определения темы.  <br/> |
|«ReflectionSize»  <br/> |Получает значение ячейки ReflectionSize из определения темы.  <br/> |
|«ReflectionTrans»  <br/> |Получает значение ячейки ReflectionTrans из определения темы.  <br/> |
|«SoftEdgesSize»  <br/> |Получает значение ячейки SoftEdgesSize из определения темы.  <br/> |
|«GlowSize»  <br/> |Получает значение ячейки GlowSize из определения темы.  <br/> |
|«GlowColor»  <br/> |Получает значение ячейки GlowColor из определения темы.  <br/> |
|«GlowTransparency»  <br/> |Получает значение ячейки GlowColorTrans из определения темы.  <br/> |
|«SketchAmount»  <br/> |Получает значение ячейки SketchAmount из определения темы.  <br/> |
|«SketchEnabled»  <br/> |Получает значение ячейки SketchEnabled из определения темы.  <br/> |
|«SketchFillChange»  <br/> |Получает значение ячейки SketchFillChange из определения темы.  <br/> |
|«SketchLineChange»  <br/> |Получает значение ячейки SketchLineChange из определения темы.  <br/> |
|«SketchLineWeight»  <br/> |Получает значение ячейки SketchLineWeight из определения темы.  <br/> |
|«LatinFont»  <br/> |Получает значение ячейки шрифта из определения темы.  <br/> |
|«TextColor»  <br/> |Получает значение цвета ячеек из определения темы.  <br/> |
|«Стиля текста»  <br/> |Получает значение ячейки Character.Style из определения темы.  <br/> |
|«ComplexFont»  <br/> |Получает значение ячейки ComplexScriptFont из определения темы.  <br/> |
|«AsianFont»  <br/> |Получает значение ячейки AsianFont из определения темы.  <br/> |
|«Цвет FillStop [x]»  <br/> |Получает значение цвета ячеек в строке *x* из определения темы.  <br/> |
|«Прозрачность FillStop [x]»  <br/> |Получает значение ячейки ColorTrans в строке *x* из определения темы.  <br/> |
|«Положение FillStop [x]»  <br/> |Получает значение ячейки позицию в строке *x* из определения темы.  <br/> |
|«Цвет LineStop [x]»  <br/> |Получает значение цвета ячеек в строке *x* из определения темы.  <br/> |
|«Прозрачность LineStop [x]»  <br/> |Получает значение ячейки ColorTrans в строке *x* из определения темы.  <br/> |
|«Положение LineStop [x]»  <br/> |Получает значение ячейки позицию в строке *x* из определения темы.  <br/> |
   
## <a name="example"></a>Пример

 `THEMEVAL("5")`
  
Возвращает «3» цветовую из определения темы.
  
 `THEMEVAL("LineWeight", "0.7 pt.")`
  
Возвращает значение «Толщина линии» ячейки из определения темы. Если нет темы, примененного фигуры, содержащей эту функцию, функция возвращает «0,7 pt.».
  

