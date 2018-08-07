---
title: Ячейка ComplexScriptFont (раздел "Символ")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60034
localization_priority: Normal
ms.assetid: e1cf9e97-101b-384f-65fe-0169c89dfccc
description: Содержит номер шрифта, используемого для форматирования текста, состоящего из символов сложного. Номера шрифтов зависят шрифты, установленные в системе.
ms.openlocfilehash: 0aae3a22be26f206763f18107eaced74f1078503
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813434"
---
# <a name="complexscriptfont-cell-character-section"></a><span data-ttu-id="59130-104">Ячейка ComplexScriptFont (раздел "Символ")</span><span class="sxs-lookup"><span data-stu-id="59130-104">ComplexScriptFont Cell (Character Section)</span></span>

<span data-ttu-id="59130-105">Содержит номер шрифта, используемого для форматирования текста, состоящего из символов сложного.</span><span class="sxs-lookup"><span data-stu-id="59130-105">Contains the number of the font used to format text composed of complex script characters.</span></span> <span data-ttu-id="59130-106">Номера шрифтов зависят шрифты, установленные в системе.</span><span class="sxs-lookup"><span data-stu-id="59130-106">Font numbers vary according to the fonts installed on your system.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="59130-107">Замечания</span><span class="sxs-lookup"><span data-stu-id="59130-107">Remarks</span></span>

<span data-ttu-id="59130-108">На вкладке **Шрифт** в диалоговом окне **текст** (щелкните стрелку в **шрифта** группы на вкладке **Главная** ) перечислены размеры шрифтов сложных скриптов.</span><span class="sxs-lookup"><span data-stu-id="59130-108">Complex script font sizes are listed on the **Font** tab in the **Text** dialog box (click the arrow in the **Font** group on the **Home** tab).</span></span> <span data-ttu-id="59130-109">В этом списке отображается только в том случае, если вы добавили языка, который содержит символы азиатских или сложных сценариев, в диалоговом окне **Языковые параметры Microsoft Office** .</span><span class="sxs-lookup"><span data-stu-id="59130-109">This list appears only if you have added a language that contains Asian or complex script characters, in the **Microsoft Office Language Preferences** dialog box.</span></span> <span data-ttu-id="59130-110">(Нажмите кнопку **Пуск**, последовательно выберите пункты **Все программы**, нажмите кнопку **Microsoft Office**, средства **Microsoft Office**и затем выберите **Языковые параметры Microsoft Office**.</span><span class="sxs-lookup"><span data-stu-id="59130-110">(Click **Start**, click **All Programs**, click **Microsoft Office**, click **Microsoft Office Tools**, and then click **Microsoft Office Language Preferences**.</span></span>
  
<span data-ttu-id="59130-111">Число 0 (ноль) означает, что шрифт не указан.</span><span class="sxs-lookup"><span data-stu-id="59130-111">The number 0 (zero) means no font is specified.</span></span> <span data-ttu-id="59130-112">Латинский шрифт или шрифты по умолчанию используются.</span><span class="sxs-lookup"><span data-stu-id="59130-112">The Latin font or default fonts are used.</span></span>
  
<span data-ttu-id="59130-113">Чтобы получить ссылку на ячейку ComplexScriptSize по имени из другой формулы или из файла с помощью свойства **CellsU** , используйте:</span><span class="sxs-lookup"><span data-stu-id="59130-113">To get a reference to the ComplexScriptSize cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="59130-114">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="59130-114">Cell name:</span></span>  <br/> |<span data-ttu-id="59130-115">Char.ComplexScriptFont [ *i* ] где *i* = < 1 > 2, 3...</span><span class="sxs-lookup"><span data-stu-id="59130-115">Char.ComplexScriptFont[ *i*  ]           where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="59130-116">Для получения ссылки на ячейки ComplexScriptFont по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="59130-116">To get a reference to the ComplexScriptFont cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="59130-117">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="59130-117">Section index:</span></span>  <br/> |<span data-ttu-id="59130-118">**visSectionCharacter**</span><span class="sxs-lookup"><span data-stu-id="59130-118">**visSectionCharacter**</span></span> <br/> |
|<span data-ttu-id="59130-119">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="59130-119">Row index:</span></span>  <br/> |<span data-ttu-id="59130-120">**visRowCharacter** +  *i* где *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="59130-120">**visRowCharacter** +  *i*           where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="59130-121">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="59130-121">Cell index:</span></span>  <br/> |<span data-ttu-id="59130-122">**visCharacterComplexScriptFont**</span><span class="sxs-lookup"><span data-stu-id="59130-122">**visCharacterComplexScriptFont**</span></span> <br/> |
   

