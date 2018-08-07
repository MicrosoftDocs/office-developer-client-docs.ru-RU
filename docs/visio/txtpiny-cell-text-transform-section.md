---
title: Ячейка TxtPinY (раздел "Преобразование текста")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm1045
localization_priority: Normal
ms.assetid: 88ddf4b5-8248-8c1a-c387-09a607639d26
description: 'Определяет, y-координата блок текста центра вращения относительно начала фигуры. Формула по умолчанию имеет вид:'
ms.openlocfilehash: e8101463413b177bf8ddd80ed52964d3eeae788f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815084"
---
# <a name="txtpiny-cell-text-transform-section"></a>Ячейка TxtPinY (раздел "Преобразование текста")

Определяет, *y* -координата блок текста центра вращения относительно начала фигуры. Формула по умолчанию имеет вид: 
  
= Высота \* 0,5
  
## <a name="remarks"></a>Замечания

Чтобы получить ссылку на ячейку TxtPinY по имени из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду: 
  
|||
|:-----|:-----|
| Имя ячейки.  <br/> | TxtPinY  <br/> |
   
Для получения ссылки на ячейки TxtPinY по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionObject** <br/> |
| Индекс строки:  <br/> |**visRowTextXForm** <br/> |
| Индекс ячейки:  <br/> |**visXFormPinY** <br/> |
   

