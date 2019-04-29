---
title: NoCoauth Cell (Document Properties Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6f2095c9-ce09-48f7-b160-c9822d96a96c
description: Указывает, может ли документ, хранящийся на сервере Microsoft SharePoint 2013 или Microsoft OneDrive, одновременно редактироваться несколькими авторами в сеансе совместного редактирования.
ms.openlocfilehash: a76e2d3b2c3cf6e99e37596b016f448b0be56fd3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420516"
---
# <a name="nocoauth-cell-document-properties-section"></a>NoCoauth Cell (Document Properties Section)

Указывает, может ли документ, хранящийся на сервере Microsoft SharePoint 2013 или Microsoft OneDrive, одновременно редактироваться несколькими авторами в сеансе совместного редактирования.
  
|**Значение**|**Описание**|
|:-----|:-----|
|TRUE  <br/> |Документ не может быть соавтором и заблокирован для редактирования при открытии.  <br/> |
|FALSE  <br/> |Документ можно совместно редактировать.  <br/> |
   
## <a name="remarks"></a>Примечания

Чтобы получить ссылку на ячейку **NoCoauth** по имени из другой формулы, по значению атрибута **N** элемента **ячейки** или из программы с помощью свойства **CellsU** , используйте: 
  
|||
|:-----|:-----|
| Имя ячейки:  <br/> | NoCoauth  <br/> |
   
Чтобы получить ссылку на ячейку **NoCoauth** по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionObject** <br/> |
| Индекс строки:  <br/> |**Висровдок** <br/> |
| Индекс ячейки:  <br/> |**Висдокнокоаус** <br/> |
   

