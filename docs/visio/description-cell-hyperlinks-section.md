---
title: Ячейка Description (раздел "Гиперссылки")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm230
localization_priority: Normal
ms.assetid: 2f571c65-6b7a-5a3a-c075-3c52d3ab989b
description: Представляет строку описательный текст гиперссылки.
ms.openlocfilehash: b58e6dc3ec2fc3b64db00e0f19e0718fe897aaa3
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25396626"
---
# <a name="description-cell-hyperlinks-section"></a>Ячейка Description (раздел "Гиперссылки")

Представляет строку описательный текст гиперссылки. 
  
## <a name="remarks"></a>Замечания

Используйте эту ячейку для хранения комментариев о гиперссылках; Например «ссылка на сайте цен».
  
Можно также задать значение данной ячейки в диалоговом окне **гиперссылки** (щелкните **гиперссылку** на вкладке **Вставка** ). 
  
Для получения ссылки на ячейки описание по имени, из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду: 
  
|||
|:-----|:-----|
| Имя ячейки:  <br/> | Гиперссылки.  *Имя* . Описание где гиперссылки.  *Имя* — это имя строки гиперссылки  <br/> |
   
Для получения ссылки на ячейки описание по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionHyperlink** <br/> |
| Индекс строки:  <br/> |**visRow1stHyperlink** +  *i* где *i* = 0, 1, 2...  <br/> |
| Индекс ячейки:  <br/> |**visHLinkDescription** <br/> |
   

