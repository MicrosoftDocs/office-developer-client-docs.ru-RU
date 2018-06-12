---
title: Ячейка PageHeight (раздел страницы свойств)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm760
localization_priority: Normal
ms.assetid: 0184814c-2d67-6ad4-e336-5694612e518d
description: Содержит высоту печатной страницы в единицах документа.
ms.openlocfilehash: e198e90e9c70aad1e41ee02d5dcefea68846486c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814332"
---
# <a name="pageheight-cell-page-properties-section"></a>Ячейка PageHeight (раздел страницы свойств)

Содержит высоту печатной страницы в единицах документа.
  
## <a name="remarks"></a>Замечания

Высота страницы также можно настроить на вкладке **Размер страницы** диалогового окна **Параметры страницы** (на вкладки " **Конструктор** ", нажмите стрелку **Параметры страницы** ), или вручную изменения размеров страницы с помощью мыши. 
  
Для получения ссылки на ячейки PageHeight по имени, из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду: 
  
|||
|:-----|:-----|
|Имя ячейки.  <br/> |PageHeight  <br/> |
   
Для получения ссылки на ячейки PageHeight по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы: 
  
|||
|:-----|:-----|
|Индекс раздела:  <br/> |**visSectionObject** <br/> |
|Индекс строки:  <br/> |**visRowPage** <br/> |
|Индекс ячейки:  <br/> |**visPageHeight** <br/> |
   

