---
title: PlowCode Cell (Page Layout Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251660
localization_priority: Normal
ms.assetid: e43f3d29-7def-d36e-ac64-62f0a389d415
description: Определяет, отодвигаются ли фигуры, когда вы уроните фигуру вблизи другой фигуры на странице рисования.
ms.openlocfilehash: 4ea85ddbaf7662305a2a82fc7f0b814019624841
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420355"
---
# <a name="plowcode-cell-page-layout-section"></a>PlowCode Cell (Page Layout Section)

Определяет, отодвигаются ли фигуры, когда вы уроните фигуру вблизи другой фигуры на странице рисования.
  
|**Значение**|**Описание**|**Константа автоматизации**|
|:-----|:-----|:-----|
|0  <br/> |Не перемещайте фигуры  <br/> |**visPLOPlowNone** <br/> |
|1  <br/> |Перемещение фигур  <br/> |**visPLOPlowAll** <br/> |
   
## <a name="remarks"></a>Примечания

Вы также можете установить значение этой ячейки на вкладке  Layout **и Routing** в диалоговом окне Установка страницы (на вкладке Дизайн, щелкните стрелку установки страницы) с помощью перемещения других фигур на поле drop **check** box.   
  
Чтобы получить ссылку на ячейку PlowCode по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте: 
  
|||
|:-----|:-----|
|Имя ячейки:  <br/> |PlowCode  <br/> |
   
Чтобы получить ссылку на ячейку PlowCode по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
|Индекс раздела:  <br/> |**visSectionObject** <br/> |
|Индекс строки:  <br/> |**visRowPageLayout** <br/> |
|Индекс ячейки:  <br/> |**visPLOPlowCode** <br/> |
   

