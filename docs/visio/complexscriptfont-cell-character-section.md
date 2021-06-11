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
# <a name="complexscriptfont-cell-character-section"></a><span data-ttu-id="209f5-104">ComplexScriptFont Cell (Character Section)</span><span class="sxs-lookup"><span data-stu-id="209f5-104">ComplexScriptFont Cell (Character Section)</span></span>

<span data-ttu-id="209f5-105">Содержит число шрифта, используемого для формата текста, состоящего из сложных символов скрипта.</span><span class="sxs-lookup"><span data-stu-id="209f5-105">Contains the number of the font used to format text composed of complex script characters.</span></span> <span data-ttu-id="209f5-106">Номера шрифтов различаются в зависимости от шрифтов, установленных в системе.</span><span class="sxs-lookup"><span data-stu-id="209f5-106">Font numbers vary according to the fonts installed on your system.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="209f5-107">Примечания</span><span class="sxs-lookup"><span data-stu-id="209f5-107">Remarks</span></span>

<span data-ttu-id="209f5-108">Сложные размеры шрифтов скрипта перечислены на вкладке **Font** в диалоговом окне **Text** (щелкните стрелку в группе **Шрифт** на вкладке **Главная).**</span><span class="sxs-lookup"><span data-stu-id="209f5-108">Complex script font sizes are listed on the **Font** tab in the **Text** dialog box (click the arrow in the **Font** group on the **Home** tab).</span></span> <span data-ttu-id="209f5-109">Этот список отображается только в том случае, если в **диалоговом окне Языковые** предпочтения добавлен язык, содержащий азиатские или сложные символы скрипта, Microsoft Office языковые предпочтения.</span><span class="sxs-lookup"><span data-stu-id="209f5-109">This list appears only if you have added a language that contains Asian or complex script characters, in the **Microsoft Office Language Preferences** dialog box.</span></span> <span data-ttu-id="209f5-110">(Нажмите **кнопку Начните,** нажмите кнопку Все **программы,** **нажмите Microsoft Office,** **нажмите Microsoft Office инструменты,** а затем нажмите кнопку Microsoft Office **Языковые предпочтения**.</span><span class="sxs-lookup"><span data-stu-id="209f5-110">(Click **Start**, click **All Programs**, click **Microsoft Office**, click **Microsoft Office Tools**, and then click **Microsoft Office Language Preferences**.</span></span>
  
<span data-ttu-id="209f5-111">Число 0 (ноль) означает, что шрифт не указан.</span><span class="sxs-lookup"><span data-stu-id="209f5-111">The number 0 (zero) means no font is specified.</span></span> <span data-ttu-id="209f5-112">Используются латинские шрифты или шрифты по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="209f5-112">The Latin font or default fonts are used.</span></span>
  
<span data-ttu-id="209f5-113">Чтобы получить ссылку на ячейку ComplexScriptSize по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте:</span><span class="sxs-lookup"><span data-stu-id="209f5-113">To get a reference to the ComplexScriptSize cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="209f5-114">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="209f5-114">Cell name:</span></span>  <br/> |<span data-ttu-id="209f5-115">Char.ComplexScriptFont[ *i*  ] где  *i*  = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="209f5-115">Char.ComplexScriptFont[ *i*  ]           where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="209f5-116">Чтобы получить ссылку на ячейку ComplexScriptFont по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="209f5-116">To get a reference to the ComplexScriptFont cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="209f5-117">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="209f5-117">Section index:</span></span>  <br/> |<span data-ttu-id="209f5-118">**visSectionCharacter**</span><span class="sxs-lookup"><span data-stu-id="209f5-118">**visSectionCharacter**</span></span> <br/> |
|<span data-ttu-id="209f5-119">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="209f5-119">Row index:</span></span>  <br/> |<span data-ttu-id="209f5-120">**visRowCharacter**  +   *i,* *где i* = 0, 1, 2 ...</span><span class="sxs-lookup"><span data-stu-id="209f5-120">**visRowCharacter** +  *i*           where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="209f5-121">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="209f5-121">Cell index:</span></span>  <br/> |<span data-ttu-id="209f5-122">**visCharacterComplexScriptFont**</span><span class="sxs-lookup"><span data-stu-id="209f5-122">**visCharacterComplexScriptFont**</span></span> <br/> |
   

