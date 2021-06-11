---
title: Функция THEMEVAL
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 9eac3b8c-532c-4312-935d-fe8b63bcaf75
description: Извлекает значения из активной темы.
ms.openlocfilehash: ba95b8a920174ee44c0349d7227258d3ee8a843c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415756"
---
# <a name="themeval-function"></a>Функция THEMEVAL

Извлекает значения из активной темы. 
  
## <a name="version-information"></a>Сведения о версии

Добавлена версия: Visio 2013
 
  
## <a name="syntax"></a>Синтаксис

 **THEMEVAL**([ _"theme_value"_][, _по умолчанию_]) 
  
### <a name="parameters"></a>Параметры

|**Имя**|**Необходимость**|**Тип данных**|**Описание**|
|:-----|:-----|:-----|:-----|
| _"theme_value"_ <br/> |Необязательный  <br/> |**String** <br/> |Имя ячейки в определении темы для получения значения.  <br/> |
| _default_ <br/> |Необязательный  <br/> |Разное  <br/> |Значение по умолчанию, если документ не является тематическим (определение темы не существует).  <br/> |
   
## <a name="remarks"></a>Примечания

Если функция **THEMEVAL** не получает никаких аргументов, она возвращает тематического значения ячейки хост. Это значение хранится в определении текущей темы. Ячейка хост должна быть способна быть темой для возврата значения; если ячейка не может быть тематическим, **THEMEVAL** возвращает ошибку. 
  
Если функция **THEMEVAL** получает один аргумент, она извлекает значение из определения темы, переданного в качестве аргумента. Аргументом, переданным для первого параметра, должен быть ряд или одна из точных строк, перечисленных в таблице ниже. 
  
Функция **THEMEVAL** также может принимать в качестве значения от 1 до 8 значение для первого параметра. Использование значений в несколько часов извлекает цвет по индексу из цветовой схемы темы. Таким образом, значение "1" возвращает цвет "Темный" из темы, "2" возвращает цвет "Светлый", "3" возвращает цвет "Accent 1" и т. д. 
  
Если функция **THEMEVAL** получает два аргумента, она извлекает значение из определения темы, переданного в качестве первого аргумента. Однако если в документе нет примененной к ней темы, то функция **THEMEVAL** использует значение, указанное в качестве второго аргумента. 
  
**Возможные аргументы для параметра "theme_value"**

|**Значение**|**Описание**|
|:-----|:-----|
|"Темный"  <br/> |Извлекает цвет Dark RGB из определения темы.  <br/> |
|"Light"  <br/> |Извлекает цвет Light RGB из определения темы.  <br/> |
|"BackgroundColor"  <br/> |Извлекает фоновый RGB-цвет из определения темы.  <br/> |
|"AccentColor"  <br/> |Извлекает цвет Accent1 RGB из определения темы.  <br/> |
|"AccentColor2"  <br/> |Извлекает цвет Accent2 RGB из определения темы.  <br/> |
|"AccentColor3"  <br/> |Извлекает цвет Accent3 RGB из определения темы.  <br/> |
|"AccentColor4"  <br/> |Извлекает цвет Accent4 RGB из определения темы.  <br/> |
|"AccentColor5"  <br/> |Извлекает цвет Accent5 RGB из определения темы.  <br/> |
|"AccentColor6"  <br/> |Извлекает цвет Accent6 RGB из определения темы.  <br/> |
|"LinePattern"  <br/> |Извлекает значение ячейки LinePattern из определения темы.  <br/> |
|"LineWeight"  <br/> |Извлекает значение ячейки LineWeight из определения темы.  <br/> |
|"LineColor"  <br/> |Извлекает значение ячейки LineColor из определения темы.  <br/> |
|"LineCap"  <br/> |Извлекает значение ячейки LineCap из определения темы.  <br/> |
|"LineBegin"  <br/> |Извлекает значение ячейки BeginArrow из определения темы.  <br/> |
|"LineEnd"  <br/> |Извлекает значение ячейки EndArrow из определения темы.  <br/> |
|"LineColorTrans"  <br/> |Извлекает значение ячейки LineColorTrans из определения темы.  <br/> |
|"LineCompoundtype"  <br/> |Извлекает значение ячейки CompoundType из определения темы.  <br/> |
|"LineBegin"  <br/> |Извлекает значение ячейки BeginArrow из определения темы.  <br/> |
|"LineEnd"  <br/> |Извлекает значение ячейки EndArrow из определения темы.  <br/> |
|"LineBeginSize"  <br/> |Извлекает значение ячейки BeginArrowSize из определения темы.  <br/> |
|"LineEndSize"  <br/> |Извлекает значение ячейки EndArrowSize из определения темы.  <br/> |
|"LineRounding"  <br/> |Извлекает значение ячейки Округление из определения темы.  <br/> |
|"ConnectorColor"  <br/> |Извлекает значение ячейки LineColor из определения темы.  <br/> |
|"ConnectorPattern"  <br/> |Извлекает значение ячейки LinePattern из определения темы.  <br/> |
|"ConnectorWeight"  <br/> |Извлекает значение ячейки LineWeight из определения темы.  <br/> |
|"ConnectorTransparency"  <br/> |Извлекает значение ячейки LineColorTrans из определения темы.  <br/> |
|"ConnectorRounding"  <br/> |Извлекает значение ячейки Округление из определения темы.  <br/> |
|"ConnectorBegin"  <br/> |Извлекает значение ячейки BeginArrow из определения темы.  <br/> |
|"ConnectorEnd"  <br/> |Извлекает значение ячейки EndArrow из определения темы.  <br/> |
|"ConnectorBeginSize"  <br/> |Извлекает значение ячейки BeginArrowSize из определения темы.  <br/> |
|"ConnectorEndSize"  <br/> |Извлекает значение ячейки EndArrowSize из определения темы.  <br/> |
|"FillColor"  <br/> |Извлекает значение ячейки FillForegnd из определения темы.  <br/> |
|"FillColor2"  <br/> |Извлекает значение ячейки FillBkgnd из определения темы.  <br/> |
|"FillTransparency"  <br/> |Извлекает значение ячейки FillForegndTrans из определения темы.  <br/> |
|"FillPattern"  <br/> |Извлекает значение ячейки FillPattern из определения темы.  <br/> |
|"LineGradientEnabled"  <br/> |Извлекает значение ячейки LineGradientEnabled из определения темы.  <br/> |
|"LineGradientDir"  <br/> |Извлекает значение ячейки LineGradientDir из определения темы.  <br/> |
|"LineGradientAngle"  <br/> |Извлекает значение ячейки LineGradientAngle из определения темы.  <br/> |
|"FillGradientEnabled"  <br/> |Извлекает значение ячейки FillGradientEnabled из определения темы.  <br/> |
|"FillGradientDir"  <br/> |Извлекает значение ячейки FillGradientDir из определения темы.  <br/> |
|"FillGradientAngle"  <br/> |Извлекает значение ячейки FillGradientAngle из определения темы.  <br/> |
|"RotateGradientWithShape"  <br/> |Извлекает значение ячейки RotateGradientWithShape из определения темы.  <br/> |
|"UseGroupGradient"  <br/> |Извлекает значение ячейки UseGroupGradient из определения темы.  <br/> |
|"ShadowType"  <br/> |Извлекает значение ячейки ShapeShdwType из определения темы.  <br/> |
|"ShadowColor"  <br/> |Извлекает значение ячейки ShdwColor из определения темы.  <br/> |
|"ShadowTransparency"  <br/> |Извлекает значение ячейки ShdwColorTrans из определения темы.  <br/> |
|"ShadowMagnification"  <br/> |Извлекает значение ячейки ShapeShdwScaleFactor из определения темы.  <br/> |
|"ShadowBlur"  <br/> |Извлекает значение ячейки ShapeShdwBlur из определения темы.  <br/> |
|"ShadowXOffset"  <br/> |Извлекает значение ячейки ShapeShdwOffsetX из определения темы.  <br/> |
|"ShadowYOffset"  <br/> |Извлекает значение ячейки ShapeShdwOffsetY из определения темы.  <br/> |
|"ShadowDirection"  <br/> |Извлекает значение ячейки ShapeShdwObliqueAngle из определения темы.  <br/> |
|"ShadowPattern"  <br/> |Извлекает значение ячейки ShdwPattern из определения темы.  <br/> |
|"BevelTopType"  <br/> |Извлекает значение ячейки BevelTopType из определения темы.  <br/> |
|"BevelTopWidth"  <br/> |Извлекает значение ячейки BevelTopWidth из определения темы.  <br/> |
|"BevelTopHeight"  <br/> |Извлекает значение ячейки BevelTopHeight из определения темы.  <br/> |
|"BevelMaterial"  <br/> |Извлекает значение ячейки BevelMaterialType из определения темы.  <br/> |
|"BevelLighting"  <br/> |Извлекает значение ячейки BevelLightingType из определения темы.  <br/> |
|"BevelLightingAngle"  <br/> |Извлекает значение ячейки BevelLightingAngle из определения темы.  <br/> |
|"BevelContourColor"  <br/> |Извлекает значение ячейки BevelContourColor из определения темы.  <br/> |
|"BevelContourSize"  <br/> |Извлекает значение ячейки BevelContourSize из определения темы.  <br/> |
|"ReflectionBlur"  <br/> |Извлекает значение ячейки ReflectionBlur из определения темы.  <br/> |
|"ReflectionDist"  <br/> |Извлекает значение ячейки ReflectionDist из определения темы.  <br/> |
|"ReflectionSize"  <br/> |Извлекает значение ReflectionSize ячейки из определения темы.  <br/> |
|"ReflectionTrans"  <br/> |Извлекает значение ячейки ReflectionTrans из определения темы.  <br/> |
|"SoftEdgesSize"  <br/> |Извлекает значение ячейки SoftEdgesSize из определения темы.  <br/> |
|"GlowSize"  <br/> |Извлекает значение ячейки GlowSize из определения темы.  <br/> |
|"GlowColor"  <br/> |Извлекает значение ячейки GlowColor из определения темы.  <br/> |
|"GlowTransparency"  <br/> |Извлекает значение ячейки GlowColorTrans из определения темы.  <br/> |
|"SketchAmount"  <br/> |Извлекает значение ячейки SketchAmount из определения темы.  <br/> |
|"SketchEnabled"  <br/> |Извлекает значение ячейки SketchEnabled из определения темы.  <br/> |
|"SketchFillChange"  <br/> |Извлекает значение ячейки SketchFillChange из определения темы.  <br/> |
|"SketchLineChange"  <br/> |Извлекает значение ячейки SketchLineChange из определения темы.  <br/> |
|"SketchLineWeight"  <br/> |Извлекает значение ячейки SketchLineWeight из определения темы.  <br/> |
|"LatinFont"  <br/> |Извлекает значение ячейки Font из определения темы.  <br/> |
|"TextColor"  <br/> |Извлекает значение ячейки Color из определения темы.  <br/> |
|"TextStyle"  <br/> |Извлекает значение ячейки Character.Style из определения темы.  <br/> |
|"ComplexFont"  <br/> |Извлекает значение ячейки ComplexScriptFont из определения темы.  <br/> |
|"AsianFont"  <br/> |Извлекает значение ячейки AsianFont из определения темы.  <br/> |
|"FillStop[x]Color"  <br/> |Извлекает значение ячейки Color в строке  *x из*  определения темы.  <br/> |
|"FillStop[x]Transparency"  <br/> |Извлекает значение ячейки ColorTrans в строке  *x из*  определения темы.  <br/> |
|"FillStop[x]Position"  <br/> |Извлекает значение ячейки Position в строке  *x из*  определения темы.  <br/> |
|"LineStop[x]Color"  <br/> |Извлекает значение ячейки Color в строке  *x из*  определения темы.  <br/> |
|"LineStop[x]Transparency"  <br/> |Извлекает значение ячейки ColorTrans в строке  *x из*  определения темы.  <br/> |
|"LineStop[x]Position"  <br/> |Извлекает значение ячейки Position в строке  *x из*  определения темы.  <br/> |
   
## <a name="example"></a>Пример

 `THEMEVAL("5")`
  
Возвращает цвет "Accent 3" из определения темы.
  
 `THEMEVAL("LineWeight", "0.7 pt.")`
  
Возвращает значение ячейки "LineWeight" из определения темы. Если фигура, содержащая эту функцию, не имеет примененной к ней темы, функция возвращает "0.7 pt.".
  

