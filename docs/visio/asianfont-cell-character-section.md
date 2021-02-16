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
description: Содержит количество шрифтов, используемых для формата текста, содержащего азиатские символы. Номера шрифтов зависят от шрифтов, установленных в системе.
ms.openlocfilehash: 4af7e590a7bd0733ad622f3df259aa6c01837c4b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406593"
---
# <a name="asianfont-cell-character-section"></a><span data-ttu-id="7b8dc-104">AsianFont Cell (Character Section)</span><span class="sxs-lookup"><span data-stu-id="7b8dc-104">AsianFont Cell (Character Section)</span></span>

<span data-ttu-id="7b8dc-105">Содержит количество шрифтов, используемых для формата текста, содержащего азиатские символы.</span><span class="sxs-lookup"><span data-stu-id="7b8dc-105">Contains the number of the font used to format the text containing Asian characters.</span></span> <span data-ttu-id="7b8dc-106">Номера шрифтов зависят от шрифтов, установленных в системе.</span><span class="sxs-lookup"><span data-stu-id="7b8dc-106">Font numbers vary according to the fonts installed on your system.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="7b8dc-107">Примечания</span><span class="sxs-lookup"><span data-stu-id="7b8dc-107">Remarks</span></span>

<span data-ttu-id="7b8dc-108">Азиатские шрифты перечислены на  вкладке **"Шрифт"** в диалоговом окне "Текст" (щелкните стрелку в группе шрифтов на вкладке  **"Главная").**</span><span class="sxs-lookup"><span data-stu-id="7b8dc-108">Asian fonts are listed on the **Font** tab in the **Text** dialog box (click the arrow in the **Font** group on the **Home** tab).</span></span> <span data-ttu-id="7b8dc-109">Этот список отображается, только если вы добавили язык, содержащий азиатские или сложные символы скрипта, в диалоговом окне Microsoft Office **Языковые** параметры.</span><span class="sxs-lookup"><span data-stu-id="7b8dc-109">This list appears only if you have added a language that contains Asian or complex script characters, in the **Microsoft Office Language Preferences** dialog box.</span></span> <span data-ttu-id="7b8dc-110">(Нажмите **кнопку**"Начните", выберите "Все программы", Microsoft Office **,** **Microsoft Office**"Инструменты" и выберите Microsoft Office **"Языковые параметры".**</span><span class="sxs-lookup"><span data-stu-id="7b8dc-110">(Click **Start**, click **All Programs**, click **Microsoft Office**, click **Microsoft Office Tools**, and then click **Microsoft Office Language Preferences**.</span></span>
  
<span data-ttu-id="7b8dc-111">Число 0 означает, что шрифт не указан.</span><span class="sxs-lookup"><span data-stu-id="7b8dc-111">The number 0 means no font is specified.</span></span> <span data-ttu-id="7b8dc-112">Латинский шрифт или шрифты по умолчанию используются, если они содержат необходимые символы.</span><span class="sxs-lookup"><span data-stu-id="7b8dc-112">The Latin font or default fonts are used if they contain the necessary characters.</span></span>
  
<span data-ttu-id="7b8dc-113">Чтобы получить ссылку на ячейку AsianFont по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте:</span><span class="sxs-lookup"><span data-stu-id="7b8dc-113">To get a reference to the AsianFont cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="7b8dc-114">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="7b8dc-114">Cell name:</span></span>  <br/> |<span data-ttu-id="7b8dc-115">Char.AsianFont[ *i*  ] где  *i*  = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="7b8dc-115">Char.AsianFont[ *i*  ]           where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="7b8dc-116">Чтобы получить ссылку на ячейку AsianFont по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="7b8dc-116">To get a reference to the AsianFont cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="7b8dc-117">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="7b8dc-117">Section index:</span></span>  <br/> |<span data-ttu-id="7b8dc-118">**visSectionCharacter**</span><span class="sxs-lookup"><span data-stu-id="7b8dc-118">**visSectionCharacter**</span></span> <br/> |
|<span data-ttu-id="7b8dc-119">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="7b8dc-119">Row index:</span></span>  <br/> |<span data-ttu-id="7b8dc-120">**visRowCharacter**  +   *i,* *где i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="7b8dc-120">**visRowCharacter** +  *i*           where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="7b8dc-121">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="7b8dc-121">Cell index:</span></span>  <br/> |<span data-ttu-id="7b8dc-122">**visCharacterAsianFont**</span><span class="sxs-lookup"><span data-stu-id="7b8dc-122">**visCharacterAsianFont**</span></span> <br/> |
   

