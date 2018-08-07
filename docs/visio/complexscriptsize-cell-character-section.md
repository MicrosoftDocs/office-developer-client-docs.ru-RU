---
title: Ячейка ComplexScriptSize (раздел "Символ")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033768
localization_priority: Normal
ms.assetid: f58687d7-2ba4-ff77-0bcc-3106867d89de
description: Размер шрифта, используемого для форматирования текста, состоящего из символов сложного.
ms.openlocfilehash: 4867ab57fa59b3a5e76598108fbb92b9bbab7913
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813439"
---
# <a name="complexscriptsize-cell-character-section"></a><span data-ttu-id="23693-103">Ячейка ComplexScriptSize (раздел "Символ")</span><span class="sxs-lookup"><span data-stu-id="23693-103">ComplexScriptSize Cell (Character Section)</span></span>

<span data-ttu-id="23693-104">Размер шрифта, используемого для форматирования текста, состоящего из символов сложного.</span><span class="sxs-lookup"><span data-stu-id="23693-104">The size of the font used to format text composed of complex script characters.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="23693-105">Замечания</span><span class="sxs-lookup"><span data-stu-id="23693-105">Remarks</span></span>

<span data-ttu-id="23693-106">На вкладке **Шрифт** в диалоговом окне **текст** (щелкните стрелку в **шрифта** группы на вкладке **Главная** ) перечислены размеры шрифтов сложных скриптов.</span><span class="sxs-lookup"><span data-stu-id="23693-106">Complex script font sizes are listed on the **Font** tab in the **Text** dialog box (click the arrow in the **Font** group on the **Home** tab).</span></span> <span data-ttu-id="23693-107">В этом списке отображается только в том случае, если вы добавили языка, который содержит символы азиатских или сложных сценариев, в диалоговом окне **Языковые параметры Microsoft Office** .</span><span class="sxs-lookup"><span data-stu-id="23693-107">This list appears only if you have added a language that contains Asian or complex script characters, in the **Microsoft Office Language Preferences** dialog box.</span></span> <span data-ttu-id="23693-108">(Нажмите кнопку **Пуск**, последовательно выберите пункты **Все программы**, нажмите кнопку **Microsoft Office**, средства **Microsoft Office**и затем выберите **Языковые параметры Microsoft Office**.</span><span class="sxs-lookup"><span data-stu-id="23693-108">(Click **Start**, click **All Programs**, click **Microsoft Office**, click **Microsoft Office Tools**, and then click **Microsoft Office Language Preferences**.</span></span>
  
<span data-ttu-id="23693-109">Это значение можно ввести размером явные точки или в процентном выражении.</span><span class="sxs-lookup"><span data-stu-id="23693-109">You can enter this value as an explicit point size or as a percentage.</span></span> <span data-ttu-id="23693-110">Если указывается процент значение основано на значение в ячейке размера.</span><span class="sxs-lookup"><span data-stu-id="23693-110">If you specify a percentage, the value is based on the value in the Size cell.</span></span> <span data-ttu-id="23693-111">Значение по умолчанию 0 (ноль) означает, что 100%.</span><span class="sxs-lookup"><span data-stu-id="23693-111">A default value of 0 (zero) means 100%.</span></span> 
  
<span data-ttu-id="23693-112">Чтобы получить ссылку на ячейку ComplexScriptSize по имени из другой формулы или из файла с помощью свойства **CellsU** , используйте:</span><span class="sxs-lookup"><span data-stu-id="23693-112">To get a reference to the ComplexScriptSize cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="23693-113">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="23693-113">Cell name:</span></span>  <br/> |<span data-ttu-id="23693-114">Char.ComplexScriptSize [ *i* ] где *i* = < 1 > 2, 3...</span><span class="sxs-lookup"><span data-stu-id="23693-114">Char.ComplexScriptSize[ *i*  ]           where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="23693-115">Для получения ссылки на ячейки ComplexScriptSize по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="23693-115">To get a reference to the ComplexScriptSize cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="23693-116">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="23693-116">Section index:</span></span>  <br/> |<span data-ttu-id="23693-117">**visSectionCharacter**</span><span class="sxs-lookup"><span data-stu-id="23693-117">**visSectionCharacter**</span></span> <br/> |
|<span data-ttu-id="23693-118">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="23693-118">Row index:</span></span>  <br/> |<span data-ttu-id="23693-119">**visRowCharacter** +  *i* где *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="23693-119">**visRowCharacter** +  *i*           where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="23693-120">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="23693-120">Cell index:</span></span>  <br/> |<span data-ttu-id="23693-121">**visCharacterComplexScriptSize**</span><span class="sxs-lookup"><span data-stu-id="23693-121">**visCharacterComplexScriptSize**</span></span> <br/> |
   

