---
title: Ячейка TxtLocPinY (раздел "Преобразование текста")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251276
localization_priority: Normal
ms.assetid: 3f46cfcf-7eac-4a37-e782-39f4e7f8fc43
description: 'Определяет, y-координаты центра блок текста ротации относительно начала блока текста. Формула по умолчанию имеет вид:'
ms.openlocfilehash: 7d43f63b8560df5fc5daf09a429ce30ec976d131
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815076"
---
# <a name="txtlocpiny-cell-text-transform-section"></a>Ячейка TxtLocPinY (раздел "Преобразование текста")

Определяет, *y* -координаты центра блок текста ротации относительно начала блока текста. Формула по умолчанию имеет вид: 
  
= ВысотаТекста \* 0,5
  
## <a name="remarks"></a>Замечания

Чтобы получить ссылку на ячейку TxtLocPinY по имени из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду: 
  
|||
|:-----|:-----|
| Имя ячейки.  <br/> | TxtLocPinY  <br/> |
   
Для получения ссылки на ячейки TxtLocPinY по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionObject** <br/> |
| Индекс строки:  <br/> |**visRowTextXForm** <br/> |
| Индекс ячейки:  <br/> |**visXFormLocPinY** <br/> |
   

