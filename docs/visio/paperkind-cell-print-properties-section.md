---
title: PaperKind Cell (Print Properties Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60067
localization_priority: Normal
ms.assetid: b2c9616f-a144-eb99-54b6-b53745c7b4d6
description: Определяет тип бумаги, на которой будет печататься страница.
ms.openlocfilehash: 694aa1fb8b52f5ae323c47e9aab8715b4a48dfb0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327064"
---
# <a name="paperkind-cell-print-properties-section"></a>PaperKind Cell (Print Properties Section)

Определяет тип бумаги, на которой будет печататься страница.
  
## <a name="remarks"></a>Замечания

Этот параметр соответствует параметру **Размер бумаги** в диалоговом окне " **Настройка печати** " (на вкладке " **конструктор** " щелкните стрелку **настройки страницы** , а затем на вкладке **Настройка печати** нажмите кнопку **установить** ). 
  
Числовые значения в этой ячейке сопоставляются с константами (с префиксом ДМПАПЕР), определенными для выбора бумаги в файле Microsoft Windows вингди. h. 
  
Чтобы получить ссылку на ячейку PaperKind по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте следующее: 
  
|||
|:-----|:-----|
|Имя ячейки:  <br/> |PaperKind  <br/> |
   
Чтобы получить ссылку на ячейку PaperKind по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
|Индекс раздела:  <br/> |**visSectionObject** <br/> |
|Индекс строки:  <br/> |**Висровпринтпропертиес** <br/> |
|Индекс ячейки:  <br/> |**Виспринтпропертиеспаперкинд** <br/> |
   

