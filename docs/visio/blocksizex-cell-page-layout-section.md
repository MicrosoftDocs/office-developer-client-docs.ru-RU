---
title: BlockSizeX Cell (Page Layout Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm105
localization_priority: Normal
ms.assetid: 253aac17-077e-48e0-39a8-a3abd5d4a257
description: Определяет горизонтальный размер блока, область, в которой каждая из фигур должна поместиться на странице рисования при раскладке фигур с помощью диалогового окна Configure Layout (на вкладке Design в группе Layout нажмите кнопку Re-Layout Page, а затем нажмите кнопку Дополнительные параметры макета).
ms.openlocfilehash: 8e4cee4b2059d9b8f2fe77c2d4902e67246eac2f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424191"
---
# <a name="blocksizex-cell-page-layout-section"></a>BlockSizeX Cell (Page Layout Section)

Определяет горизонтальный размер блока, область, в которой каждая из фигур должна поместиться на странице рисования при раскладке фигур с помощью диалогового окна **Configure** **Layout**(на вкладке Design, в группе **Layout,** щелкните страницу повторного макета **и** нажмите кнопку Дополнительные параметры макета). 
  
## <a name="remarks"></a>Примечания

Вы также можете установить  это значение в диалоговом окне  Макет и Маршрутинг интервалов (на вкладке Дизайн щелкните стрелку в группе установки страницы, щелкните вкладку Макет и маршрутизацию, а затем щелкните **Spacing).**  
  
Чтобы получить ссылку на ячейку BlockSizeX по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте: 
  
|||
|:-----|:-----|
|Имя ячейки:  <br/> |BlockSizeX  <br/> |
   
Чтобы получить ссылку на ячейку BlockSizeX по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionObject** <br/> |
| Индекс строки:  <br/> |**visRowPageLayout** <br/> |
| Индекс ячейки:  <br/> |**visPLOBlockSizeX** <br/> |
   

