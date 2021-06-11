---
title: Функция LUM
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251460
localization_priority: Normal
ms.assetid: 38e6bba7-1bf2-3d31-0912-707002454f5d
description: Возвращает значение компонента светоносности цвета.
ms.openlocfilehash: 17fa43f8e2cd7422428f92724e351436233c2d62
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419340"
---
# <a name="lum-function"></a>Функция LUM

Возвращает значение компонента светоносности цвета.
  
## <a name="syntax"></a>Синтаксис

Выражение LUM(**  ** ) 
  
### <a name="parameters"></a>Параметры

|**Имя**|**Необходимость**|**Тип данных**|**Описание**|
|:-----|:-----|:-----|:-----|
| _expression_ <br/> |Обязательный  <br/> |**Числовой** <br/> |Индекс цвета в цветовой таблице документа или ссылка на ячейку с индексом цвета.  <br/> |
   
### <a name="return-value"></a>Возвращаемое значение

Номер
  
## <a name="remarks"></a>Примечания

Возвратное значение — это число в диапазоне от 0 до 240 включительно. Функция возвращает 0 для недействительных входных данных. 
  
## <a name="example-1"></a>Пример 1

LUM(Sheet.4! FillForegnd)
  
Возвращает светоносность цвета на переднем плане заполняемого листа.4.
  
## <a name="example-2"></a>Пример 2

LUM(6)
  
Возвращает 120, если в документе используется Visio цветовая палитра, где пурпурный цвет — это цвет в индексе 6.
  
## <a name="example-3"></a>Пример 3

LUM(HSL(10, 20, 30))
  
Возвращает 30.
  

