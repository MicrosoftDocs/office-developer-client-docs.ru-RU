---
title: BlockSizeY Cell (Page Layout Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm110
localization_priority: Normal
ms.assetid: be51e18e-ea49-0788-1a17-866090afb9f4
description: Определяет размер вертикального блока, область, в которой каждая из фигур должна поместиться на странице рисования при раскладке фигур с помощью диалогового окна Configure Layout (на вкладке Дизайн в группе Макет нажмите кнопку Re-Layout Page, а затем нажмите кнопку Дополнительные параметры макета).
ms.openlocfilehash: 08f2012bb027267810c21ef253a0073bb42d3a96
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427404"
---
# <a name="blocksizey-cell-page-layout-section"></a>BlockSizeY Cell (Page Layout Section)

Определяет размер вертикального блока, область, в которой каждая из фигур должна поместиться на странице рисования при раскладке фигур, используя диалоговое окно **Configure Layout** (на вкладке Design, в группе  **Макет,** щелкните страницу **повторного** макета, а затем нажмите кнопку Дополнительные параметры макета). 
  
## <a name="remarks"></a>Примечания

Вы также можете установить  это значение в диалоговом окне  Макет и Маршрутинг интервалов (на вкладке Дизайн щелкните стрелку в группе установки страницы, щелкните вкладку Макет и маршрутизацию, а затем щелкните **Spacing).**  
  
Чтобы получить ссылку на ячейку BlockSizeY по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте: 
  
|||
|:-----|:-----|
| Имя ячейки:  <br/> | BlockSizeY  <br/> |
   
Чтобы получить ссылку на ячейку BlockSizeY по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionObject** <br/> |
| Индекс строки:  <br/> |**visRowPageLayout** <br/> |
| Индекс ячейки:  <br/> |**visPLOBlockSizeY** <br/> |
   

