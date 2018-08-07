---
title: Ячейка Disabled (раздел "Теги действий")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60038
localization_priority: Normal
ms.assetid: bf0a80c9-0fdb-e2cf-3ab0-74cb6338fdce
description: Указывает, отображается ли тег действия в окне документа.
ms.openlocfilehash: 409327365f3daf78dba20b1874be5911a517df0f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813603"
---
# <a name="disabled-cell-action-tags-section"></a>Ячейка Disabled (раздел "Теги действий")

Указывает, отображается ли тег действия в окне документа.
  
> [!NOTE]
> В предыдущих версиях Microsoft Visio теги действий, называются смарт-тегов. 
  
|**Значение**|**Описание**|
|:-----|:-----|
| TRUE  <br/> | Тег действия отключено.  <br/> |
| FALSE  <br/> | Тег действия включена (по умолчанию).  <br/> |
   
## <a name="remarks"></a>Замечания

При отключении тег действие он отображался на всех до он перезапускается. 
  
Чтобы получить ссылку на ячейку отключено по имени из другой формулы или из файла с помощью свойства **CellsU** , используйте: 
  
|||
|:-----|:-----|
| Имя ячейки.  <br/> | Смарт-тегов.  *имя* . Этот параметр отключен где смарт-тегов. *имя* — это имя строки тега действия  <br/> |
   
Для получения ссылки на ячейки отключено по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionSmartTag** <br/> |
| Индекс строки:  <br/> |**visRowSmartTag** +  *i* где *i* = 0, 1, 2...  <br/> |
| Индекс ячейки:  <br/> |**visSmartTagDisabled** <br/> |
   

