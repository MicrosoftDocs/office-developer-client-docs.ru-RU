---
title: Ячейка LockTextEdit (раздел Защита)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm665
localization_priority: Normal
ms.assetid: d8de5fa4-826b-e869-4d9f-997361d05fd8
description: Блокирует текст фигуры, не может быть изменен.
ms.openlocfilehash: 7f8800f0b260e808a46ec123d27784f3dd92e847
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814153"
---
# <a name="locktextedit-cell-protection-section"></a>Ячейка LockTextEdit (раздел Защита)

Блокирует текст фигуры, не может быть изменен.
  
|**Значение**|**Описание**|
|:-----|:-----|
|TRUE  <br/> |Невозможно изменить текст.  <br/> |
| FALSE  <br/> | Текст можно редактировать.  <br/> |
   
## <a name="remarks"></a>Замечания

По-прежнему можно отформатировать текст с применением стилей в диалоговое окно " **текст** " (на вкладке **Главная** щелкните стрелку **шрифтов** ). 
  
Чтобы получить ссылку на ячейку LockTextEdit по имени из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду: 
  
|||
|:-----|:-----|
| Имя ячейки.  <br/> | LockTextEdit  <br/> |
   
Для получения ссылки на ячейки LockTextEdit по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionObject** <br/> |
| Индекс строки:  <br/> |**visRowLock** <br/> |
| Индекс ячейки:  <br/> |**visLockTextEdit** <br/> |
   

