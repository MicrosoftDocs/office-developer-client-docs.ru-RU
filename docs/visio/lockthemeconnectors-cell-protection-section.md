---
title: Ячейка LockThemeConnectors (раздел Защита)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ae7ddd55-7bcc-4bb6-bab7-97806122f166
description: Запрещает ConnectorsSchemeIndex ячейку в строке темы свойств изменяются применение новой темы или выбрать новую схему соединителя. Запрещает пользователям изменять это значение в таблице свойств фигуры вручную.
ms.openlocfilehash: c74bcf554f0f14de47480397a96680469826d2c2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814155"
---
# <a name="lockthemeconnectors-cell-protection-section"></a>Ячейка LockThemeConnectors (раздел Защита)

Запрещает **ConnectorsSchemeIndex** ячейку в строке **Темы свойств** изменяются применение новой темы или выбрать новую схему соединителя. Запрещает пользователям изменять это значение в таблице свойств фигуры вручную. 
  
|**Значение**|**Описание**|
|:-----|:-----|
|TRUE  <br/> |Ячейка **ConnectorsSchemeIndex** может быть изменен с текущим значением только напрямую изменить в таблице свойств фигуры.  <br/> |
|FALSE  <br/> |Ячейка **ConnectorsSchemeIndex** могут изменяться с текущим значением в пользовательском Интерфейсе.  <br/> |
   
## <a name="remarks"></a>Замечания

Для получения ссылки на ячейки **LockThemeConnectors** по имени из другой формулы, по значению атрибута **N** элемент **ячейки** и программы, с помощью свойства **CellsU** , используйте: 
  
|||
|:-----|:-----|
| Имя ячейки.  <br/> | LockThemeConnectors  <br/> |
   
Для получения ссылки на ячейки **LockThemeConnectors** по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionObject** <br/> |
| Индекс строки:  <br/> |**visRowLock** <br/> |
| Индекс ячейки:  <br/> |**visLockThemeConnectors** <br/> |
   

