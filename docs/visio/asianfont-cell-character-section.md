---
title: AsianFont Cell (Character Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033764
localization_priority: Normal
ms.assetid: 45bfaaaa-52cc-f8b4-68e7-8b99e5788ce1
description: Содержит номер шрифта, используемого для форматирования текста, содержащего восточноазиатские символы. Номера шрифтов зависят от установленных в системе шрифтов.
ms.openlocfilehash: 4af7e590a7bd0733ad622f3df259aa6c01837c4b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341331"
---
# <a name="asianfont-cell-character-section"></a><span data-ttu-id="c86b6-104">AsianFont Cell (Character Section)</span><span class="sxs-lookup"><span data-stu-id="c86b6-104">AsianFont Cell (Character Section)</span></span>

<span data-ttu-id="c86b6-105">Содержит номер шрифта, используемого для форматирования текста, содержащего восточноазиатские символы.</span><span class="sxs-lookup"><span data-stu-id="c86b6-105">Contains the number of the font used to format the text containing Asian characters.</span></span> <span data-ttu-id="c86b6-106">Номера шрифтов зависят от установленных в системе шрифтов.</span><span class="sxs-lookup"><span data-stu-id="c86b6-106">Font numbers vary according to the fonts installed on your system.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="c86b6-107">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c86b6-107">Remarks</span></span>

<span data-ttu-id="c86b6-108">Восточноазиатские шрифты отображаются на вкладке **Шрифт** в диалоговом окне **текст** (щелкните стрелку в группе **Шрифт** на вкладке **Главная** ).</span><span class="sxs-lookup"><span data-stu-id="c86b6-108">Asian fonts are listed on the **Font** tab in the **Text** dialog box (click the arrow in the **Font** group on the **Home** tab).</span></span> <span data-ttu-id="c86b6-109">Этот список отображается только в том случае, если в диалоговом окне **языковые параметры Microsoft Office** добавлен язык, содержащий восточноазиатские или сложные знаки.</span><span class="sxs-lookup"><span data-stu-id="c86b6-109">This list appears only if you have added a language that contains Asian or complex script characters, in the **Microsoft Office Language Preferences** dialog box.</span></span> <span data-ttu-id="c86b6-110">(Нажмите кнопку **Пуск**, **выберите все программы**, **Microsoft Office**, **средства Microsoft Office**, а затем выберите языковые **Параметры Microsoft Office**.</span><span class="sxs-lookup"><span data-stu-id="c86b6-110">(Click **Start**, click **All Programs**, click **Microsoft Office**, click **Microsoft Office Tools**, and then click **Microsoft Office Language Preferences**.</span></span>
  
<span data-ttu-id="c86b6-111">Число 0 означает, что шрифт не указан.</span><span class="sxs-lookup"><span data-stu-id="c86b6-111">The number 0 means no font is specified.</span></span> <span data-ttu-id="c86b6-112">Латинский шрифт или шрифты по умолчанию используются, если они содержат необходимые символы.</span><span class="sxs-lookup"><span data-stu-id="c86b6-112">The Latin font or default fonts are used if they contain the necessary characters.</span></span>
  
<span data-ttu-id="c86b6-113">Чтобы получить ссылку на ячейку AsianFont по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте следующее:</span><span class="sxs-lookup"><span data-stu-id="c86b6-113">To get a reference to the AsianFont cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="c86b6-114">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="c86b6-114">Cell name:</span></span>  <br/> |<span data-ttu-id="c86b6-115">Char. AsianFont [ *i* ], где *i* = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="c86b6-115">Char.AsianFont[ *i*  ]           where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="c86b6-116">Чтобы получить ссылку на ячейку AsianFont по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="c86b6-116">To get a reference to the AsianFont cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="c86b6-117">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="c86b6-117">Section index:</span></span>  <br/> |<span data-ttu-id="c86b6-118">**Виссектиончарактер**</span><span class="sxs-lookup"><span data-stu-id="c86b6-118">**visSectionCharacter**</span></span> <br/> |
|<span data-ttu-id="c86b6-119">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="c86b6-119">Row index:</span></span>  <br/> |<span data-ttu-id="c86b6-120">**висровчарактер** +  *i* , где *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="c86b6-120">**visRowCharacter** +  *i*           where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="c86b6-121">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="c86b6-121">Cell index:</span></span>  <br/> |<span data-ttu-id="c86b6-122">**Висчарактерасианфонт**</span><span class="sxs-lookup"><span data-stu-id="c86b6-122">**visCharacterAsianFont**</span></span> <br/> |
   

