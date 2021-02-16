---
title: PreviewScope Cell (Document Properties Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm820
localization_priority: Normal
ms.assetid: d03ae1b3-da6c-56d3-4f96-6e131c04e93e
description: Определяет, включает ли ваш рисунок предварительный просмотр. Если в вашем рисунке есть предварительный просмотр, он определяет, будет ли в режиме предварительного просмотра показана только первая страница или все страницы в этом рисунке.
ms.openlocfilehash: 34dbc9ac02032b2cb5cb6373c3c6361e3d822312
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426508"
---
# <a name="previewscope-cell-document-properties-section"></a>PreviewScope Cell (Document Properties Section)

Определяет, включает ли ваш рисунок предварительный просмотр. Если в вашем рисунке есть предварительный просмотр, он определяет, будет ли в режиме предварительного просмотра показана только первая страница или все страницы в этом рисунке.
  
|**Значение**|**Область предварительного просмотра**|**Константа автоматизации**|
|:-----|:-----|:-----|
| 0  <br/> | Первая страница  <br/> |**visDocPreviewScope1stPage** <br/> |
| 1   <br/> | Нет  <br/> |**visDocPreviewScopeNone** <br/> |
| 2   <br/> | Все страницы  <br/> |**visDocPreviewScopeAllPages** <br/> |
   
## <a name="remarks"></a>Примечания

Это значение также можно  установить на вкладке "Сводка" в диалоговом окне "Свойства" (нажмите кнопку **"Office",** выберите вкладку "Сведения", "Свойства документа" и "Дополнительные **свойства").**  
  
Чтобы получить ссылку на ячейку PreviewScope по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте: 
  
|||
|:-----|:-----|
| Имя ячейки:  <br/> | PreviewScope  <br/> |
   
Чтобы получить ссылку на ячейку PreviewScope по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionObject** <br/> |
| Индекс строки:  <br/> |**visRowDoc** <br/> |
| Индекс ячейки:  <br/> |**visDocPreviewScope** <br/> |
   

