---
title: NoProofing Cell (Miscellaneous Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 668f993c-b4d1-4762-9801-c578b17fdafd
description: Определяет, происходит ли автоматическое исправление орфографии и отображаются ли ошибки орфографии для выбранной формы. Принимает значение Boolean.
ms.openlocfilehash: 8d7eebcc349c54db3cd48d6c5fa3c8fa6f4f760e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431255"
---
# <a name="noproofing-cell-miscellaneous-section"></a>NoProofing Cell (Miscellaneous Section)

Определяет, происходит ли автоматическое исправление орфографии и отображаются ли ошибки орфографии для выбранной формы. Принимает **значение Boolean.** 
  
|**Значение**|**Описание**|
|:-----|:-----|
|TRUE  <br/> |Орфография не исправляется автоматически, а ошибки орфографии не отображаются для выбранной формы.  <br/> |
|FALSE  <br/> |Орфография автоматически корректируется, и для выбранной формы отображаются ошибки орфографии.  <br/> |
   
## <a name="remarks"></a>Примечания

Чтобы получить ссылку на ячейку NoProofing по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте: 
  
|||
|:-----|:-----|
|Имя ячейки:  <br/> |NoProofing  <br/> |
   
Чтобы получить ссылку на ячейку NoProofing по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
|Индекс раздела:  <br/> |**visSectionObject** <br/> |
|Индекс строки:  <br/> |**visRowMisc** <br/> |
|Индекс ячейки:  <br/> |**visObjNoProofing** <br/> |
   

