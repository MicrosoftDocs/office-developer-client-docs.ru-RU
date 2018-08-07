---
title: Ячейка TxtPinX (раздел "Преобразование текста")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm1040
localization_priority: Normal
ms.assetid: d0c0fe52-6a9e-e40e-394e-83a851db55a4
description: 'Определяет значение x-координаты центра блок текста из ротации относительно начала фигуры. Формула по умолчанию имеет вид:'
ms.openlocfilehash: df103557d103dbde7e4a1c8d67cabe37a0af9311
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815078"
---
# <a name="txtpinx-cell-text-transform-section"></a>Ячейка TxtPinX (раздел "Преобразование текста")

Определяет значение *x* -координаты центра блок текста из ротации относительно начала фигуры. Формула по умолчанию имеет вид: 
  
= Ширина \* 0,5
  
## <a name="remarks"></a>Замечания

Чтобы получить ссылку на ячейку TxtPinX по имени из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду: 
  
|||
|:-----|:-----|
| Имя ячейки.  <br/> | TxtPinX  <br/> |
   
Для получения ссылки на ячейки TxtPinX по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionObject** <br/> |
| Индекс строки:  <br/> |**visRowTextXForm** <br/> |
| Индекс ячейки:  <br/> |**visXFormPinX** <br/> |
   

