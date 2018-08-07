---
title: Ячейка Invisible (раздел "Действия")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60046
localization_priority: Normal
ms.assetid: 070b4468-c907-b201-1633-1d3e10ecc2b2
description: Указывает, видима ли действие в меню Действие тег или ярлык.
ms.openlocfilehash: 8749b7d6db4a932b97c68ab5cf30b879a57d28f2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813970"
---
# <a name="invisible-cell-actions-section"></a>Ячейка Invisible (раздел "Действия")

Указывает, видима ли действие в меню Действие тег или ярлык. 
  
> [!NOTE]
> В предыдущих версиях Microsoft Visio теги действий, называются смарт-тегов. 
  
|**Значение**|**Описание**|
|:-----|:-----|
|TRUE  <br/> |Действие не отображается в меню.  <br/> |
|FALSE  <br/> |Действие отображается в меню (по умолчанию).  <br/> |
   
## <a name="remarks"></a>Замечания

Для получения ссылки на невидимой ячейку по имени из другой формулы или из файла с помощью свойства **CellsU** , используйте следующую команду: 
  
|||
|:-----|:-----|
|Имя ячейки.  <br/> |Действия. *имя* . Invisiblewhere действия.  *имя* — это имя строки действий  <br/> |
   
Для получения ссылки на ячейки невидимой по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы: 
  
|||
|:-----|:-----|
|Индекс раздела:  <br/> |**visSectionAction** <br/> |
|Индекс строки:  <br/> |**visRowAction** +  *i* где *i* = 0, 1, 2...  <br/> |
|Индекс ячейки:  <br/> |**visActionInvisible** <br/> |
   

