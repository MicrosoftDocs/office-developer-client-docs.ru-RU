---
title: Функция ISTHEMED
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 91cde601-dca9-4737-afe1-bdf76638dfe3
description: Возвращает значение boolean, указывающее, применяется ли к фигуре тема.
ms.openlocfilehash: 49f53eaaacbdc86a633703d6ef847e38097f5122
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418122"
---
# <a name="isthemed-function"></a>Функция ISTHEMED

Возвращает значение boolean, указывающее, применяется ли к фигуре тема. 
  
## <a name="version-information"></a>Сведения о версии

Добавлена версия: Visio 2013
 
  
## <a name="syntax"></a>Синтаксис

 **ISTHEMED**()
  
## <a name="return-value"></a>Возвращаемое значение

Boolean
  
## <a name="remarks"></a>Примечания

> [!NOTE]
> Функция **ISTHEMED** в Visio 2013 заменяет функцию **CELLISTHEMED** из предыдущих версий Visio. 
  
Функция **ISTHEMED** позволяет назначать фигуре соответствующие части форматирования темы, но сохраняет возможность переопределять другие части форматирования темы с помощью ручного форматирования. Если впоследствии вы повторно примесь к теме, любое ручное форматирование переопределяется и фигура принимает все форматирование темы. 
  
 **IsTHEMED** оценивается как TRUE, если [ячейка ColorSchemeIndex](colorschemeindex-cell-theme-properties-section.md) в фигуре больше 0. Если эта ячейка равна 0, **isTHEMED** оценивается как FALSE. Тема таблицы документов и таблицы страниц не влияет на значение функции **ISTHEMED,** используемой в shapeSheet. Только если функция **ISTHEMED** появляется в листе PageSheet, тема страницы имеет значение. 
  
## <a name="example"></a>Пример

||||
|:-----|:-----|:-----|
|Cell  <br/> |Формула  <br/> |Результат  <br/> |
|Char.Font  <br/> |IF(ISTHEMED(), THEMEVAL(), FONT("Calibri"))  <br/> |Если к фигуре применена тема, текст фигуры принимает форматирование шрифта из темы. Если фигура не является темой, текст фигуры форматирован шрифтом Calibri.  <br/> |
|LineColor  <br/> |IF(ISTHEMED, RGB(255, 0, 0), RGB(0, 255, 0))  <br/> |Если к фигуре применена тема, цвет линии фигуры красный. Если фигура не является темой, цвет линии фигуры зеленый.  <br/> |
   

