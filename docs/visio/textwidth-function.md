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
description: Возвращает ширину составленного текста в форме.
ms.openlocfilehash: 43848bba4d24a0c31a3a084d123cd56140bf0709
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422035"
---
# <a name="textwidth-function"></a>Функция TEXTWIDTH

Возвращает ширину составленного текста в форме. 
  
## <a name="syntax"></a>Синтаксис

TEXTWIDTH(** *shapename! TheText* ** ** *[,maximumwidth]* ** ) 
  
### <a name="parameters"></a>Параметры

|**Имя**|**Необходимость**|**Тип данных**|**Описание**|
|:-----|:-----|:-----|:-----|
| _shapename!theText_ <br/> |Обязательный  <br/> |**String** <br/> |Ссылка на ячейку с именем TheText в целевой форме.  _shapename!_ это имя фигуры, из которой нужно получить текст.  <br/> |
| _maximumwidth_ <br/> |Необязательный  <br/> |**Числовой** <br/> |Максимальная ширина текстового блока.  <br/> |
   
### <a name="return-value"></a>Возвращаемое значение

String
  
## <a name="remarks"></a>Примечания

Функция TEXTWIDTH обычно используется для настройки ширины фигуры, чтобы соответствовать тексту, который она содержит.
  
Если  _sheetN!_ опущен, фигура по умолчанию — это текущая форма. 
  
Если _задано_ максимальное значение, результат — это самая длинная строка текста, которая соответствует _максимальному объему._ Если  _значение maximumwidth_ пропущено, результатом является общая ширина текста. 
  
## <a name="example"></a>Пример

TEXTWIDTH (TheText) 
  
Возвращает общую длину текста в текущей форме. 
  

