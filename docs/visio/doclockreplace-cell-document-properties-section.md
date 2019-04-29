---
title: DocLockReplace Cell (Document Properties Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 74eae5e5-80ab-4e10-b292-e58a6d7607d2
description: Определяет, следует ли отключить пользовательский интерфейс замены фигуры для этого документа.
ms.openlocfilehash: cfec9b3c51a170c549fdd0d1b0b3597c030c410c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413425"
---
# <a name="doclockreplace-cell-document-properties-section"></a>DocLockReplace Cell (Document Properties Section)

Определяет, следует ли отключить пользовательский интерфейс замены фигуры для этого документа. 
  
|||
|:-----|:-----|
|TRUE  <br/> |Кнопка **заменить фигуру** неактивна в пользовательском интерфейсе.  <br/> |
|FALSE  <br/> |Кнопка **заменить фигура** активна в пользовательском интерфейсе. Пользователи могут использовать функцию заменить фигуру в этом документе.  <br/> |
   
## <a name="remarks"></a>Примечания

Чтобы получить ссылку на ячейку **DocLockReplace** по имени из другой формулы, по значению атрибута **N** элемента **ячейки** или из программы с помощью свойства **CellsU** , используйте: 
  
|||
|:-----|:-----|
| Имя ячейки:  <br/> | Доклокреплаце  <br/> |
   
Чтобы получить ссылку на ячейку **доклокреплаце** по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionObject** <br/> |
| Индекс строки:  <br/> |**Висровдок** <br/> |
| Индекс ячейки:  <br/> |* * Висдоклоккреплаце * * <br/> |
   

