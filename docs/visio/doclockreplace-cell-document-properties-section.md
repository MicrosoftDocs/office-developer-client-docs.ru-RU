---
title: Ячейка DocLockReplace (раздел "Свойства документа")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 74eae5e5-80ab-4e10-b292-e58a6d7607d2
description: Определяет, отключены ли фигура заменить пользовательского интерфейса для данного документа.
ms.openlocfilehash: 41552ddad4e48680960c45869ded5cf4f80d760f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813648"
---
# <a name="doclockreplace-cell-document-properties-section"></a>Ячейка DocLockReplace (раздел "Свойства документа")

Определяет, отключены ли фигура заменить пользовательского интерфейса для данного документа. 
  
|||
|:-----|:-----|
|TRUE  <br/> |**Замена фигуры** кнопка недоступна в пользовательском Интерфейсе.  <br/> |
|FALSE  <br/> |**Замена фигуры** кнопка активна в пользовательском Интерфейсе. Пользователи могут использовать функцию замените фигуры в этом документе.  <br/> |
   
## <a name="remarks"></a>Замечания

Для получения ссылки на ячейки **DocLockReplace** по имени из другой формулы, по значению атрибута **N** элемент **ячейки** и программы, с помощью свойства **CellsU** , используйте: 
  
|||
|:-----|:-----|
| Имя ячейки.  <br/> | DocLocReplace  <br/> |
   
Для получения ссылки на ячейки **DocLocReplace** по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionObject** <br/> |
| Индекс строки:  <br/> |**visRowDoc** <br/> |
| Индекс ячейки:  <br/> |** visDocLockReplace ** <br/> |
   

