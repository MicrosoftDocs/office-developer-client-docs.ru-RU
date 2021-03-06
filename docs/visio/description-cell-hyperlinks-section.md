---
title: Description Cell (Hyperlinks Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm230
localization_priority: Normal
ms.assetid: 2f571c65-6b7a-5a3a-c075-3c52d3ab989b
description: Представляет текстовую строку для гиперссылки.
ms.openlocfilehash: b58e6dc3ec2fc3b64db00e0f19e0718fe897aaa3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360244"
---
# <a name="description-cell-hyperlinks-section"></a>Description Cell (Hyperlinks Section)

Представляет текстовую строку для гиперссылки. 
  
## <a name="remarks"></a>Примечания

Используйте эту ячейку для хранения комментариев по гиперссылке; например, "Ссылка на наш сайт ценообразования".
  
Вы также можете установить значение этой  ячейки в диалоговом окне Гиперссылки (щелкните **Гиперссылку** на вкладке **Вставка).** 
  
Чтобы получить ссылку на ячейку Description по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте: 
  
|||
|:-----|:-----|
| Имя ячейки:  <br/> | Гиперссылка.  *Имя*  . Описание, где гиперссылка.  *Имя*  — это имя строки гиперссылки  <br/> |
   
Чтобы получить ссылку на ячейку Description по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionHyperlink** <br/> |
| Индекс строки:  <br/> |**visRow1stHyperlink**  +   *i,* *где i* = 0, 1, 2 ...  <br/> |
| Индекс ячейки:  <br/> |**visHLinkDescription** <br/> |
   

