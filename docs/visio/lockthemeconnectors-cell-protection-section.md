---
title: LockThemeConnectors Cell (Protection Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ae7ddd55-7bcc-4bb6-bab7-97806122f166
description: Предотвращает изменение ячейки ConnectorsSchemeIndex в строке "Свойства темы" путем применения новой темы или выбора новой схемы соединителя. Не мешает пользователям вручную редактировать это значение в таблице shapeSheet.
ms.openlocfilehash: 8097e50646fd59f4ac0212cbe9ca2ecfaadab7a2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438409"
---
# <a name="lockthemeconnectors-cell-protection-section"></a>LockThemeConnectors Cell (Protection Section)

Предотвращает изменение **ячейки ConnectorsSchemeIndex** в строке **"Свойства** темы" путем применения новой темы или выбора новой схемы соединителя. Не мешает пользователям вручную редактировать это значение в таблице shapeSheet. 
  
|**Значение**|**Описание**|
|:-----|:-----|
|TRUE  <br/> |Ячейку **ConnectorsSchemeIndex** нельзя изменить по текущему значению, если она не изменена непосредственно в shapeSheet.  <br/> |
|FALSE  <br/> |Ячейку **ConnectorsSchemeIndex** можно изменить с текущего значения через пользовательский интерфейс.  <br/> |
   
## <a name="remarks"></a>Примечания

Чтобы получить ссылку на ячейку **LockThemeConnectors** по имени из другой формулы, по значению атрибута **N** элемента **Cell** или из программы, использующей свойство **CellsU,** используйте: 
  
|||
|:-----|:-----|
| Имя ячейки:  <br/> | LockThemeConnectors  <br/> |
   
Чтобы получить ссылку на ячейку **LockThemeConnectors** по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionObject** <br/> |
| Индекс строки:  <br/> |**visRowLock** <br/> |
| Индекс ячейки:  <br/> |**visLockThemeConnectors** <br/> |
   

