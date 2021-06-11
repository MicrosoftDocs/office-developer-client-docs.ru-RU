---
title: NoCoauth Cell (Document Properties Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6f2095c9-ce09-48f7-b160-c9822d96a96c
description: Задает, может ли документ, хранимый на сервере Microsoft SharePoint 2013 г. или Microsoft OneDrive может быть отредактирован несколькими авторами одновременно в сеансе совместной работы.
ms.openlocfilehash: a76e2d3b2c3cf6e99e37596b016f448b0be56fd3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420516"
---
# <a name="nocoauth-cell-document-properties-section"></a>NoCoauth Cell (Document Properties Section)

Задает, может ли документ, хранимый на сервере Microsoft SharePoint 2013 г. или Microsoft OneDrive может быть отредактирован несколькими авторами одновременно в сеансе совместной работы.
  
|**Значение**|**Описание**|
|:-----|:-----|
|TRUE  <br/> |Документ не может быть соавтором и заблокирован для редактирования при открываемом.  <br/> |
|FALSE  <br/> |Документ можно совместно использовать.  <br/> |
   
## <a name="remarks"></a>Примечания

Чтобы получить ссылку на **ячейку NoCoauth** по имени из другой формулы, по значению атрибута **N** элемента **Cell** или из программы с использованием свойства **CellsU,** используйте: 
  
|||
|:-----|:-----|
| Имя ячейки:  <br/> | NoCoauth  <br/> |
   
Чтобы получить ссылку на **ячейку NoCoauth** по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionObject** <br/> |
| Индекс строки:  <br/> |**visRowDoc** <br/> |
| Индекс ячейки:  <br/> |**visDocNoCoauth** <br/> |
   

