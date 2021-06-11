---
title: LockTextEdit Cell (Protection Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm665
localization_priority: Normal
ms.assetid: d8de5fa4-826b-e869-4d9f-997361d05fd8
description: Заблокирует текст фигуры, чтобы он не был отредактирован.
ms.openlocfilehash: f6e5176e3ab654b76c0641b8f642abcf6b1050dd
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404500"
---
# <a name="locktextedit-cell-protection-section"></a>LockTextEdit Cell (Protection Section)

Заблокирует текст фигуры, чтобы он не был отредактирован.
  
|**Значение**|**Описание**|
|:-----|:-----|
|TRUE  <br/> |Текст не может быть изменен.  <br/> |
| FALSE  <br/> | Текст можно изменить.  <br/> |
   
## <a name="remarks"></a>Примечания

Вы по-прежнему можете форматировать текст, применяя стиль в диалоговом окне **Text** (на вкладке **Главная** щелкните **стрелку Шрифта).** 
  
Чтобы получить ссылку на ячейку LockTextEdit по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте: 
  
|||
|:-----|:-----|
| Имя ячейки:  <br/> | LockTextEdit  <br/> |
   
Чтобы получить ссылку на ячейку LockTextEdit по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionObject** <br/> |
| Индекс строки:  <br/> |**visRowLock** <br/> |
| Индекс ячейки:  <br/> |**visLockTextEdit** <br/> |
   

