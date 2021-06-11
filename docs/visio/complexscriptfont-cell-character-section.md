---
title: ComplexScriptFont Cell (Character Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60034
localization_priority: Normal
ms.assetid: e1cf9e97-101b-384f-65fe-0169c89dfccc
description: Содержит число шрифта, используемого для формата текста, состоящего из сложных символов скрипта. Номера шрифтов различаются в зависимости от шрифтов, установленных в системе.
ms.openlocfilehash: 5ec8deb59b875a01592b6d7b652204089ecf11e0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404836"
---
# <a name="complexscriptfont-cell-character-section"></a>ComplexScriptFont Cell (Character Section)

Содержит число шрифта, используемого для формата текста, состоящего из сложных символов скрипта. Номера шрифтов различаются в зависимости от шрифтов, установленных в системе. 
  
## <a name="remarks"></a>Примечания

Сложные размеры шрифтов скрипта перечислены на вкладке **Font** в диалоговом окне **Text** (щелкните стрелку в группе **Шрифт** на вкладке **Главная).** Этот список отображается только в том случае, если в **диалоговом окне Языковые** предпочтения добавлен язык, содержащий азиатские или сложные символы скрипта, Microsoft Office языковые предпочтения. (Нажмите **кнопку Начните,** нажмите кнопку Все **программы,** **нажмите Microsoft Office,** **нажмите Microsoft Office инструменты,** а затем нажмите кнопку Microsoft Office **Языковые предпочтения**.
  
Число 0 (ноль) означает, что шрифт не указан. Используются латинские шрифты или шрифты по умолчанию.
  
Чтобы получить ссылку на ячейку ComplexScriptSize по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте: 
  
|||
|:-----|:-----|
|Имя ячейки:  <br/> |Char.ComplexScriptFont[ *i*  ] где  *i*  = <1>, 2, 3...  <br/> |
   
Чтобы получить ссылку на ячейку ComplexScriptFont по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
|Индекс раздела:  <br/> |**visSectionCharacter** <br/> |
|Индекс строки:  <br/> |**visRowCharacter**  +   *i,* *где i* = 0, 1, 2 ...  <br/> |
|Индекс ячейки:  <br/> |**visCharacterComplexScriptFont** <br/> |
   

