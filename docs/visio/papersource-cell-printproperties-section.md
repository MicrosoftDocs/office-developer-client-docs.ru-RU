---
title: Ячейка PaperSource (раздел "Свойства печати")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60068
localization_priority: Normal
ms.assetid: 771a2ab4-578d-51c3-fabd-138f7952bb11
description: Определяет источник бумаги для страницы.
ms.openlocfilehash: f1dedf210dfe0dd8cac3d36fdec03fb497f6572c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814347"
---
# <a name="papersource-cell-printproperties-section"></a>Ячейка PaperSource (раздел "Свойства печати")

Определяет источник бумаги для страницы. 
  
## <a name="remarks"></a>Замечания

Этот параметр соответствует параметру **Источник бумаги** в диалоговом окне " **Настройка печати** " (на вкладке " **Конструктор** ", нажмите стрелку **Параметры страницы** и нажмите кнопку **программы установки**на вкладке **Настройка печати** ).
  
Числовые значения в с помощью этой карты ячейки для константы (с DMBIN префиксом), заданных для ячейки выбранные элементы в файле wingdi.h Microsoft Windows; Например DMBIN_AUTO представляет значение 7. 
  
Чтобы получить ссылку на ячейку PaperSource по имени из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду: 
  
|||
|:-----|:-----|
|Имя ячейки.  <br/> |PaperSource  <br/> |
   
Для получения ссылки на ячейки PaperSource по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы: 
  
|||
|:-----|:-----|
|Индекс раздела:  <br/> |**visSectionObject** <br/> |
|Индекс строки:  <br/> |**visRowPrintProperties** <br/> |
|Индекс ячейки:  <br/> |**visPrintPropertiesPaperSource** <br/> |
   

