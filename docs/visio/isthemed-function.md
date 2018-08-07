---
title: Функция ISTHEMED
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 91cde601-dca9-4737-afe1-bdf76638dfe3
description: Возвращает логическое значение, указывающее, имеет ли фигуры темы, примененной к нему.
ms.openlocfilehash: 4311780d8686b5792e999c204ec182d23efb723c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814023"
---
# <a name="isthemed-function"></a>Функция ISTHEMED

Возвращает логическое значение, указывающее, имеет ли фигуры темы, примененной к нему. 
  
## <a name="version-information"></a>Сведения о версии

Добавлена версия: Visio 2013
 
  
## <a name="syntax"></a>Синтаксис

 **ISTHEMED** ()
  
## <a name="return-value"></a>������������ ��������

Логический
  
## <a name="remarks"></a>Замечания

> [!NOTE]
> Функция **ISTHEMED** в Visio 2013 заменяет функцию **CELLISTHEMED** из предыдущих версий Visio. 
  
**ISTHEMED** функция позволяет назначить соответствующие части форматирование темы фигуры, но сохранить возможность переопределить другим частям форматирования с помощью вручную применить форматирование темы. Если впоследствии применения темы, вручную форматирования имеет преимущество и фигуры принимает все форматирование темы. 
  
 **ISTHEMED** имеет значение TRUE, если ячейка [ColorSchemeIndex](colorschemeindex-cell-theme-properties-section.md) в фигуре больше 0. Если эта ячейка равно 0, **ISTHEMED** принимает значение FALSE. Темы DocumentSheet и PageSheet не влияет на значение **ISTHEMED** функции, используемые в таблице свойств фигуры. Только в том случае, если функция **ISTHEMED** отображаемым на PageSheet не данному темы страницы. 
  
## <a name="example"></a>Пример

||||
|:-----|:-----|:-----|
|Cell  <br/> |Формула  <br/> |Результат  <br/> |
|Char.Font  <br/> |IF(ISTHEMED(), THEMEVAL(), FONT("Calibri"))  <br/> |Если фигура имеет темой применяется к нему, текст фигуры принимает параметры темы шрифта. Если фигура не является темой, с помощью шрифта «Calibri» форматирования текста фигуры.  <br/> |
|Цвет линии  <br/> |ЕСЛИ (ISTHEMED, RGB (255, 0, 0), RGB (0, 255, 0))  <br/> |Если фигура имеет темой применяется к нему, красный цвет линии фигуры. Если фигура не является темой, зеленый цвет линии фигуры.  <br/> |
   

