---
title: AddMarkup Cell (Document Properties Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1030801
localization_priority: Normal
ms.assetid: 46146424-b4c9-2240-36c0-19bb35ec51d1
description: Указывает, пересматривается ли документ для разметки.
ms.openlocfilehash: 4e0860639b0d89fce2c35a8947bd5ac00fcc63e5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427635"
---
# <a name="addmarkup-cell-document-properties-section"></a>AddMarkup Cell (Document Properties Section)

Указывает, пересматривается ли документ для разметки.
  
|**Значение**|**Описание**|
|:-----|:-----|
|TRUE  <br/> |Документ пересматривается.  <br/> |
|FALSE  <br/> |Документ не пересматривается (по умолчанию).  <br/> |
   
## <a name="remarks"></a>Примечания

Когда ячейка AddMarkup настроена на TRUE, рецензент добавляет разметку и изменения применяются к страницам наложения разметки, а не к исходным страницам рисования. Когда ячейка AddMarkup является FALSE, отслеживание разметки отключено и изменения применяются к исходным страницам рисования.
  
> [!NOTE]
> Вы можете предотвратить разметку на документах с помощью функции GUARD. Если ячейка AddMarkup содержит формулу =GUARD (FALSE), команда **разметки** track отключена. 
  
Этот параметр соответствует параметру **команды Track Markup** в группе **разметки** на вкладке **Обзор.** 
  
Чтобы получить ссылку на ячейку AddMarkup по имени из другой формулы или из программы с помощью **свойства CellsU,** используйте: 
  
|||
|:-----|:-----|
|Имя ячейки:  <br/> |AddMarkup  <br/> |
   
Чтобы получить ссылку на ячейку AddMarkup по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
|Индекс раздела:  <br/> |**visSectionObject** <br/> |
|Индекс строки:  <br/> |**visRowDoc** <br/> |
|Индекс ячейки:  <br/> |**visDocAddMarkup** <br/> |
   

