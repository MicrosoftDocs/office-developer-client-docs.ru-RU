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
# <a name="complexscriptsize-cell-character-section"></a><span data-ttu-id="34f50-103">ComplexScriptSize Cell (Character Section)</span><span class="sxs-lookup"><span data-stu-id="34f50-103">ComplexScriptSize Cell (Character Section)</span></span>

<span data-ttu-id="34f50-104">Размер шрифта, используемого для формата текста, состоящего из сложных символов сценария.</span><span class="sxs-lookup"><span data-stu-id="34f50-104">The size of the font used to format text composed of complex script characters.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="34f50-105">Примечания</span><span class="sxs-lookup"><span data-stu-id="34f50-105">Remarks</span></span>

<span data-ttu-id="34f50-106">Сложные размеры шрифтов скрипта перечислены на вкладке **Font** в диалоговом окне **Text** (щелкните стрелку в группе **Шрифт** на вкладке **Главная).**</span><span class="sxs-lookup"><span data-stu-id="34f50-106">Complex script font sizes are listed on the **Font** tab in the **Text** dialog box (click the arrow in the **Font** group on the **Home** tab).</span></span> <span data-ttu-id="34f50-107">Этот список отображается только в том случае, если в **диалоговом окне Языковые** предпочтения добавлен язык, содержащий азиатские или сложные символы скрипта, Microsoft Office языковые предпочтения.</span><span class="sxs-lookup"><span data-stu-id="34f50-107">This list appears only if you have added a language that contains Asian or complex script characters, in the **Microsoft Office Language Preferences** dialog box.</span></span> <span data-ttu-id="34f50-108">(Нажмите **кнопку Начните,** нажмите кнопку Все **программы,** **нажмите Microsoft Office,** **нажмите Microsoft Office инструменты,** а затем нажмите кнопку Microsoft Office **Языковые предпочтения**.</span><span class="sxs-lookup"><span data-stu-id="34f50-108">(Click **Start**, click **All Programs**, click **Microsoft Office**, click **Microsoft Office Tools**, and then click **Microsoft Office Language Preferences**.</span></span>
  
<span data-ttu-id="34f50-109">Это значение можно ввести в виде явного размера точки или в процентах.</span><span class="sxs-lookup"><span data-stu-id="34f50-109">You can enter this value as an explicit point size or as a percentage.</span></span> <span data-ttu-id="34f50-110">Если указать процент, значение основано на значении в ячейке Size.</span><span class="sxs-lookup"><span data-stu-id="34f50-110">If you specify a percentage, the value is based on the value in the Size cell.</span></span> <span data-ttu-id="34f50-111">Значение по умолчанию 0 (ноль) означает 100%.</span><span class="sxs-lookup"><span data-stu-id="34f50-111">A default value of 0 (zero) means 100%.</span></span> 
  
<span data-ttu-id="34f50-112">Чтобы получить ссылку на ячейку ComplexScriptSize по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте:</span><span class="sxs-lookup"><span data-stu-id="34f50-112">To get a reference to the ComplexScriptSize cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="34f50-113">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="34f50-113">Cell name:</span></span>  <br/> |<span data-ttu-id="34f50-114">Char.ComplexScriptSize[i] где *i* = <1>, 2, 3... </span><span class="sxs-lookup"><span data-stu-id="34f50-114">Char.ComplexScriptSize[ *i*  ]           where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="34f50-115">Чтобы получить ссылку на ячейку ComplexScriptSize по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="34f50-115">To get a reference to the ComplexScriptSize cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="34f50-116">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="34f50-116">Section index:</span></span>  <br/> |<span data-ttu-id="34f50-117">**visSectionCharacter**</span><span class="sxs-lookup"><span data-stu-id="34f50-117">**visSectionCharacter**</span></span> <br/> |
|<span data-ttu-id="34f50-118">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="34f50-118">Row index:</span></span>  <br/> |<span data-ttu-id="34f50-119">**visRowCharacter**  +   *i,* *где i* = 0, 1, 2 ...</span><span class="sxs-lookup"><span data-stu-id="34f50-119">**visRowCharacter** +  *i*           where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="34f50-120">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="34f50-120">Cell index:</span></span>  <br/> |<span data-ttu-id="34f50-121">**visCharacterComplexScriptSize**</span><span class="sxs-lookup"><span data-stu-id="34f50-121">**visCharacterComplexScriptSize**</span></span> <br/> |
   

