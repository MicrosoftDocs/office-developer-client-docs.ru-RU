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
description: Возвращает высоту текста в фигуры, где в строке не превышает maximumwidth.
ms.openlocfilehash: 9a80dafcf80a1dcba968a0f60465aae4e2a2758b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815006"
---
# <a name="textheight-function"></a>Функция TEXTHEIGHT

Возвращает высоту текста в фигуры, где в строке не превышает _maximumwidth_. 
  
## <a name="syntax"></a>Синтаксис

TEXTHEIGHT (** указанной фигуре *! TheText* ** ** *[, maximumwidth]* **) 
  
### <a name="parameters"></a>Параметры

|**Имя**|**Обязательный или необязательный**|**Тип данных**|**Описание**|
|:-----|:-----|:-----|:-----|
| _указанной фигуре! theText_ <br/> |Обязательный  <br/> |**Строка** <br/> |Ссылка на ячейку с именем TheText в конечную фигуру.  _указанной фигуре!_ — Это имя фигуры, из которого требуется получить текст.  <br/> |
| _MaximumWidth_ <br/> |Optional  <br/> |**Числовой** <br/> |Максимальная ширина блока текста.  <br/> |
   
### <a name="return-value"></a>������������ ��������

Строка
  
## <a name="remarks"></a>Замечания

Возвращаемое значение включает в себя высота текста, включая пробел до и после текста, междустрочным интервалом в текст и верхние и нижние поля блока текста. Эта функция обычно используется для настройки высоты фигуры в соответствии с текстом, которые он содержит.
  
## <a name="example"></a>Пример

TEXTHEIGHT (TheText, (ширина - 0,5)) 
  
Возвращает высоту текста при переносятся ширину фигуры минус 0,5 дюйма. 
  

