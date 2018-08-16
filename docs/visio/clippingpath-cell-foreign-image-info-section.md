---
title: Ячейка ClippingPath (раздел "Сведения о внешнем изображении")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 0ec70417-5b23-45af-95a0-1b26f6791699
description: Содержит ссылку на геометрии путь, заключенное изображения.
ms.openlocfilehash: 9f1c159e303c1d7bc3467c36756a422a3f325c7b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813385"
---
# <a name="clippingpath-cell-foreign-image-info-section"></a>Ячейка ClippingPath (раздел "Сведения о внешнем изображении")

Содержит ссылку на геометрии путь, заключенное изображения. 
  
## <a name="remarks"></a>Замечания

Если ячейка **ClippingPath** указывает допустимый путь, изображение обрезается, чтобы изображения отображается в пути. Если ячейка **ClippingPath** пуст или содержит недопустимый запись, изображения будет отображаться с прямоугольной картинок, с помощью значения масштабирования и смещение. 
  
> [!NOTE]
> Только пути, определенные в раздел [геометрии](geometry-section.md) в таблице свойств фигуры изображения, вводимых в ячейке **ClippingPath** . Ссылки на разных листах не может использоваться для определения пути отсечения изображения. 
  
Для получения ссылки на ячейки **ClippingPath** по имени из другой формулы, по значению атрибута **N** элемент **ячейки** и программы, с помощью свойства **CellsU** , используйте: 
  
|||
|:-----|:-----|
| Имя ячейки.  <br/> | ClippingPath  <br/> |
   
Для получения ссылки на ячейки **ClippingPath** по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionObject** <br/> |
| Индекс строки:  <br/> |**visRowForeign** <br/> |
| Индекс ячейки:  <br/> |**visFrgnImgClippingPath** <br/> |
   
## <a name="example"></a>Пример

Можно переместить ограничивающего фигуры изображение овала, выполнив следующие:
  
- Вставьте рисунок на полотно.
    
- Щелкните правой кнопкой мыши изображение и выберите пункт **Показать таблицу свойств фигуры**.
    
- Щелкните правой кнопкой мыши в таблице свойств фигуры и выберите **Вставить раздел**.
    
- В диалоговом окне **Вставить раздел,** выберите **геометрии** и нажмите кнопку **ОК**.
    
- Удалите только один строку, в новый раздел геометрии (например, «Geometry2»).
    
- Щелкните правой кнопкой мыши оставшиеся строки и нажмите кнопку **Изменить тип строки**.
    
- В диалоговом окне **Изменение типа строки** выберите **эллипс** и нажмите кнопку **ОК**.
    
- В разделе **Внешний рисунок** задать формулу для ячейки **ClippingPath** для `="Geometry2.Path"` и примите формулу. 
    
