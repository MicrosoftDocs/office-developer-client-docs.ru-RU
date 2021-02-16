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
description: Размер шрифта, используемого для формата текста, состоящего из сложных символов скрипта.
ms.openlocfilehash: 38b01c4a0142c7eca2923ee9b13963eaa1a62830
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428440"
---
# <a name="complexscriptsize-cell-character-section"></a>ComplexScriptSize Cell (Character Section)

Размер шрифта, используемого для формата текста, состоящего из сложных символов скрипта. 
  
## <a name="remarks"></a>Примечания

Сложные размеры шрифтов скриптов перечислены  на вкладке **"Шрифт"**  в диалоговом окне "Текст" (щелкните стрелку в группе шрифтов на вкладке **"Главная").** Этот список отображается, только если вы добавили язык, содержащий азиатские или сложные символы скрипта, в диалоговом окне Microsoft Office **Языковые** параметры. (Нажмите **кнопку**"Начните", выберите "Все программы", Microsoft Office **,** **Microsoft Office**"Инструменты" и выберите Microsoft Office **"Языковые параметры".**
  
Это значение можно ввести в виде явного размера точки или в виде процента. Если указать процент, значение будет основано на значении в ячейке Size. Значение по умолчанию 0 (ноль) означает 100%. 
  
Чтобы получить ссылку на ячейку ComplexScriptSize по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте: 
  
|||
|:-----|:-----|
|Имя ячейки:  <br/> |Char.ComplexScriptSize[ *i*  ] где  *i*  = <1>, 2, 3...  <br/> |
   
Чтобы получить ссылку на ячейку ComplexScriptSize по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
|Индекс раздела:  <br/> |**visSectionCharacter** <br/> |
|Индекс строки:  <br/> |**visRowCharacter**  +   *i,* *где i* = 0, 1, 2...  <br/> |
|Индекс ячейки:  <br/> |**visCharacterComplexScriptSize** <br/> |
   

