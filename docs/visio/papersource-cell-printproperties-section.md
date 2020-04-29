---
title: PaperSource Cell (PrintProperties Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60068
localization_priority: Normal
ms.assetid: 771a2ab4-578d-51c3-fabd-138f7952bb11
description: Определяет источник бумаги для страницы.
ms.openlocfilehash: eb6e7daccb1743c43a30b34598e47187496e4aac
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406761"
---
# <a name="papersource-cell-printproperties-section"></a>PaperSource Cell (PrintProperties Section)

Определяет источник бумаги для страницы. 
  
## <a name="remarks"></a>Примечания

Этот параметр соответствует параметру **источник бумаги** в диалоговом окне " **Настройка печати** " (на вкладке " **конструктор** " щелкните стрелку **Параметры страницы** , а затем на вкладке **Настройка печати** нажмите кнопку **Настройка**).
  
Числовые значения в этой ячейке сопоставляются с константами (с префиксом ДМБИН), определенными для выбранных ячеек в файле Microsoft Windows вингди. h; Например, значение 7 соответствует DMBIN_AUTO. 
  
Чтобы получить ссылку на ячейку PaperSource по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте следующее: 
  
|||
|:-----|:-----|
|Имя ячейки:  <br/> |PaperSource  <br/> |
   
Чтобы получить ссылку на ячейку PaperSource по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
|Индекс раздела:  <br/> |**visSectionObject** <br/> |
|Индекс строки:  <br/> |**висровпринтпропертиес** <br/> |
|Индекс ячейки:  <br/> |**виспринтпропертиеспаперсаурце** <br/> |
   

