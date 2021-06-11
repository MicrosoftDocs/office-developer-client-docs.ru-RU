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
description: Возвращает высоту составленного текста в форме, в которой ни одна текстовая строка не превышает максимально допустимого.
ms.openlocfilehash: 7455f58f14f9a4a0ae1fcd5375dba5d5860d3852
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427411"
---
# <a name="textheight-function"></a>Функция TEXTHEIGHT

Возвращает высоту составленного текста в форме, в которой ни одна текстовая строка не превышает _максимально допустимого._ 
  
## <a name="syntax"></a>Синтаксис

TEXTHEIGHT(** *shapename! TheText* ** ** *[,maximumwidth]* ** ) 
  
### <a name="parameters"></a>Параметры

|**Имя**|**Необходимость**|**Тип данных**|**Описание**|
|:-----|:-----|:-----|:-----|
| _shapename!theText_ <br/> |Обязательный  <br/> |**String** <br/> |Ссылка на ячейку с именем TheText в целевой форме.  _shapename!_ это имя фигуры, из которой нужно получить текст.  <br/> |
| _maximumwidth_ <br/> |Необязательный  <br/> |**Числовой** <br/> |Максимальная ширина текстового блока.  <br/> |
   
### <a name="return-value"></a>Возвращаемое значение

String
  
## <a name="remarks"></a>Примечания

Возвращенное значение включает высоту текста, включая пространство до и после текста, интервал строки в тексте, а также поля верхнего и нижнего блоков текста. Эта функция обычно используется для настройки высоты фигуры, чтобы соответствовать тексту, который она содержит.
  
## <a name="example"></a>Пример

TEXTHEIGHT(TheText,(Ширина — 0,5 в)) 
  
Возвращает высоту текста при завернутой в ширину фигуры минус 0,5 дюйма. 
  

