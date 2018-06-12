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
description: Возвращает ширину текста в фигуре.
ms.openlocfilehash: d96b9489c08ce38205f8e9ad91e361fcb643c39c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815004"
---
# <a name="textwidth-function"></a>Функция TEXTWIDTH

Возвращает ширину текста в фигуре. 
  
## <a name="syntax"></a>Синтаксис

TEXTWIDTH (** указанной фигуре *! TheText* ** ** *[, maximumwidth]* **) 
  
### <a name="parameters"></a>Параметры

|**Имя**|**Обязательный или необязательный**|**Тип данных**|**Описание**|
|:-----|:-----|:-----|:-----|
| _указанной фигуре! theText_ <br/> |Обязательный  <br/> |**Строка** <br/> |Ссылка на ячейку с именем TheText в конечную фигуру.  _указанной фигуре!_ — Это имя фигуры, из которого требуется получить текст.  <br/> |
| _MaximumWidth_ <br/> |Optional  <br/> |**Числовой** <br/> |Максимальная ширина блока текста.  <br/> |
   
### <a name="return-value"></a>������������ ��������

Строка
  
## <a name="remarks"></a>Замечания

Функция TEXTWIDTH обычно используется для настройки ширины фигуры в соответствии с текстом, которые он содержит.
  
Если _sheetN!_ — Этот параметр опущен, по умолчанию имеет текущей фигуры. 
  
Если указан _maximumwidth_ , результатом будет длинной строки текста, которая помещается в _maximumwidth_. Если _maximumwidth_ опущен, результатом будет общая ширина текста. 
  
## <a name="example"></a>Пример

TEXTWIDTH(TheText) 
  
Возвращает общее длины текста в текущей форме. 
  

