---
title: Ячейка NoCoauth (раздел "Свойства документа")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6f2095c9-ce09-48f7-b160-c9822d96a96c
description: Задает ли документ, хранящийся на сервере Microsoft SharePoint 2013 или Microsoft OneDrive можно редактировать несколькими авторами одновременно в также сеанса.
ms.openlocfilehash: a20c3a5aa1392e0e6c3bef124f536b91b9642f47
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814302"
---
# <a name="nocoauth-cell-document-properties-section"></a>Ячейка NoCoauth (раздел "Свойства документа")

Задает ли документ, хранящийся на сервере Microsoft SharePoint 2013 или Microsoft OneDrive можно редактировать несколькими авторами одновременно в также сеанса.
  
|**Значение**|**Описание**|
|:-----|:-----|
|TRUE  <br/> |Документ нельзя совместное редактирование и заблокирован для редактирования при открытии.  <br/> |
|FALSE  <br/> |Можно совместное редактирование документа.  <br/> |
   
## <a name="remarks"></a>Замечания

Для получения ссылки на ячейки **NoCoauth** по имени из другой формулы, по значению атрибута **N** элемент **ячейки** и программы, с помощью свойства **CellsU** , используйте: 
  
|||
|:-----|:-----|
| Имя ячейки.  <br/> | NoCoauth  <br/> |
   
Для получения ссылки на ячейки **NoCoauth** по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionObject** <br/> |
| Индекс строки:  <br/> |**visRowDoc** <br/> |
| Индекс ячейки:  <br/> |**visDocNoCoauth** <br/> |
   

