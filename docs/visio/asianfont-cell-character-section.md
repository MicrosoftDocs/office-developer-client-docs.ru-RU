---
title: Ячейка AsianFont (раздел "Символ")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033764
localization_priority: Normal
ms.assetid: 45bfaaaa-52cc-f8b4-68e7-8b99e5788ce1
description: Содержит номер шрифта, используемого для форматирования текста, содержащий азиатских языков. Номера шрифтов зависят шрифты, установленные в системе.
ms.openlocfilehash: 1fbaa0b27a0c639519c302129142dcefe5708115
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813155"
---
# <a name="asianfont-cell-character-section"></a><span data-ttu-id="b7703-104">Ячейка AsianFont (раздел "Символ")</span><span class="sxs-lookup"><span data-stu-id="b7703-104">AsianFont Cell (Character Section)</span></span>

<span data-ttu-id="b7703-105">Содержит номер шрифта, используемого для форматирования текста, содержащий азиатских языков.</span><span class="sxs-lookup"><span data-stu-id="b7703-105">Contains the number of the font used to format the text containing Asian characters.</span></span> <span data-ttu-id="b7703-106">Номера шрифтов зависят шрифты, установленные в системе.</span><span class="sxs-lookup"><span data-stu-id="b7703-106">Font numbers vary according to the fonts installed on your system.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="b7703-107">Замечания</span><span class="sxs-lookup"><span data-stu-id="b7703-107">Remarks</span></span>

<span data-ttu-id="b7703-108">На вкладке **Шрифт** в диалоговом окне **текст** (щелкните стрелку в **шрифта** группы на вкладке **Главная** ) перечислены азиатских шрифтов.</span><span class="sxs-lookup"><span data-stu-id="b7703-108">Asian fonts are listed on the **Font** tab in the **Text** dialog box (click the arrow in the **Font** group on the **Home** tab).</span></span> <span data-ttu-id="b7703-109">В этом списке отображается только в том случае, если вы добавили языка, который содержит символы азиатских или сложных сценариев, в диалоговом окне **Языковые параметры Microsoft Office** .</span><span class="sxs-lookup"><span data-stu-id="b7703-109">This list appears only if you have added a language that contains Asian or complex script characters, in the **Microsoft Office Language Preferences** dialog box.</span></span> <span data-ttu-id="b7703-110">(Нажмите кнопку **Пуск**, последовательно выберите пункты **Все программы**, нажмите кнопку **Microsoft Office**, средства **Microsoft Office**и затем выберите **Языковые параметры Microsoft Office**.</span><span class="sxs-lookup"><span data-stu-id="b7703-110">(Click **Start**, click **All Programs**, click **Microsoft Office**, click **Microsoft Office Tools**, and then click **Microsoft Office Language Preferences**.</span></span>
  
<span data-ttu-id="b7703-111">Значение 0 означает, что шрифт не указан.</span><span class="sxs-lookup"><span data-stu-id="b7703-111">The number 0 means no font is specified.</span></span> <span data-ttu-id="b7703-112">Латинская или шрифты по умолчанию будут использоваться, если они с символами, необходимые.</span><span class="sxs-lookup"><span data-stu-id="b7703-112">The Latin font or default fonts are used if they contain the necessary characters.</span></span>
  
<span data-ttu-id="b7703-113">Чтобы получить ссылку на ячейку AsianFont по имени из другой формулы или из файла с помощью свойства **CellsU** , используйте:</span><span class="sxs-lookup"><span data-stu-id="b7703-113">To get a reference to the AsianFont cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b7703-114">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="b7703-114">Cell name:</span></span>  <br/> |<span data-ttu-id="b7703-115">Char.AsianFont [ *i* ] где *i* = < 1 > 2, 3...</span><span class="sxs-lookup"><span data-stu-id="b7703-115">Char.AsianFont[ *i*  ]           where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="b7703-116">Для получения ссылки на ячейки AsianFont по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="b7703-116">To get a reference to the AsianFont cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b7703-117">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="b7703-117">Section index:</span></span>  <br/> |<span data-ttu-id="b7703-118">**visSectionCharacter**</span><span class="sxs-lookup"><span data-stu-id="b7703-118">**visSectionCharacter**</span></span> <br/> |
|<span data-ttu-id="b7703-119">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="b7703-119">Row index:</span></span>  <br/> |<span data-ttu-id="b7703-120">**visRowCharacter** +  *i* где *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="b7703-120">**visRowCharacter** +  *i*           where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="b7703-121">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="b7703-121">Cell index:</span></span>  <br/> |<span data-ttu-id="b7703-122">**visCharacterAsianFont**</span><span class="sxs-lookup"><span data-stu-id="b7703-122">**visCharacterAsianFont**</span></span> <br/> |
   

