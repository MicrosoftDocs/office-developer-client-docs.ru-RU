---
title: Ячейка PaperKind (раздел "Свойства печати")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60067
localization_priority: Normal
ms.assetid: b2c9616f-a144-eb99-54b6-b53745c7b4d6
description: Указывает тип бумаги для печати на странице.
ms.openlocfilehash: 03659553ab32afd20d1a5a40b85a8bbf107dbb08
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814351"
---
# <a name="paperkind-cell-print-properties-section"></a>Ячейка PaperKind (раздел "Свойства печати")

Указывает тип бумаги для печати на странице.
  
## <a name="remarks"></a>Замечания

Этот параметр соответствует параметру **Размер бумаги** в диалоговом окне " **Настройка печати** " (на вкладке " **Конструктор** ", щелкните стрелку **Параметры страницы** и на вкладке **Настройка печати** нажмите кнопку **программы установки** ). 
  
Числовые значения в этой ячейке сопоставить с константы (с DMPAPER префиксом), определенных для выбранных элементов документ в файле wingdi.h Microsoft Windows. 
  
Чтобы получить ссылку на ячейку PaperKind по имени из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду: 
  
|||
|:-----|:-----|
|Имя ячейки.  <br/> |PaperKind  <br/> |
   
Для получения ссылки на ячейки PaperKind по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы: 
  
|||
|:-----|:-----|
|Индекс раздела:  <br/> |**visSectionObject** <br/> |
|Индекс строки:  <br/> |**visRowPrintProperties** <br/> |
|Индекс ячейки:  <br/> |**visPrintPropertiesPaperKind** <br/> |
   

