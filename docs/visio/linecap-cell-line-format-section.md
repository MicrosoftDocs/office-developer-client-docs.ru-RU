---
title: LineCap Cell (Line Format Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251231
localization_priority: Normal
ms.assetid: 3519216b-b6cf-2e8c-e20f-adfa373c9028
description: Указывает, имеет ли линия скругленные, квадратные или расширенные концы линий.
ms.openlocfilehash: 44de4bff87fd3d121dfce9eec934ec39bc61065a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425201"
---
# <a name="linecap-cell-line-format-section"></a>LineCap Cell (Line Format Section)

Указывает, имеет ли линия скругленные, квадратные или расширенные концы линий.
  
|**Значение**|**Стиль конца линии**|
|:-----|:-----|
|нуль  <br/> |Округляется  <br/> |
|1,1  <br/> |Го  <br/> |
|2  <br/> |Долго  <br/> |
   
## <a name="remarks"></a>Примечания

Значение этой ячейки также можно задать в диалоговом окне **линия** (на вкладке **Главная** , в группе **фигур** , нажмите кнопку **линия**, наведите указатель мыши на **стрелку**и выберите **Другие стрелки**).
  
Чтобы получить ссылку на ячейку LineCap по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте следующее: 
  
|||
|:-----|:-----|
|Имя ячейки:  <br/> |LineCap  <br/> |
   
Чтобы получить ссылку на ячейку LineCap по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
|Индекс раздела:  <br/> |**visSectionObject** <br/> |
|Индекс строки:  <br/> |**висровлине** <br/> |
|Индекс ячейки:  <br/> |**вислининдкап** <br/> |
   

