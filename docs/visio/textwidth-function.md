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

TEXTWIDTH(** *shapename! TheText* ** ** *[,maximumwidth]* ** ) 
  
### <a name="parameters"></a>Параметры

|**Имя**|**Необходимость**|**Тип данных**|**Описание**|
|:-----|:-----|:-----|:-----|
| _shapename!theText_ <br/> |Обязательно  <br/> |**Строка** <br/> |Ссылка на ячейку с именем TheText в целевой фигуре.  _shapename!_ — имя фигуры, из которой вы хотите получить текст.  <br/> |
| _maximumwidth_ <br/> |Необязательный  <br/> |**Числовой** <br/> |Максимальная ширина текстового блока.  <br/> |
   
### <a name="return-value"></a>Возвращаемое значение

String
  
## <a name="remarks"></a>Примечания

Функция TEXTWIDTH обычно используется для настройки ширины фигуры в виде текста, который она содержит.
  
If  _sheetN!_ опущен, фигурой по умолчанию является текущая фигура. 
  
Если указано значение  _maximumwidth,_ результатом будет самая длинная строка текста, которая соответствует  _максимальному объему_ текста. Если  _значение maximumwidth_ опущено, результатом будет общая ширина текста. 
  
## <a name="example"></a>Пример

TEXTWIDTH(TheText) 
  
Возвращает общую длину текста в текущей фигуре. 
  

