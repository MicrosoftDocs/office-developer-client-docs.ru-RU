---
title: ComplexScriptSize Cell (Character Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033768
localization_priority: Normal
ms.assetid: f58687d7-2ba4-ff77-0bcc-3106867d89de
description: Размер шрифта, используемого для формата текста, состоящего из сложных символов сценария.
ms.openlocfilehash: 38b01c4a0142c7eca2923ee9b13963eaa1a62830
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428440"
---
# <a name="complexscriptsize-cell-character-section"></a>ComplexScriptSize Cell (Character Section)

Размер шрифта, используемого для формата текста, состоящего из сложных символов сценария. 
  
## <a name="remarks"></a>Примечания

Сложные размеры шрифтов скрипта перечислены на вкладке **Font** в диалоговом окне **Text** (щелкните стрелку в группе **Шрифт** на вкладке **Главная).** Этот список отображается только в том случае, если в **диалоговом окне Языковые** предпочтения добавлен язык, содержащий азиатские или сложные символы скрипта, Microsoft Office языковые предпочтения. (Нажмите **кнопку Начните,** нажмите кнопку Все **программы,** **нажмите Microsoft Office,** **нажмите Microsoft Office инструменты,** а затем нажмите кнопку Microsoft Office **Языковые предпочтения**.
  
Это значение можно ввести в виде явного размера точки или в процентах. Если указать процент, значение основано на значении в ячейке Size. Значение по умолчанию 0 (ноль) означает 100%. 
  
Чтобы получить ссылку на ячейку ComplexScriptSize по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте: 
  
|||
|:-----|:-----|
|Имя ячейки:  <br/> |Char.ComplexScriptSize[i] где *i* = <1>, 2, 3...   <br/> |
   
Чтобы получить ссылку на ячейку ComplexScriptSize по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
|Индекс раздела:  <br/> |**visSectionCharacter** <br/> |
|Индекс строки:  <br/> |**visRowCharacter**  +   *i,* *где i* = 0, 1, 2 ...  <br/> |
|Индекс ячейки:  <br/> |**visCharacterComplexScriptSize** <br/> |
   

