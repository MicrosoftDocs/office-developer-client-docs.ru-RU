---
title: LineWeight Cell (Line Format Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm585
localization_priority: Normal
ms.assetid: 16b0e293-eeef-34b4-aeb0-4472815dd543
description: Определяет вес строки фигуры. Установите вес строки, введите номер с допустимой единицей измерения.
ms.openlocfilehash: 654a93f939226bedab2e40ab591dad0e3f872267
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412249"
---
# <a name="lineweight-cell-line-format-section"></a>LineWeight Cell (Line Format Section)

Определяет вес строки фигуры. Установите вес строки, введите номер с допустимой единицей измерения.
  
## <a name="remarks"></a>Примечания

Вы также можете задать значение LineWeight в диалоговом окне **Line** (на вкладке Главная, в группе **Shape** нажмите кнопку **Строка,** указать **вес,** а затем нажмите кнопку **Дополнительные линии).** 
  
Если единица измерения не введена, используется единица измерения для текста, указанного в диалоговом **окне Visio Options** (щелкните вкладку **Файл** и нажмите кнопку **Параметры).** Вес строки не зависит от масштаба рисунка. Если рисунок масштабировать, вес строки остается таким же. 
  
Чтобы получить ссылку на ячейку LineWeight по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте: 
  
|||
|:-----|:-----|
| Имя ячейки:  <br/> | LineWeight  <br/> |
   
Чтобы получить ссылку на ячейку LineWeight по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionObject** <br/> |
| Индекс строки:  <br/> |**visRowLine** <br/> |
| Индекс ячейки:  <br/> |**visLineWeight** <br/> |
   

