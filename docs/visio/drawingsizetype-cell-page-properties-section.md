---
title: DrawingSizeType Cell (Page Properties Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm275
localization_priority: Normal
ms.assetid: 7fe270e8-0dff-bf1f-dfc0-c0608af79f59
description: Определяет размер документа.
ms.openlocfilehash: 33c85b6c2f0587654038eaec1a9490ca8bd8301b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425451"
---
# <a name="drawingsizetype-cell-page-properties-section"></a>DrawingSizeType Cell (Page Properties Section)

Определяет размер документа.
  
|**Значение**|**Описание**|**Константа автоматизации**|
|:-----|:-----|:-----|
|нуль  <br/> |То же, что принтер  <br/> |**виспринтсетуп** <br/> |
|1,1  <br/> |Вписать страницу в контент для рисования  <br/> |**вистигхт** <br/> |
|2  <br/> |Standard  <br/> |**висстандард** <br/> |
|4  <br/> |Настраиваемый размер страницы  <br/> |**вискустом** <br/> |
|4   <br/> |Размер настраиваемого масштабированного рисунка  <br/> |**вислогикал** <br/> |
|5   <br/> |Метрическая система показателей (ISO)  <br/> |**висдсметрик** <br/> |
|6   <br/> |Разработка с ANSI  <br/> |**висдсенгр** <br/> |
|7   <br/> |Архитектура ANSI  <br/> |**висдсарч** <br/> |
   
## <a name="remarks"></a>Примечания

Чтобы задать размер документа, воспользуйтесь диалоговым окном **Параметры страницы** (щелкните стрелку **настройки страницы** на вкладке **конструктор** ) или вручную измените размер страницы с помощью мыши. 
  
Чтобы получить ссылку на ячейку DrawingSizeType по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте следующее: 
  
|||
|:-----|:-----|
|Имя ячейки:  <br/> |DrawingSizeType  <br/> |
   
Чтобы получить ссылку на ячейку DrawingSizeType по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
|Индекс раздела:  <br/> |**visSectionObject** <br/> |
|Индекс строки:  <br/> |**висровпаже** <br/> |
|Индекс ячейки:  <br/> |**виспажедравсизетипе** <br/> |
   

